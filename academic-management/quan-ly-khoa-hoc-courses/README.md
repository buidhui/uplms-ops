# Quản lý khóa học

Khóa học là đơn vị nội dung gốc của hệ thống: nó chứa bài học, bài kiểm tra, tài liệu và chứng chỉ. Lớp học ở [Class Management](../../class-management/tong-quan-lop-hoc-classes.md) không tự chứa nội dung — lớp gắn vào một khóa học đã publish và học viên trong lớp học theo nội dung của khóa đó. Vì vậy khóa học phải hoàn chỉnh trước khi mở lớp.

#### Luồng tạo khóa học

Một khóa học được dựng qua 4 bước tuần tự:

1. **Tạo khóa học** — điền thông tin cơ bản: tên, mã, danh mục, loại khóa (Normal hoặc Foundation), điểm đạt và tỷ trọng điểm thành phần.
2. **Tạo nội dung khóa học** — dựng các hoạt động học và hoạt động kiểm tra bên trong khóa.
3. **Thêm tài liệu khóa học** — đính kèm học liệu dùng chung cho khóa.
4. **Thêm chứng chỉ khóa học** — gắn mẫu chứng chỉ cấp cho học viên khi hoàn thành.

<figure><img src="../../.gitbook/assets/image (941).png" alt=""><figcaption></figcaption></figure>

#### Trạng thái khóa học

| Trạng thái    | Ý nghĩa                                                                        |
| ------------- | ------------------------------------------------------------------------------ |
| **Draft**     | Khóa học đang tạo dở, chưa publish.                                            |
| **Publish**   | Khóa học đã hoàn chỉnh và sẵn sàng để thêm vào lớp học.                        |
| **Lock**      | Khóa học đã có ít nhất một học viên bắt đầu học.                               |
| **Block**     | Khóa học bị chặn, không thể thêm vào lớp học.                                  |

{% hint style="warning" %}
Khóa học chỉ được **Publish** khi đã tạo nội dung và gắn chứng chỉ. Khóa ở trạng thái **Draft** hoặc **Block** không thêm được vào lớp.
{% endhint %}

#### Nội dung trong mục này

* [**Danh sách khóa học**](xem-danh-sach-khoa-hoc-course-list.md): xem, tìm kiếm và lọc khóa học theo tên, trạng thái, danh mục.
* [**Tạo khóa học**](tao-khoa-hoc-course-infor.md): bước đầu tiên — thông tin cơ bản, loại khóa, điểm đạt và điểm thành phần.
* [**Tạo nội dung khóa học**](tao-noi-dung-khoa-hoc-course-content/README.md): dựng hoạt động học và hoạt động kiểm tra trong khóa.
* [**Thêm tài liệu khóa học**](tai-len-tai-lieu-cho-khoa-hoc-resource.md): đính kèm học liệu cho khóa.
* [**Thêm chứng chỉ khóa học**](gan-chung-chi-cho-khoa-hoc-certificate.md): gắn mẫu chứng chỉ hoàn thành.

***

### Business Rule

<details>

<summary>Quy tắc chung về Course</summary>

| Mã rule       | Business Rule                                                                                                                                     |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-COURSE-001 | Người dùng chỉ được truy cập module Course khi đã đăng nhập thành công vào hệ thống UpLMS Ops và được phân quyền phù hợp.                         |
| BR-COURSE-002 | Người dùng chỉ được tạo, chỉnh sửa, xóa hoặc thay đổi trạng thái khóa học nếu tài khoản có quyền tương ứng.                                       |
| BR-COURSE-003 | Một khóa học sau khi tạo mặc định ở trạng thái **Draft**.                                                                                         |
| BR-COURSE-004 | Một khóa học hoàn chỉnh cần đi qua 4 bước cấu hình: **Course Info → Course Content → Resource → Certificate**.                                    |
| BR-COURSE-005 | Thanh process cho phép Admin điều hướng giữa các bước tạo khóa học, tuy nhiên mỗi bước vẫn cần đáp ứng điều kiện dữ liệu tương ứng trước khi lưu. |
| BR-COURSE-006 | Cấu trúc nội dung khóa học gồm 2 cấp: **Section → Activity**.                                 |
| BR-COURSE-007 | Danh sách khóa học hỗ trợ tìm kiếm/lọc theo tên khóa học, Course Category, Status, Type, khoảng ngày và Sort by.                                          |

