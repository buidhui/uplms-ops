---
description: Lớp học là nơi gắn khóa học với người học cụ thể và vận hành việc học hàng ngày.
---

# Tổng quan lớp học (Classes)

#### Module này dùng để làm gì?

Nếu Academic Management là nơi xây dựng "nội dung cần dạy", thì Class Management là nơi quyết định "ai học, học nội dung nào và trong thời gian nào".

Lớp học không tự chứa nội dung. Mỗi lớp gắn với một khóa học đã publish, và học viên trong lớp học theo nội dung của khóa đó. Những gì thuộc về lớp là: danh sách học viên, trợ giảng phụ trách, tài liệu riêng của lớp, thời hạn truy cập, và kết quả bài kiểm tra của từng học viên.

***

#### Vòng đời một lớp học

<figure><img src="../.gitbook/assets/image (857).png" alt=""><figcaption></figcaption></figure>

1. **Tạo lớp** — đặt tên và mã lớp, chọn hình thức và loại lớp, đặt số học viên tối đa và thời hạn, rồi gắn khóa học.
2. **Đưa người vào lớp** — thêm học viên (thủ công hoặc import) và thêm trợ giảng phụ trách.
3. **Vận hành trong lúc học** — thêm tài liệu cho lớp, điều chỉnh thời hạn hoặc cấu phần học cho từng học viên, theo dõi bài kiểm tra.

***

#### Loại lớp và thời hạn

Người dùng chỉ tạo thủ công được lớp **Lesson**. Lớp **Foundation** do hệ thống tự tạo khi khóa Normal gắn với lớp Lesson có cấu hình Foundation Course.

| Duration     | Cách tính thời hạn                                                        |
| ------------ | ------------------------------------------------------------------------- |
| **Fixed**    | Lớp diễn ra trong khoảng Start Date – End Date đã đặt.                    |
| **Flexible** | Lớp diễn ra trong N ngày, tính từ ngày học viên chọn bắt đầu khóa học.    |

{% hint style="info" %}
Thao tác thêm hoặc xóa học viên và trợ giảng ở lớp **Lesson** sẽ đồng bộ sang lớp **Foundation** gắn kèm. Ngược lại thì không: thao tác tại lớp Foundation không ảnh hưởng lớp Lesson.
{% endhint %}

***

#### Nội dung trong mục này

* [**Danh sách và Chi tiết lớp học**](xem-danh-sach-va-thong-tin-chi-tiet-lop-hoc/README.md): tìm lớp, xem thông tin lớp và các tab bên trong — gồm cả [quản lý bài kiểm tra trong lớp](xem-danh-sach-va-thong-tin-chi-tiet-lop-hoc/quan-ly-bai-kiem-tra-trong-lop-test-quiz.md).
* [**Tạo lớp học**](tao-lop-hoc.md): tạo từng lớp, tạo hàng loạt bằng import, và quy tắc chỉnh sửa lớp đã tạo.
* [**Quản lý học viên trong lớp**](quan-ly-hoc-vien-trong-lop.md): thêm, import, xóa học viên; điều chỉnh thời hạn và cấu phần học cho từng người.
* [**Quản lý trợ giảng trong lớp**](quan-ly-tro-giang-trong-lop.md): thêm, xóa trợ giảng và chọn trợ giảng chính.
* [**Quản lý tài liệu lớp học**](quan-ly-tai-lieu-lop-hoc.md): thư mục và tài liệu riêng của lớp, quyền xem và quyền tải.

***

### Business Rule

<details>

<summary>Quy tắc chung về Class</summary>

| Mã rule      | Business Rule                                                                                                                                                                  |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| BR-CLASS-001 | Người dùng chỉ được truy cập module **Class** khi đã đăng nhập thành công vào hệ thống UpLMS Operations.                                                                       |
| BR-CLASS-002 | Người dùng chỉ được xem danh sách lớp học nếu tài khoản có quyền truy cập màn hình **Class List**.                                                                             |
| BR-CLASS-003 | Người dùng chỉ được tạo, chỉnh sửa, import hoặc thao tác với lớp học nếu có quyền tương ứng.                                                                                   |
| BR-CLASS-004 | Danh sách lớp học mặc định được hiển thị theo **thời gian tạo giảm dần**.                                                                                                      |
| BR-CLASS-005 | Người dùng có thể tìm kiếm/lọc lớp học theo tên/mã lớp, Code, Status, Construction Mode, Type, Sort by và khoảng thời gian. |
| BR-CLASS-006 | Nút **Reset** chỉ xóa điều kiện tìm kiếm/lọc, không xóa dữ liệu lớp học.                                                                                                       |
| BR-CLASS-007 | Người dùng có thể xem chi tiết lớp học bằng cách nhấp vào **tên lớp học** tại màn hình Class List.                                                                             |
| BR-CLASS-008 | Màn hình chi tiết lớp học gồm 6 tab: **Overview, Students, Mentors, Grading, Test/Quiz, Resources**.                     |

