# Quản lý khóa học

Khóa học là đơn vị nội dung gốc của hệ thống: chứa bài học, bài kiểm tra, quiz, tài liệu và chứng chỉ. Lớp học ở [Class Management](../../class-management/tong-quan-lop-hoc-classes/) không tự chứa nội dung, lớp phải gắn vào một khóa học đã publish và học viên trong lớp học theo nội dung của khóa đó. Vì vậy khóa học phải hoàn chỉnh trước khi mở lớp.

#### Luồng tạo khóa học

Một khóa học được dựng qua 4 bước tuần tự:

1. **Tạo khóa học:** điền thông tin cơ bản bao gồm tên, mã, danh mục, loại khóa (Normal hoặc Foundation), điểm đạt và tỷ trọng điểm thành phần.
2. **Tạo nội dung khóa học:** tạo các hoạt động học và hoạt động kiểm tra bên trong khóa.
3. **Thêm tài liệu khóa học:** đính kèm tài liệu dùng chung cho khóa.
4. **Thêm chứng chỉ khóa học:** gắn mẫu chứng chỉ cấp cho học viên khi hoàn thành.

<figure><img src="../../.gitbook/assets/Create Course Workflow.png" alt="" width="563"><figcaption></figcaption></figure>

#### Trạng thái khóa học

| Trạng thái  | Ý nghĩa                                                 |
| ----------- | ------------------------------------------------------- |
| **Draft**   | Khóa học đang tạo dở, chưa publish.                     |
| **Publish** | Khóa học đã hoàn chỉnh và sẵn sàng để thêm vào lớp học. |
| **Lock**    | Khóa học đã có ít nhất một học viên bắt đầu học.        |
| **Block**   | Khóa học bị chặn, không thể thêm vào lớp học.           |

{% hint style="warning" %}
Khóa học chỉ được **Publish** khi đã tạo nội dung và gắn chứng chỉ. Khóa ở trạng thái **Draft** hoặc **Block** không thêm được vào lớp.
{% endhint %}

#### Nội dung trong mục này

* [**Danh sách khóa học**](xem-danh-sach-khoa-hoc-course-list.md): xem, tìm kiếm khóa học, trạng thái, danh mục.
* [**Tạo khóa học**](tao-khoa-hoc-course-infor.md): bước đầu tiên, tạo thông tin cơ bản, loại khóa, điểm đạt và điểm thành phần.
* [**Tạo nội dung khóa học**](tao-noi-dung-khoa-hoc-course-content/): tạo hoạt động học và hoạt động kiểm tra trong khóa.
* [**Thêm tài liệu khóa học**](tai-len-tai-lieu-cho-khoa-hoc-resource.md): đính kèm tài liệu cho khóa.
* [**Thêm chứng chỉ khóa học**](gan-chung-chi-cho-khoa-hoc-certificate.md): gắn mẫu chứng chỉ hoàn thành.

***

#### Business Rule

<details>

<summary>Quy tắc chung về Course</summary>

<table><thead><tr><th width="199.91015625">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-COURSE-01</td><td>Một khóa học sau khi tạo mặc định ở trạng thái <strong>Draft</strong>.</td></tr><tr><td>BR-COURSE-02</td><td>Cấu trúc nội dung khóa học gồm 2 cấp: <strong>Section → Activity</strong>.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc về Course Info</summary>

<table><thead><tr><th width="199.56640625">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-COURSE-INFO-01</td><td>Trường <strong>Course Category</strong> bắt buộc chọn từ danh sách danh mục có sẵn trên hệ thống.</td></tr><tr><td>BR-COURSE-INFO-02</td><td>Một khóa học chỉ được chọn một <strong>Type</strong> tại thời điểm tạo.</td></tr><tr><td>BR-COURSE-INFO-03</td><td>Hệ thống hỗ trợ 2 Type: <strong>Normal Course</strong> và <strong>Foundation Course</strong>.</td></tr><tr><td>BR-COURSE-INFO-04</td><td>Nếu Type = <strong>Normal Course</strong>, Admin có thể gắn kèm một <strong>Foundation Course</strong>; khi đó học viên phải hoàn thành khóa Foundation trước khi học khóa chính.</td></tr><tr><td>BR-COURSE-INFO-05</td><td>Với <strong>Normal Course</strong>, Admin có thể chọn hoặc không chọn Foundation Course.</td></tr><tr><td>BR-COURSE-INFO-06</td><td>Trường <strong>Pass Point</strong> là điểm yêu cầu học viên phải đạt để có thể nhận chứng chỉ của khóa học.</td></tr><tr><td>BR-COURSE-INFO-07</td><td>Tổng điểm các thành phần của khóa học phải bằng <strong>100</strong>.</td></tr><tr><td>BR-COURSE-INFO-08</td><td>Các thành phần điểm gồm: <strong>Tiến độ học, Section Test, Mid Test, Final Test</strong>.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc về loại khóa học</summary>