</details>

<details>

<summary>Quy tắc về Course Info</summary>

| Mã rule            | Business Rule                                                                                                                                       |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-COURSE-INFO-001 | Khi tạo mới khóa học, các trường bắt buộc gồm: **Course Name, Course Category, Type, Pass Point, điểm các thành phần**.                             |
| BR-COURSE-INFO-002 | Trường **Name** dùng để hiển thị tên khóa học trên hệ thống.                                                                                        |
| BR-COURSE-INFO-003 | Trường **Code** là mã định danh của khóa học và không được trùng với Code của khóa học đã tồn tại.                                                  |
| BR-COURSE-INFO-004 | Trường **Tag** không bắt buộc. Admin có thể tạo tag mới bằng cách nhập nội dung tag.                                                                |
| BR-COURSE-INFO-005 | Trường **Course Category** bắt buộc chọn từ danh sách danh mục có sẵn trên hệ thống.                                                                         |
| BR-COURSE-INFO-007 | Một khóa học chỉ được chọn một **Type** tại thời điểm tạo.                                                                                          |
| BR-COURSE-INFO-008 | Hệ thống hỗ trợ 2 Type: **Normal Course** và **Foundation Course**.                                                  |
| BR-COURSE-INFO-009 | Nếu Type = **Foundation Course**, Admin bắt buộc chọn ít nhất một level cho khóa học.                                                               |
| BR-COURSE-INFO-010 | Nếu Type = **Normal Course**, Admin có thể gắn kèm một **Foundation Course**; khi đó học viên phải hoàn thành khóa Foundation trước khi học khóa chính. |
| BR-COURSE-INFO-011 | Với **Normal Course**, Admin có thể chọn hoặc không chọn Foundation Course.                                                         |
| BR-COURSE-INFO-012 | Trường **Pass Point** là điểm yêu cầu học viên phải đạt để có thể nhận chứng chỉ của khóa học.                                                      |
| BR-COURSE-INFO-013 | Tổng điểm các thành phần của khóa học phải bằng **100**.                                                                                            |
| BR-COURSE-INFO-014 | Các thành phần điểm gồm: **Tiến độ học, Graded Quiz, Chapter Test, Topic Test, Mid Test, Final Test**.                                              |
| BR-COURSE-INFO-015 | Admin chỉ có thể lưu Course Info khi các trường bắt buộc đã được nhập hợp lệ.                                                                       |

</details>

<details>

<summary>Quy tắc về loại khóa học</summary>

| Mã rule            | Business Rule                                                                                                                                          |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| BR-COURSE-TYPE-001 | **Foundation Course** là khóa học nền tảng, được gắn tương ứng với level của học viên.                                                                 |
| BR-COURSE-TYPE-004 | **Normal Course** là khóa học thường, có thể yêu cầu học viên hoàn thành một số Foundation Course trước khi học.                                       |
| BR-COURSE-TYPE-007 | Khi Block một **Foundation Course** đã được gắn với Normal Course, hệ thống cảnh báo rằng khóa Foundation sẽ bị unlink khỏi các khóa Normal liên quan. |
| BR-COURSE-TYPE-008 | Khi Block khóa **Normal Course**, hệ thống cảnh báo rằng khóa học sẽ bị remove khỏi các lớp chưa bắt đầu.                                  |

</details>

<details>

<summary>Quy tắc về Course Content</summary>