</details>

<details>

<summary>Quy tắc tạo lớp học</summary>

| Mã rule       | Business Rule                                                                                                                                           |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-CREATE-001 | Người dùng chỉ được tạo lớp học nếu có quyền **Create Class**.                                                                                          |
| BR-CREATE-002 | Các trường bắt buộc khi tạo lớp bao gồm: **Name, Code, Construction Mode, Type, Số học viên tối đa** và các trường điều kiện khác tùy loại lớp.         |
| BR-CREATE-003 | **Code** của lớp phải là duy nhất trên hệ thống.                                                                                                        |
| BR-CREATE-004 | Mã lớp học cần có ký tự **“.”**.                                                                                                     |
| BR-CREATE-005 | Người dùng chỉ có thể tạo thủ công lớp có Type là **Lesson**.                                                          |
| BR-CREATE-006 | Lớp **Foundation** không tạo thủ công; hệ thống tự động tạo khi lớp Lesson gắn với Normal Course có cấu hình Foundation Course.                         |
| BR-CREATE-012 | Sau khi tạo lớp thành công, lớp được hiển thị tại màn hình **Class List**.                                                                              |

</details>

<details>

<summary>Quy tắc Type của lớp học</summary>

| Mã rule     | Business Rule                                                                       |
| ----------- | ----------------------------------------------------------------------------------- |
| BR-TYPE-001 | **Lesson** là lớp học chính.                                                        |
| BR-TYPE-004 | **Foundation** là lớp nền tảng được hệ thống tự động tạo, không tạo thủ công.       |
| BR-TYPE-005 | Khi chọn Course cho lớp **Lesson**, hệ thống chỉ hiển thị **Normal Course**.        |

</details>

<details>

<summary>Quy tắc Duration</summary>

| Mã rule         | Business Rule                                                                                                                      |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| BR-DURATION-002 | Duration có 2 kiểu: **Fixed** và **Flexible**.                                                                                     |
| BR-DURATION-003 | Với Duration = **Fixed**, thời hạn lớp được xác định theo Start Date - End Date.                                                   |
| BR-DURATION-004 | Với Duration = **Flexible**, thời hạn học của học viên phụ thuộc vào ngày học viên kích hoạt khóa học.                             |

</details>

<details>

<summary>Quy tắc chỉnh sửa thông tin lớp học</summary>

| Mã rule     | Business Rule                                                                                                                                                                                                                                     |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-EDIT-001 | Người dùng chỉ được chỉnh sửa lớp nếu có quyền **Edit Class**.                                                                                                                                                                                    |
| BR-EDIT-002 | Lớp có trạng thái **Ended** không được chỉnh sửa.                                                                                                                                                                                                 |
| BR-EDIT-003 | Việc chỉnh sửa lớp phụ thuộc vào **Type** và tiến độ học của học viên trong lớp.                                                                                                                                           |
| BR-EDIT-006 | Với lớp **Foundation** đã có học viên học, chỉ được chỉnh sửa Name, Code và Số học viên tối đa.                                                                                                              |
| BR-EDIT-007 | Với lớp **Foundation** chưa có học viên học, được chỉnh sửa tất cả thông tin, ngoại trừ Type và Course.                                                                                                                    |
| BR-EDIT-008 | Với lớp **Lesson** chưa có học viên học, người dùng được chỉnh sửa tất cả thông tin.                                                                                                                                                   |
| BR-EDIT-009 | Với lớp **Lesson** đã có học viên nhưng lớp chưa bắt đầu hoặc học viên chưa học, không được chỉnh sửa Status, Construction Mode, Type và Course.                                                                       |
| BR-EDIT-010 | Với lớp **Lesson** đã có học viên đang học hoặc lớp đã bắt đầu, không được chỉnh sửa Status, Construction Mode, Type và Course. |

</details>

<details>

<summary>Quy tắc Import Class</summary>