<table><thead><tr><th width="200.20703125">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-COURSE-TYPE-01</td><td><strong>Foundation Course</strong> là khóa học nền tảng, học viên cần hoàn thành trước khi học khóa chính.</td></tr><tr><td>BR-COURSE-TYPE-02</td><td><strong>Normal Course</strong> là khóa học thường, có thể yêu cầu học viên hoàn thành một số Foundation Course trước khi học.</td></tr><tr><td>BR-COURSE-TYPE-03</td><td>Khi Block một <strong>Foundation Course</strong> đã được gắn với Normal Course, hệ thống cảnh báo rằng khóa Foundation sẽ bị unlink khỏi các khóa Normal liên quan.</td></tr><tr><td>BR-COURSE-TYPE-04</td><td>Khi Block khóa <strong>Normal Course</strong>, hệ thống cảnh báo rằng khóa học sẽ bị remove khỏi các lớp chưa bắt đầu.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc về Course Content</summary>

<table><thead><tr><th width="200.0546875">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-CONTENT-01</td><td>Tạo <strong>Section</strong> trước khi tạo <strong>Activity</strong>.</td></tr><tr><td>BR-CONTENT-02</td><td><strong>Learning Outcome</strong> được tạo ở cấp <strong>Section</strong>.</td></tr><tr><td>BR-CONTENT-03</td><td>Một Section có thể có một hoặc nhiều Learning Outcome.</td></tr><tr><td>BR-CONTENT-04</td><td>Một Activity có thể được gắn với một hoặc nhiều Learning Outcome đã tạo trong Section chứa Activity đó.</td></tr><tr><td>BR-CONTENT-05</td><td>Các mã <strong>Section Code</strong> và <strong>Activity Code</strong> được hệ thống tạo tự động theo rule của khóa học.</td></tr><tr><td>BR-CONTENT-06</td><td><strong>Type of Activity</strong> dùng để hiển thị icon trên giao diện học viên UpLMS.</td></tr><tr><td>BR-CONTENT-07</td><td>Type of Activity gồm: <strong>Text, Video, Quiz</strong>.</td></tr><tr><td>BR-CONTENT-08</td><td>Activity có thể đính kèm một hoặc nhiều Resource.</td></tr><tr><td>BR-CONTENT-09</td><td>Khóa học chỉ được Publish khi đã được tạo nội dung và gán chứng chỉ.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc về Activity và Document</summary>

<table><thead><tr><th width="199.94140625">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-ACTIVITY-01</td><td>Activity phải thuộc một Section đã tồn tại.</td></tr><tr><td>BR-ACTIVITY-02</td><td>Một Activity có thể có một hoặc nhiều Tab.</td></tr><tr><td>BR-ACTIVITY-03</td><td>Mỗi Tab có thể có một hoặc nhiều Document.</td></tr><tr><td>BR-ACTIVITY-04</td><td>Document trong Activity gồm 3 loại: <strong>Text, Video, Quiz</strong>.</td></tr><tr><td>BR-ACTIVITY-05</td><td>Với Document dạng Text, nội dung có thể chưa cả định dạng ảnh</td></tr><tr><td>BR-ACTIVITY-06</td><td>Timeline được sắp xếp theo thứ tự thời gian của video.</td></tr><tr><td>BR-ACTIVITY-07</td><td>Câu hỏi trong Video được sắp xếp theo thứ tự thời gian của video.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc về Add Question trong Test/ Quiz</summary>