| Mã rule        | Business Rule                                                                                                                          |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| BR-CONTENT-001 | Admin cần tạo nội dung theo thứ tự: **Section → Activity**.                                  |
| BR-CONTENT-002 | Admin cần tạo **Section** trước khi tạo **Activity**.                                                                                |
| BR-CONTENT-005 | **Learning Outcome** được tạo ở cấp **Subsection**.                                                                                    |
| BR-CONTENT-006 | Một Subsection có thể có một hoặc nhiều Learning Outcome.                                                                              |
| BR-CONTENT-007 | Một Activity có thể được gắn với một hoặc nhiều Learning Outcome đã tạo.                                                               |
| BR-CONTENT-008 | Các mã **Section Code** và **Activity Code** được hệ thống tạo tự động theo rule của khóa học.                   |
| BR-CONTENT-009 | Mỗi Activity bắt buộc nhập **Tên activity, Activity Code, Duration, Type of Activity, Grade Activity**.                                |
| BR-CONTENT-010 | **Type of Activity** dùng để hiển thị icon trên giao diện học viên UpLMS.                                                              |
| BR-CONTENT-011 | Type of Activity gồm: **Text, Video, Quiz, Pass Exam Analysis**.                                                                       |
| BR-CONTENT-012 | **Grade Activity** xác định Activity có tính điểm hay không. Hệ thống mặc định chọn **Yes**.                                           |
| BR-CONTENT-013 | Activity có thể đính kèm một hoặc nhiều Resource.                                                                                      |
| BR-CONTENT-014 | File Resource đính kèm trong Activity có dung lượng tối đa **500MB/file**.                                                             |
| BR-CONTENT-015 | Admin có thể tạo nội dung khóa học bằng 3 cách: tạo thủ công, copy cấu phần từ khóa học khác, hoặc link cấu phần học từ khóa học khác. |
| BR-CONTENT-017 | Không được link chồng các cấu phần học để tránh vòng lặp dữ liệu giữa các khóa học.                                                    |
| BR-CONTENT-018 | Admin có thể preview các cấp nội dung gồm **Section, Activity**.                                                                 |
| BR-CONTENT-019 | Admin có thể Lock/Unlock các nội dung đã tạo.                                                                                          |
| BR-CONTENT-020 | Admin có thể Show Lock/Hide Lock để kiểm soát việc hiển thị trạng thái khóa trên giao diện học viên.                                   |
| BR-CONTENT-021 | Admin có thể Change CTA to Preview/Change CTA to Begin cho các nội dung đã tạo.                                                        |
|                | Khóa học chỉ được Publish khi đã được tạo nội dung và gán chứng chỉ.                                                                   |

</details>

<details>

<summary>Quy tắc về Section</summary>

| Mã rule        | Business Rule                                                                                                                                 |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-SECTION-001 | Section là cấp nội dung lớn nhất trong cấu trúc khóa học.                                                                             |
| BR-SECTION-002 | Khi tạo Section, trường **Tên Section** là bắt buộc.                                                                                          |
| BR-SECTION-003 | **Section Code** là bắt buộc và được hệ thống tự động tạo.                                                                                    |
| BR-SECTION-004 | Section Code được tạo theo rule: **Code khóa học\_S\[Số thứ tự tạo mới section trong khóa]**.                                                 |
| BR-SECTION-005 | **Foundation Content** của Section cho phép chọn nhiều giá trị.                                                                               |
| BR-SECTION-006 | **Key content of** chỉ hiển thị khi chỉnh sửa Section.                                                                                        |
| BR-SECTION-007 | Nếu Section A được đánh dấu là Foundation Content của Section B, thì tại màn Edit của Section A, trường Key content of sẽ hiển thị Section B. |
| BR-SECTION-008 | Admin có thể tạo Activity, tạo bài kiểm tra, Edit, Preview hoặc Delete Section từ menu Action.                          |

</details>

<details>

<summary>Quy tắc về Activity và Document</summary>