| Mã rule       | Business Rule                                                                      |
| ------------- | ---------------------------------------------------------------------------------- |
| BR-IMPORT-001 | Người dùng chỉ được import lớp học nếu có quyền **Import Class**.                  |
| BR-IMPORT-002 | Chức năng Import Class dùng để tạo nhiều lớp học cùng lúc.                         |
| BR-IMPORT-003 | File import chỉ chấp nhận định dạng **.csv** hoặc **.xlsx**.                       |
| BR-IMPORT-004 | Mỗi lần import chỉ được chọn **01 file**.                                          |
| BR-IMPORT-005 | Người dùng nên tải file mẫu từ hệ thống trước khi nhập dữ liệu import.             |
| BR-IMPORT-006 | Dữ liệu trong file import cần tuân thủ đúng template và rule tạo lớp học.          |
| BR-IMPORT-007 | Các dòng hợp lệ trong file sẽ được tạo lớp thành công.                             |
| BR-IMPORT-008 | Các dòng không hợp lệ sẽ không được tạo lớp và được ghi nhận tại log import.       |
| BR-IMPORT-009 | Sau khi import, hệ thống hiển thị kết quả gồm Source, Data, Successfully và Error. |
| BR-IMPORT-010 | Người dùng có thể chọn **View Log** để xem chi tiết lỗi từng dòng.                 |
| BR-IMPORT-011 | Các trường không hợp lệ trong file import được bôi đỏ tại màn hình Import Detail.  |
| BR-IMPORT-012 | Lý do lỗi được hiển thị tại cột **Errors**.                                        |

</details>

<details>

<summary>Quy tắc quản lý học viên trong lớp</summary>

| Mã rule        | Business Rule                                                                                                                       |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| BR-STUDENT-002 | Người dùng có thể thêm học viên thủ công bằng chức năng **Add Student** nếu có quyền.                                               |
| BR-STUDENT-003 | Người dùng có thể import học viên bằng file nếu có quyền.                                                                           |
| BR-STUDENT-004 | File import học viên chỉ chấp nhận định dạng **.csv** hoặc **.xlsx**.                                                               |
| BR-STUDENT-005 | Mỗi lần import học viên chỉ được chọn **01 file**.                                                                                  |
| BR-STUDENT-007 | Khi thêm học viên vào lớp **Lesson**, học viên đó cũng được thêm vào lớp **Foundation** gắn với lớp ban đầu.        |
| BR-STUDENT-008 | Khi xóa học viên khỏi lớp **Lesson**, học viên đó cũng được xóa khỏi lớp **Foundation** gắn với lớp ban đầu.        |
| BR-STUDENT-009 | Khi thêm hoặc xóa học viên khỏi lớp **Foundation**, thao tác này không ảnh hưởng đến học viên của lớp **Lesson**. |
| BR-STUDENT-010 | Người dùng có thể xóa một học viên hoặc nhiều học viên khỏi lớp nếu có quyền.                                                       |
| BR-STUDENT-011 | Khi xóa học viên, hệ thống hiển thị popup xác nhận trước khi thực hiện.                                                             |
| BR-STUDENT-012 | Với lớp có Duration = Flexible, nếu học viên chưa kích hoạt khóa học thì không thể cập nhật thời hạn học của học viên đó.           |
| BR-STUDENT-013 | Thời hạn học riêng của học viên có thể dài hơn hoặc ngắn hơn thời hạn mặc định của lớp.                                             |
| BR-STUDENT-014 | Người dùng có thể chỉnh sửa Course Content riêng cho từng học viên.                                                                 |
| BR-STUDENT-015 | Việc chỉnh sửa Course Content riêng chỉ áp dụng cho học viên được chọn, không ảnh hưởng toàn bộ lớp.                                |
| BR-STUDENT-016 | Người dùng luôn được thêm mới cấu phần học cho học viên.                                                                            |
| BR-STUDENT-017 | Người dùng chỉ được xóa cấu phần học khỏi chương trình học của học viên nếu học viên chưa học cấu phần đó.                          |
| BR-STUDENT-018 | Nếu học viên đã học cấu phần đó, hệ thống không cho phép xóa cấu phần khỏi chương trình học của học viên.                           |
| BR-STUDENT-019 | Chức năng **Allow Pass Foundation** chỉ áp dụng khi lớp Lesson có gắn lớp Foundation.                                               |
| BR-STUDENT-020 | Allow Pass Foundation dùng để đánh dấu học viên hoàn thành khóa Foundation và cho phép học viên chuyển sang học khóa chính.         |

</details>

<details>

<summary>Quy tắc chọn/bỏ chọn cấu phần học của học viên</summary>