<table><thead><tr><th width="199.640625">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-QUESTION-01</td><td>Câu hỏi thêm vào Test/ Quiz được lấy từ Question Bank.</td></tr><tr><td>BR-QUESTION-02</td><td>Danh sách câu hỏi hiển thị phụ thuộc vào Type of Test.</td></tr><tr><td>BR-QUESTION-03</td><td>Nếu chọn đơn lẻ từng câu hỏi, câu nào được chọn trước sẽ đứng trước.</td></tr><tr><td>BR-QUESTION-04</td><td>Nếu chọn toàn bộ câu hỏi trong trang, thứ tự câu hỏi giữ nguyên như thứ tự đang hiển thị tại màn Add Question.</td></tr><tr><td>BR-QUESTION-05</td><td>Nếu chọn một câu hỏi, sau đó bỏ chọn và chọn lại, câu hỏi đó được đưa xuống cuối danh sách.</td></tr><tr><td>BR-QUESTION-06</td><td>Thứ tự câu hỏi tại Setup Score và Reorder phụ thuộc vào thứ tự chọn câu hỏi tại Add Question.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc về Reorder câu hỏi</summary>

<table><thead><tr><th width="199.66015625">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-REORDER-01</td><td>Số thứ tự phản ánh thứ tự thực tế của câu hỏi trong bài Test/ Quiz.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc chỉnh sửa khóa học</summary>

<table><thead><tr><th width="199.64453125">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-EDIT-01</td><td>Nếu lớp chưa có học viên hoặc có học viên nhưng học viên chưa học, được sửa tất cả thông tin khóa học.</td></tr><tr><td>BR-EDIT-02</td><td>Nếu đã có học viên học nhưng chưa có học viên nào học xong, Course Info vẫn được sửa tất cả thông tin.</td></tr><tr><td>BR-EDIT-03</td><td>Nếu đã có học viên học nhưng chưa học xong, được sửa/ xóa Section, Activity, Tab dạng Text hoặc Video nếu không chứa Test/ Quiz/ Case Study đã có người làm.</td></tr><tr><td>BR-EDIT-04</td><td>Nếu đã có học viên học nhưng chưa học xong, được phép kéo thả cấu phần học.</td></tr><tr><td>BR-EDIT-05</td><td>Nếu đã có học viên học nhưng chưa học xong, được thêm cấu phần học và bài Test.</td></tr><tr><td>BR-EDIT-06</td><td>Với Test/ Quiz/ Case Study đã có người làm, không được xóa bài Test/ Quiz/ Case study và không được xóa cấu phần chứa các bài này.</td></tr><tr><td>BR-EDIT-07</td><td>Với Test/Quiz đã có người làm, Admin không được chỉnh sửa Type of Test, Test Mode, Graded Assignment, Grading Preference, Pass Point, Attempt.</td></tr><tr><td>BR-EDIT-08</td><td>Với Test/ Quiz đã có người làm, danh sách câu hỏi chỉ được xem, không được thêm/xóa/chỉnh sửa tại bước Add Question.</td></tr><tr><td>BR-EDIT-09</td><td>Với Test/Quiz chưa có người làm, được sửa toàn bộ Setting, thêm câu hỏi, xóa câu hỏi và xóa bài test.</td></tr><tr><td>BR-EDIT-10</td><td>Nếu đã có học viên học xong, được thêm cấu phần học nhưng không được thêm Test/Quiz/Case Study.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc về cập nhật cấu phần học mới cho học viên</summary>

<table><thead><tr><th width="199.83984375">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-STUDENT-CONTENT-01</td><td>Khi khóa học đã có học viên học, cấu phần học mới thêm không tự động hiển thị ngay cho học viên.</td></tr><tr><td>BR-STUDENT-CONTENT-02</td><td>Để học viên nhìn thấy cấu phần mới, cần cập nhật Course Content cho lớp hoặc cho từng học viên.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc về Copy Course Content</summary>

<table><thead><tr><th width="200.12109375">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-COPY-01</td><td>Nếu Activity đã gắn với Learning Outcome, liên kết này được giữ nguyên trong khóa học mới nếu Copy đồng thời cả Learning Outcome và Section chứa Activity đó.</td></tr><tr><td>BR-COPY-02</td><td>Với khóa học đã có học viên hoàn thành 100%, chỉ được phép Copy bài kiểm tra vào khóa học nếu bài kiểm tra không được tính điểm.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc xóa dữ liệu trong Course</summary>

<table><thead><tr><th width="199.66015625">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-DELETE-01</td><td>Không được xóa Test/Quiz/Case Study đã có học viên làm.</td></tr><tr><td>BR-DELETE-02</td><td>Không được xóa cấu phần cha nếu bên trong chứa Test/ Quiz/ Case Study đã có học viên làm.</td></tr><tr><td>BR-DELETE-03</td><td>Không thể xóa Course Category đã được gán với khóa học.</td></tr></tbody></table>

</details>