| Mã rule         | Business Rule                                                                          |
| --------------- | -------------------------------------------------------------------------------------- |
| BR-ACTIVITY-001 | Activity phải thuộc một Section đã tồn tại.                                               |
| BR-ACTIVITY-002 | Một Activity có thể có một hoặc nhiều Tab.                                             |
| BR-ACTIVITY-003 | Mỗi Tab có thể có một hoặc nhiều Document.                                             |
| BR-ACTIVITY-004 | Document trong Activity gồm 3 loại: **Text, Video, Quiz**.                             |
| BR-ACTIVITY-005 | Với Document dạng Text, Admin nhập nội dung dạng chữ và chọn **Save Document** để lưu. |
| BR-ACTIVITY-006 | Với Document dạng Video, Admin có thể chọn **Single Video** hoặc **Multiple Videos**.  |
| BR-ACTIVITY-007 | Với **Multiple Videos**, Admin có thể chọn từ 1 đến 3 video.                           |
| BR-ACTIVITY-008 | Video có thể được upload trực tiếp từ thiết bị hoặc chọn từ kho Resource của hệ thống. |
| BR-ACTIVITY-009 | Với video upload từ thiết bị, Admin có thể cấu hình **Timeline, Question, Settings**.  |
| BR-ACTIVITY-010 | Nội dung mô tả Timeline không được bỏ trống.                                           |
| BR-ACTIVITY-011 | Timeline được sắp xếp theo thứ tự thời gian của video.                                 |
| BR-ACTIVITY-012 | Admin có thể thêm nhiều câu hỏi vào một Video.                                         |
| BR-ACTIVITY-013 | Câu hỏi trong Video được sắp xếp theo thứ tự thời gian của video.                      |
| BR-ACTIVITY-014 | Tab Settings của Video dùng để cấu hình các câu hỏi đã thêm tại tab Question.          |
| BR-ACTIVITY-015 | Với Document dạng Quiz, Admin thực hiện theo luồng tạo Test/Quiz.                      |

</details>

<details>

<summary>Quy tắc về Test/Quiz trong Course</summary>

| Mã rule     | Business Rule                                                                                                              |
| ----------- | -------------------------------------------------------------------------------------------------------------------------- |
| BR-TEST-001 | Test/Quiz chỉ áp dụng trong phạm vi Course.                                                                                |
| BR-TEST-002 | Các loại bài test có thể tạo gồm: **Midterm Test, Final Test, Chapter/Module Test, Quiz Test**. |
| BR-TEST-006 | **Quiz Test** được tạo khi Admin chọn Document = Quiz trong Tab.                                                           |
| BR-TEST-007 | Type of Test gồm: **Multiple Choice, Constructed, Mixed**.                                                                 |
| BR-TEST-008 | Nếu Type of Test = Multiple Choice, hệ thống chỉ hiển thị câu hỏi trắc nghiệm ở bước Add Question.                         |
| BR-TEST-009 | Nếu Type of Test = Constructed, hệ thống chỉ hiển thị câu hỏi tự luận ở bước Add Question.                                 |
| BR-TEST-010 | Nếu Type of Test = Mixed, hệ thống hiển thị cả câu hỏi trắc nghiệm và tự luận.                                             |
| BR-TEST-011 | Test Mode gồm **Tutor** và **Timed**.                                                                                      |
| BR-TEST-012 | Nếu Test Mode = Timed, Admin bắt buộc nhập Duration theo giờ và phút.                                                      |
| BR-TEST-013 | Manual Grading chỉ hiển thị với Type of Test = Constructed hoặc Mixed.                                                     |
| BR-TEST-014 | Nếu Manual Grading = Yes, bài kiểm tra được chấm điểm thủ công bởi đội SX.                                                 |
| BR-TEST-015 | Nếu Manual Grading = No, bài kiểm tra được hệ thống chấm điểm tự động.                                                     |
| BR-TEST-016 | Với Quiz/Chapter Test/Topic Test/Midterm Test/Final Test, nếu Manual Grading = Yes thì Graded Assignment = Yes.            |
| BR-TEST-018 | Grading Preference gồm **After each question** và **After all questions**.                                                 |
| BR-TEST-019 | Pass Point mặc định là **Auto 50%**.                                                                                       |
| BR-TEST-020 | Nếu Pass Point = Manual, Admin cần nhập số điểm pass point.                                                                |
| BR-TEST-021 | Attempt mặc định là **Unlimited**.                                                                                         |
| BR-TEST-022 | Nếu Attempt = Limited, Admin cần nhập số lần học viên được phép nộp bài.                                                   |
| BR-TEST-023 | Total Score có thể khác 100 nhưng phải lớn hơn 0.                                                                          |
| BR-TEST-024 | Total Score chỉ cho phép phần thập phân tối đa 2 chữ số.                                                                   |