| Mã rule                | Business Rule                                                                                              |
| ---------------------- | ---------------------------------------------------------------------------------------------------------- |
| BR-STUDENT-CONTENT-001 | Khi chọn/bỏ chọn **All**, tất cả checkbox cấu phần học được tick hoặc bỏ tick.                             |
| BR-STUDENT-CONTENT-002 | Khi chọn **Section**, tất cả Activity, Test và Quiz thuộc Section được chọn.                   |
| BR-STUDENT-CONTENT-005 | Khi chọn **Activity**, Section chứa Activity đó được chọn.                             |
| BR-STUDENT-CONTENT-006 | Cấu phần bị bỏ chọn sẽ không xuất hiện trong chương trình học của học viên.                                |
| BR-STUDENT-CONTENT-007 | Học viên không cần học các cấu phần đã bị bỏ chọn khỏi chương trình học cá nhân.                           |
| BR-STUDENT-CONTENT-008 | Không được xóa cấu phần học viên đã học.                                                                   |
| BR-STUDENT-CONTENT-009 | Được phép xóa cấu phần học viên chưa học.                                                                  |

</details>

<details>

<summary>Quy tắc quản lý trợ giảng trong lớp</summary>

| Mã rule       | Business Rule                                                                                                           |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| BR-MENTOR-001 | Người dùng chỉ được thêm/xóa trợ giảng nếu có quyền quản lý Mentor trong lớp.                                           |
| BR-MENTOR-002 | Danh sách trợ giảng được lấy từ **Staff List** trên hệ thống.                                                           |
| BR-MENTOR-003 | Người dùng có thể thêm một hoặc nhiều trợ giảng vào lớp.                                                                |
| BR-MENTOR-004 | Người dùng có thể xóa một trợ giảng hoặc nhiều trợ giảng cùng lúc.                                                      |
| BR-MENTOR-005 | Khi xóa trợ giảng, hệ thống hiển thị popup xác nhận trước khi thực hiện.                                                |
| BR-MENTOR-006 | Trợ giảng được chọn tại cột **Main Responsible** được hiểu là trợ giảng chính của lớp.                                  |
| BR-MENTOR-007 | Main Responsible là trợ giảng chịu trách nhiệm chính về chấm điểm của lớp.               |
| BR-MENTOR-008 | Nếu lớp Lesson có gắn Foundation, khi thêm trợ giảng vào lớp Lesson thì trợ giảng đó cũng được thêm vào lớp Foundation. |
| BR-MENTOR-009 | Nếu lớp Lesson có gắn Foundation, khi xóa trợ giảng khỏi lớp Lesson thì trợ giảng đó cũng bị xóa khỏi lớp Foundation.   |
| BR-MENTOR-010 | Thao tác thêm/xóa trợ giảng tại lớp không gắn Foundation chỉ áp dụng cho lớp đang thao tác.                             |

</details>

<details>

<summary>Quy tắc quản lý bài kiểm tra trong lớp</summary>

| Mã rule     | Business Rule                                                                                                  |
| ----------- | -------------------------------------------------------------------------------------------------------------- |
| BR-TEST-001 | Tab **Test/Quiz** hiển thị danh sách bài kiểm tra thuộc Course đã gắn với lớp.                                 |
| BR-TEST-002 | Nếu Course chưa có bài kiểm tra trong Course Content, tab Test/Quiz không hiển thị dữ liệu bài kiểm tra.       |
| BR-TEST-003 | Người dùng có thể tìm kiếm/lọc bài kiểm tra theo tên bài kiểm tra, loại bài kiểm tra và Manual Grading.        |
| BR-TEST-004 | Người dùng có thể xem chi tiết bài kiểm tra bằng cách nhấp vào tên bài kiểm tra hoặc chọn **Action → Detail**. |
| BR-TEST-005 | Màn hình chi tiết bài kiểm tra hiển thị danh sách học viên được làm bài kiểm tra đó.                           |
| BR-TEST-006 | Thời gian truy cập bài kiểm tra có thể được cài đặt cho toàn bộ học viên hoặc cho từng học viên.               |
| BR-TEST-007 | Thời gian truy cập riêng của từng học viên chỉ áp dụng cho học viên đó.                                        |
| BR-TEST-008 | Khi xóa Access Time của bài kiểm tra, hệ thống hiển thị popup xác nhận trước khi thực hiện.                    |
| BR-TEST-009 | Người dùng có thể xuất kết quả bài kiểm tra ra file Excel bằng chức năng **Export Result**.                    |
| BR-TEST-010 | File Export Result được đặt tên theo cú pháp **\[Mã lớp]\_\[Tên bài kiểm tra]**.                               |
| BR-TEST-011 | Nếu học viên chưa nộp bài, thông tin điểm trong file Excel hiển thị rỗng.                                      |
| BR-TEST-012 | Nếu bài kiểm tra chấm thủ công chưa chấm xong, thông tin điểm trong file Excel hiển thị rỗng.                  |

