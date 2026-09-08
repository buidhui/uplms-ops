# Quản lý lớp học

Nếu Academic Management là nơi xây dựng "nội dung cần dạy", thì Class Management là nơi quyết định "ai học, học nội dung nào và trong thời gian nào".

Lớp học không tự chứa nội dung. Mỗi lớp gắn với một khóa học đã publish, và học viên trong lớp học theo nội dung của khóa đó. Những gì thuộc về lớp là: danh sách học viên, trợ giảng phụ trách, tài liệu riêng của lớp, thời hạn truy cập, và kết quả bài kiểm tra của từng học viên.

***

#### Vòng đời một lớp học

<figure><img src="../.gitbook/assets/Create Class Flow.png" alt="" width="563"><figcaption></figcaption></figure>

1. **Tạo lớp:** đặt tên và mã lớp, chọn hình thức và loại lớp, đặt số học viên tối đa và thời hạn, rồi gắn khóa học.
2. **Thêm học viên:** thêm học viên (thủ công hoặc import) và thêm trợ giảng phụ trách.
3. **Vận hành lớp:** thêm tài liệu, điều chỉnh thời hạn hoặc cấu phần học cho từng học viên, theo dõi và chấm bài kiểm tra.

***

#### Loại lớp và thời hạn

Người dùng chỉ tạo thủ công được lớp **Lesson**. Lớp **Foundation** do hệ thống tự tạo khi khóa Normal gắn với lớp Lesson có cấu hình Foundation Course.

| Duration     | Cách tính thời hạn                                                     |
| ------------ | ---------------------------------------------------------------------- |
| **Fixed**    | Lớp diễn ra trong khoảng Start Date – End Date đã đặt.                 |
| **Flexible** | Lớp diễn ra trong N ngày, tính từ ngày học viên chọn bắt đầu khóa học. |

{% hint style="info" %}
Thao tác thêm hoặc xóa học viên và trợ giảng ở lớp **Lesson** sẽ đồng bộ sang lớp **Foundation** gắn kèm. Ngược lại thao tác tại lớp Foundation không ảnh hưởng lớp Lesson.
{% endhint %}

***

#### Nội dung trong mục này

* [**Danh sách và Chi tiết lớp học**](xem-danh-sach-va-thong-tin-chi-tiet-lop-hoc/):
* [**Tạo lớp học**](tao-lop-hoc.md): tạo từng lớp, tạo hàng loạt bằng import, và quy tắc chỉnh sửa lớp đã tạo.
* [**Quản lý học viên trong lớp**](quan-ly-hoc-vien-trong-lop.md): thêm, import, xóa học viên, điều chỉnh thời hạn và cấu phần học cho từng người.
* [**Quản lý trợ giảng trong lớp**](quan-ly-tro-giang-trong-lop.md): thêm, xóa trợ giảng và chọn trợ giảng chính.
* [**Quản lý tài liệu lớp học**](quan-ly-tai-lieu-lop-hoc.md): thư mục và tài liệu riêng của lớp, quyền với tài liệu.

***

#### Business Rule

<details>

<summary>Quy tắc Type của lớp học</summary>

<table><thead><tr><th width="200.0625">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-TYPE-001</td><td>Khi chọn Course cho lớp <strong>Lesson</strong>, hệ thống chỉ hiển thị <strong>Normal Course</strong>.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc quản lý trợ giảng trong lớp</summary>

<table><thead><tr><th width="200.1015625">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-MENTOR-01</td><td>Main Responsible là trợ giảng chịu trách nhiệm chính về chấm điểm của lớp. Người review cuối cùng trước khi gửi kết quả chấm cho học viên.</td></tr><tr><td>BR-MENTOR-02</td><td>Nếu lớp Lesson có gắn Foundation, khi thêm trợ giảng vào lớp Lesson thì trợ giảng đó cũng được thêm vào lớp Foundation.</td></tr><tr><td>BR-MENTOR-03</td><td>Nếu lớp Lesson có gắn Foundation, khi xóa trợ giảng khỏi lớp Lesson thì trợ giảng đó cũng bị xóa khỏi lớp Foundation.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc quản lý bài kiểm tra trong lớp</summary>

<table><thead><tr><th width="299.921875">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-TEST-01</td><td>Nếu bài kiểm tra chấm thủ công chưa chấm xong, thông tin điểm trong file export hiển thị rỗng.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc trạng tháiTest/Quiz</summary>

<table><thead><tr><th width="199.55859375">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-TEST-STATUS-01</td><td>Với bài kiểm tra hệ thống chấm tự động, trạng thái bài làm gồm <strong>Unsubmitted</strong> và <strong>Submitted</strong>.<br>- <strong>Unsubmitted</strong> nghĩa là học viên chưa nộp bài.<br>- <strong>Submitted</strong> nghĩa là học viên đã hoàn thành bài kiểm tra.</td></tr><tr><td>BR-TEST-STATUS-02</td><td>Với bài kiểm tra chấm thủ công, trạng thái bài làm gồm <strong>Unsubmitted</strong>, <strong>Awaiting Grading</strong> và <strong>Finish Grading</strong>.<br>- <strong>Awaiting Grading</strong> nghĩa là học viên đã nộp bài và đang chờ chấm.<br>- <strong>Finish Grading</strong> nghĩa là bài làm của học viên đã được chấm xong.</td></tr></tbody></table>

</details>

<details>

<summary>Quy tắc trạng thái và kết thúc lớp</summary>

<table><thead><tr><th width="200.46875">Mã rule</th><th>Business Rule</th></tr></thead><tbody><tr><td>BR-STATUS-01</td><td>Thời hạn mặc định của lớp Foundation là 60 ngày.</td></tr></tbody></table>

</details>