</details>

<details>

<summary>Quy tắc về Add Question trong Test/Quiz</summary>

| Mã rule         | Business Rule                                                                                                        |
| --------------- | -------------------------------------------------------------------------------------------------------------------- |
| BR-QUESTION-001 | Câu hỏi thêm vào Test/Quiz được lấy từ Question Bank.                                                                |
| BR-QUESTION-002 | Danh sách câu hỏi hiển thị phụ thuộc vào Type of Test.                                                               |
| BR-QUESTION-003 | Câu hỏi được nhóm theo Item Set.                                                                                     |
| BR-QUESTION-004 | Item Set được tạo gần đây nhất hiển thị ở đầu danh sách.                                                             |
| BR-QUESTION-005 | Các câu hỏi trong cùng một Item Set được sắp xếp theo thời gian tạo từ gần đến xa.                                   |
| BR-QUESTION-006 | Câu hỏi trắc nghiệm và tự luận có thể hiển thị xen kẽ theo đúng thứ tự tạo trong Item Set.                           |
| BR-QUESTION-007 | Nếu Admin chọn đơn lẻ từng câu hỏi, câu nào được chọn trước sẽ đứng trước.                                           |
| BR-QUESTION-008 | Nếu Admin chọn toàn bộ câu hỏi trong trang, thứ tự câu hỏi giữ nguyên như thứ tự đang hiển thị tại màn Add Question. |
| BR-QUESTION-009 | Nếu Admin chọn một câu hỏi, sau đó bỏ chọn và chọn lại, câu hỏi đó được đưa xuống cuối danh sách.                    |
| BR-QUESTION-010 | Thứ tự câu hỏi tại Setup Score và Reorder phụ thuộc vào thứ tự Admin chọn câu hỏi tại Add Question.                  |
| BR-QUESTION-011 | Nếu bài Test/Quiz đã có học viên làm, Admin chỉ được xem thông tin tại bước Add Question và không thể chỉnh sửa.     |

</details>

<details>

<summary>Quy tắc về Setup Score trong Test/Quiz</summary>