</details>

<details>

<summary>Quy tắc trạng thái bài làm Test/Quiz</summary>

| Mã rule            | Business Rule                                                                                                       |
| ------------------ | ------------------------------------------------------------------------------------------------------------------- |
| BR-TEST-STATUS-001 | Với bài kiểm tra hệ thống chấm tự động, trạng thái bài làm gồm **Unsubmitted** và **Submitted**.                    |
| BR-TEST-STATUS-002 | **Unsubmitted** nghĩa là học viên chưa nộp bài.                                                                     |
| BR-TEST-STATUS-003 | **Submitted** nghĩa là học viên đã hoàn thành bài kiểm tra.                                                         |
| BR-TEST-STATUS-004 | Với bài kiểm tra chấm thủ công, trạng thái bài làm gồm **Unsubmitted**, **Awaiting Grading** và **Finish Grading**. |
| BR-TEST-STATUS-005 | **Awaiting Grading** nghĩa là học viên đã nộp bài và đang chờ chấm.                                                 |
| BR-TEST-STATUS-006 | **Finish Grading** nghĩa là bài làm của học viên đã được chấm xong.                                                 |

</details>

<details>

<summary>Quy tắc Access Time của Test/Quiz</summary>

| Mã rule       | Business Rule                                                                                                                                    |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| BR-ACCESS-001 | Start date của Access Time phải lớn hơn hoặc bằng **Start Date** của Class.                                                                    |
| BR-ACCESS-002 | End date của Access Time phải nhỏ hơn hoặc bằng **End Date** của Class.                                                                          |
| BR-ACCESS-003 | Nếu Start Date của Class thay đổi và Start Date mới lớn hơn Start date của Access Time, Access Time được cập nhật theo Start Date của lớp. |
| BR-ACCESS-004 | Nếu End Date của Class thay đổi và End Date mới nhỏ hơn End Date của Access Time, Access Time được cập nhật theo End Date của lớp.               |
| BR-ACCESS-005 | Học viên chỉ truy cập được bài kiểm tra trong khoảng thời gian Access Time được cấu hình.                                                        |
| BR-ACCESS-006 | Nếu chưa đến thời gian mở hoặc đã quá thời hạn nộp, học viên không thể truy cập bài kiểm tra.                                                    |

</details>

<details>

<summary>Quy tắc trạng thái và kết thúc lớp</summary>

| Mã rule       | Business Rule                                                                                         |
| ------------- | ----------------------------------------------------------------------------------------------------- |
| BR-STATUS-001 | Lớp có trạng thái **Ended** không được chỉnh sửa.                                                     |
| BR-STATUS-002 | Một số thao tác với lớp phụ thuộc vào trạng thái lớp và việc học viên đã học hay chưa.                |
| BR-STATUS-004 | Lớp Foundation có nhiều thông tin đồng bộ từ lớp Lesson nên bị giới hạn chỉnh sửa trực tiếp. |

</details>

<details>

<summary>Quy tắc dữ liệu đồng bộ giữa các lớp liên quan</summary>

| Mã rule     | Business Rule                                                                                            |
| ----------- | -------------------------------------------------------------------------------------------------------- |
| BR-SYNC-002 | Lớp Foundation được tạo và đồng bộ theo logic từ lớp Lesson gắn Normal Course có Foundation Course.      |
| BR-SYNC-003 | Khi thêm/xóa học viên ở lớp Lesson, hệ thống đồng bộ học viên sang lớp Foundation liên quan. |
| BR-SYNC-004 | Khi thêm/xóa học viên ở lớp Foundation, hệ thống không đồng bộ ngược về lớp Lesson.        |
| BR-SYNC-005 | Khi thêm/xóa Mentor ở lớp Lesson có gắn Foundation, hệ thống đồng bộ Mentor sang lớp Foundation.         |
| BR-SYNC-006 | Khi thao tác Mentor tại lớp không gắn Foundation, hệ thống chỉ áp dụng cho lớp đang thao tác.            |

</details>