| Mã rule      | Business Rule                                                                                                                         |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| BR-SCORE-001 | Màn Setup Score gồm khu vực cài đặt điểm toàn bài và khu vực danh sách câu hỏi.                                                       |
| BR-SCORE-002 | Total Score là tổng điểm tối đa của bài Test/Quiz.                                                                                    |
| BR-SCORE-003 | Current Score là tổng điểm hiện tại của toàn bộ câu hỏi, được hệ thống tự tính.                                                       |
| BR-SCORE-004 | Nếu Current Score khác Total Score, khi chọn Next hệ thống báo lỗi: **“Mark of all questions not equal \[Total Score]”**.             |
| BR-SCORE-005 | Nếu Current Score bằng Total Score, Admin được chuyển sang bước Reorder.                                                              |
| BR-SCORE-006 | Score Distribution gồm: **Evenly across all questions, Evenly by Question Type, Custom**.                                             |
| BR-SCORE-007 | Nếu Score Distribution = Evenly across all questions, hệ thống chia đều Total Score cho toàn bộ câu hỏi.                              |
| BR-SCORE-008 | Nếu Score Distribution = Evenly by Question Type, Admin nhập MCQ Score và Essay Score, hệ thống chia đều điểm theo từng nhóm câu hỏi. |
| BR-SCORE-009 | MCQ Score chỉ hiển thị khi Score Distribution = Evenly by Question Type.                                                              |
| BR-SCORE-010 | Essay Score chỉ hiển thị khi Score Distribution = Evenly by Question Type.                                                            |
| BR-SCORE-011 | MCQ Score phải lớn hơn 0 và nhỏ hơn Total Score.                                                                                      |
| BR-SCORE-012 | Essay Score phải lớn hơn 0 và nhỏ hơn Total Score.                                                                                    |
| BR-SCORE-013 | Nếu MCQ Score không hợp lệ, hệ thống báo lỗi: **“MCQ Score must be between 0 and \[Total Score]”**.                                   |
| BR-SCORE-014 | Nếu Essay Score không hợp lệ, hệ thống báo lỗi: **“Essay Score must be between 0 and \[Total Score]”**.                               |
| BR-SCORE-015 | Nếu Score Distribution = Custom, Admin tự nhập điểm cho từng câu hỏi.                                                                 |
| BR-SCORE-016 | Khi Score Distribution = Custom, Admin có thể setup điểm hàng loạt nếu chọn từ 2 câu hỏi trở lên.                                     |
| BR-SCORE-017 | Converted Mark được tính theo công thức: **Converted Mark = Mark / Total Score × 100**.                                               |
| BR-SCORE-018 | Nếu bài Test/Quiz đã có học viên làm, Admin chỉ được xem thông tin tại Setup Score và không thể chỉnh sửa.                            |

</details>

<details>

<summary>Quy tắc về Reorder câu hỏi</summary>

| Mã rule        | Business Rule                                                                            |
| -------------- | ---------------------------------------------------------------------------------------- |
| BR-REORDER-001 | Thứ tự mặc định tại màn Reorder là thứ tự Admin đã tick câu hỏi tại bước Add Question.   |
| BR-REORDER-002 | STT phản ánh thứ tự thực tế của câu hỏi trong bài Test/Quiz.                             |
| BR-REORDER-003 | Admin có thể di chuyển một câu hỏi bằng kéo thả.                                         |
| BR-REORDER-004 | Admin có thể chọn **Move to top** để đưa câu hỏi lên đầu danh sách.                      |
| BR-REORDER-005 | Admin có thể chọn **Move to bottom** để đưa câu hỏi xuống cuối danh sách.                |
| BR-REORDER-006 | Admin có thể chọn **Move to position** để chuyển câu hỏi đến vị trí xác định.            |
| BR-REORDER-007 | Admin chỉ có thể di chuyển nhiều câu hỏi cùng lúc nếu chọn từ 2 câu hỏi liền kề trở lên. |
| BR-REORDER-008 | Ví dụ chọn câu hỏi 2, 3, 4, 5 là hợp lệ.                                                 |
| BR-REORDER-009 | Ví dụ chọn câu hỏi 1, 3, 4, 5 là không hợp lệ.                                           |
| BR-REORDER-010 | Sau khi sắp xếp xong, Admin chọn Finish để quay lại màn Test/Quiz Detail.                |

</details>

<details>

<summary>Quy tắc chỉnh sửa khóa học</summary>

| Mã rule     | Business Rule                                                                                                                                                                     |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-EDIT-001 | Nếu lớp chưa có học viên hoặc có học viên nhưng học viên chưa học, Admin được sửa tất cả thông tin khóa học.                                                                      |
| BR-EDIT-002 | Nếu đã có học viên học nhưng chưa có học viên nào học xong, Course Info vẫn được sửa tất cả thông tin.                                                                            |
| BR-EDIT-003 | Nếu đã có học viên học nhưng chưa học xong, Admin được sửa/xóa Section, Activity, Tab dạng Text hoặc Video nếu không chứa Test/Quiz/Case Study đã có người làm. |
| BR-EDIT-004 | Nếu đã có học viên học nhưng chưa học xong, Admin được phép kéo thả cấu phần học.                                                                                                 |
| BR-EDIT-005 | Nếu đã có học viên học nhưng chưa học xong, Admin được thêm cấu phần học và bài Test.                                                                                             |
| BR-EDIT-006 | Với Test/Quiz/Case Study đã có người làm, Admin không được xóa bài test/quiz/case study và không được xóa cấu phần chứa các bài này.                                              |
| BR-EDIT-007 | Với Test/Quiz đã có người làm, Admin không được chỉnh sửa Type of Test, Test Mode, Graded Assignment, Grading Preference, Pass Point, Attempt.                                    |
| BR-EDIT-008 | Với Test/Quiz đã có người làm, danh sách câu hỏi chỉ được xem, không được thêm/xóa/chỉnh sửa tại bước Add Question.                                                               |
| BR-EDIT-009 | Với Test/Quiz chưa có người làm, Admin được sửa toàn bộ Setting, thêm câu hỏi, xóa câu hỏi và xóa bài test.                                                                       |
| BR-EDIT-010 | Nếu đã có ít nhất một học viên học xong khóa học, Admin được sửa tất cả Course Info.                                                                                              |
| BR-EDIT-011 | Nếu đã có học viên học xong, Admin được thêm cấu phần học nhưng không được thêm Test/Quiz/Case Study.                                                                             |
| BR-EDIT-012 | Nếu đã có học viên học xong, Admin chỉ được link các cấu phần học không chứa Test/Quiz/Case Study.                                                                                |
| BR-EDIT-013 | Nếu đã có học viên học xong, các bài Test/Quiz/Case Study đã tồn tại không được chỉnh sửa toàn bộ cài đặt.                                                                        |
| BR-EDIT-014 | Nếu đã có học viên học xong, Admin không xóa được Test/Quiz/Case Study và các cấu phần chứa các bài này.                                                                          |
| BR-EDIT-015 | Resource có thể được thêm hoặc xóa khi chỉnh sửa khóa học.                                                                                                                        |
| BR-EDIT-016 | Certificate có thể được thêm hoặc đổi Template khi chỉnh sửa khóa học, nếu hệ thống cho phép.                                                                                     |
| BR-EDIT-017 | Với khóa học đã có học viên học, các cấu phần mới thêm sẽ không hiển thị ngay trên giao diện học viên để tránh ảnh hưởng tiến trình học.                                          |

</details>

<details>

<summary>Quy tắc về cập nhật cấu phần học mới cho học viên</summary>

| Mã rule                | Business Rule                                                                                                                    |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| BR-STUDENT-CONTENT-001 | Khi khóa học đã có học viên học, cấu phần học mới thêm không tự động hiển thị ngay cho học viên.                                 |
| BR-STUDENT-CONTENT-002 | Để học viên nhìn thấy cấu phần mới, Admin cần cập nhật Course Content cho lớp hoặc cho từng học viên.                            |
| BR-STUDENT-CONTENT-003 | Với cập nhật cho toàn bộ học viên trong lớp, Admin vào Class List, chọn Action của lớp và chọn **Edit Course Content**.          |
| BR-STUDENT-CONTENT-004 | Admin tick chọn học phần mới thêm và chọn Save để lưu cấu phần học cho toàn bộ học viên thuộc lớp.                               |
| BR-STUDENT-CONTENT-005 | Với cập nhật cho từng học viên, Admin vào lớp, chọn **List Students**, chọn Action của học viên và chọn **Edit Course Content**. |
| BR-STUDENT-CONTENT-006 | Admin tick chọn học phần mới thêm và chọn Save để lưu cấu phần học cho học viên đó.                                              |

</details>

<details>

<summary>Quy tắc về Copy Course Content</summary>

| Mã rule     | Business Rule                                                                                                                                                         |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-COPY-001 | Admin có thể sao chép cấu phần học từ khóa học đã tồn tại trên hệ thống.                                                                                              |
| BR-COPY-002 | Khi copy cấu phần, Admin bắt buộc chọn khóa học nguồn tại trường **Select Course**.                                                                                   |
| BR-COPY-003 | Admin có thể chọn một hoặc nhiều cấu phần muốn sao chép.                                                                                                              |
| BR-COPY-004 | Khi copy Section, các cấu phần có thể copy gồm **Section, Midterm Test, Final Test**.                                                |
| BR-COPY-007 | Khi copy Activity, cấu phần có thể copy là **Activity**.                                                                                                              |
| BR-COPY-008 | Khi copy một cấu phần, toàn bộ cấu phần con của cấu phần được chọn sẽ được sao chép sang khóa học hiện tại.                                                           |
| BR-COPY-009 | Nếu Activity đã liên kết với Learning Outcome, liên kết này được giữ nguyên trong khóa học mới nếu Admin copy đồng thời cả Learning Outcome và Unit chứa Activity đó. |
| BR-COPY-010 | Với khóa học đã có học viên hoàn thành 100%, Admin chỉ được phép copy bài kiểm tra vào khóa học nếu bài kiểm tra không được tính điểm.                                |
| BR-COPY-011 | Với khóa học đã có học viên hoàn thành 100%, Admin chỉ được copy Quiz thuộc Activity nếu Quiz không được tính điểm.                                                   |

</details>

<details>

<summary>Quy tắc về Link Course Content</summary>

| Mã rule     | Business Rule                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------ |
| BR-LINK-002 | Các cấu phần có thể link gồm **Section, Activity**.                            |
| BR-LINK-003 | Link Section được thực hiện từ button **Link Section** trên màn Course Content.                  |
| BR-LINK-006 | Link Activity được thực hiện từ Action của Unit.                                                 |
| BR-LINK-007 | Admin cần tìm kiếm và chọn khóa học nguồn chứa cấu phần cần link.                                |
| BR-LINK-008 | Admin có thể chọn một hoặc nhiều học phần để link.                                               |
| BR-LINK-009 | Sau khi link thành công, học phần được link hiển thị trong Course Content với ký hiệu tương ứng. |
| BR-LINK-010 | Không được link chồng các cấu phần học.                                                          |
| BR-LINK-011 | Admin có thể gỡ link bằng chức năng **Unlink** tại Action của học phần đã link.                  |
| BR-LINK-012 | Khi chọn Unlink, hệ thống hiển thị popup xác nhận trước khi gỡ học phần khỏi khóa học.           |

</details>

<details>

<summary>Quy tắc xóa dữ liệu trong Course</summary>

| Mã rule       | Business Rule                                                                           |
| ------------- | --------------------------------------------------------------------------------------- |
| BR-DELETE-001 | Admin chỉ được xóa Course Content nếu có quyền và cấu phần thỏa mãn điều kiện xóa.      |
| BR-DELETE-002 | Không được xóa Test/Quiz/Case Study đã có học viên làm.                                 |
| BR-DELETE-003 | Không được xóa cấu phần cha nếu bên trong chứa Test/Quiz/Case Study đã có học viên làm. |
| BR-DELETE-005 | Không thể xóa Course Category đã được gán với khóa học.                   |
| BR-DELETE-006 | Admin có thể xóa tài liệu khỏi Resource của khóa học nếu có quyền.                      |
| BR-DELETE-007 | Xóa buổi học trong Learning Schedule cần xác nhận tại popup trước khi thực hiện.        |

</details>
