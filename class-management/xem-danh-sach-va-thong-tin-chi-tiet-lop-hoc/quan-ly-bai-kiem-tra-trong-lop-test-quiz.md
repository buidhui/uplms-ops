---
hidden: true
---

# Quản lý bài kiểm tra trong lớp (Test/Quiz)

## Record of changes

_A - Add | M - Modify | D - Delete_

| Effective Date | Update Person | A,M,D | Change Description                                    | Version |
| -------------- | ------------- | ----- | ----------------------------------------------------- | ------- |
| May 25, 2026   | Lê Xuân Mai   | M     | Chuẩn hóa nội dung lên GitBook                        | 4.7.0   |
| Jun 18, 2026   | Nhà BA        | M     | Chuẩn hóa component theo template User guide mới nhất | 4.8.0   |

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** Admin, UpLMS Operator

**Đường dẫn:** LMS → Class List → Chọn lớp học → Test/Quiz
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Class
* **Chức năng chính:** Test/Quiz
* **Module liên quan:** Class Detail, Course, Course Content, Student, Manual Grading, Marks/Result Export
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Người dùng đã đăng nhập thành công vào hệ thống **UpLMS Operations**.
* Tài khoản có quyền truy cập module **Class** và quyền xem chi tiết lớp học.
* Khóa học đã được gắn vào lớp.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Xem danh sách bài kiểm tra trong lớp</summary>

{% stepper %}
{% step %}
**Mở màn hình Class Detail**

Người dùng nhấp vào **tên lớp học** tại màn hình **Class List**. Hệ thống mở màn hình **Class Detail**.
{% endstep %}

{% step %}
**Chọn tab Test/Quiz**

Người dùng chọn tab **Test/Quiz** tại màn hình **Class Detail**. Hệ thống hiển thị danh sách bài kiểm tra thuộc khóa học đang gắn với lớp.

<figure><img src="../../.gitbook/assets/image (247)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xem thông tin bài kiểm tra**

Người dùng xem thông tin tại bảng danh sách **Test/Quiz**:

<table data-search="false"><thead><tr><th>Cột thông tin</th><th>Mô tả</th></tr></thead><tbody><tr><td><strong>Quiz Name</strong></td><td>Tên bài kiểm tra.</td></tr><tr><td><strong>Quiz Type</strong></td><td>Loại bài kiểm tra.</td></tr><tr><td><strong>Mode</strong></td><td>Hình thức kiểm tra (online hoặc offline).</td></tr><tr><td><strong>Start Time</strong></td><td>Thời điểm học viên bắt đầu có thể truy cập và làm bài.</td></tr><tr><td><strong>End Time</strong></td><td>Thời điểm đóng bài; sau thời điểm này học viên không thể truy cập bài kiểm tra.</td></tr><tr><td><strong>Total attempts</strong></td><td>Số lượng học viên tham gia bài kiểm tra.</td></tr><tr><td><strong>Manual Grading</strong></td><td>Hình thức chấm bài: hệ thống tự động chấm hoặc đội ngũ UpBase chấm thủ công.</td></tr><tr><td><strong>Graded attempt</strong></td><td>Số bài đã được chấm xong trên tổng số bài học viên đã nộp.</td></tr><tr><td><strong>Action</strong></td><td>Menu thao tác: Detail, Edit Access Time, Delete Access Time, Export Result.</td></tr></tbody></table>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tìm kiếm/lọc bài kiểm tra</summary>

{% stepper %}
{% step %}
**Nhập/chọn điều kiện tìm kiếm**

Người dùng nhập hoặc chọn điều kiện tại vùng bộ lọc của tab **Test/Quiz** (tên bài kiểm tra, loại bài kiểm tra, hình thức chấm bài).

<figure><img src="../../.gitbook/assets/image (249)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Search**

Người dùng chọn **Search**. Hệ thống hiển thị danh sách bài kiểm tra thỏa mãn điều kiện tìm kiếm.
{% endstep %}

{% step %}
**Chọn Reset**

Người dùng chọn **Reset** nếu muốn xóa toàn bộ điều kiện. Hệ thống hiển thị lại danh sách theo trạng thái mặc định.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xem thông tin học viên theo từng bài kiểm tra</summary>

{% stepper %}
{% step %}
**Mở chi tiết bài kiểm tra**

Người dùng chọn **tên bài kiểm tra** tại tab **Test/Quiz**. Hệ thống mở màn hình chi tiết bài kiểm tra theo học viên.

<figure><img src="../../.gitbook/assets/image (251)" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (253)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Hoặc chọn Action → Detail**

Người dùng chọn **Action → Detail** tại bài kiểm tra cần xem nếu không mở bằng tên bài kiểm tra. Hệ thống mở màn hình chi tiết bài kiểm tra theo học viên.

<figure><img src="../../.gitbook/assets/image (256)" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (253)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xem danh sách học viên và trạng thái bài làm**

Hệ thống hiển thị thông tin: Student Name, Email, Access Period, Submission Time, Status, Grading Attempts, Final score, Grader, Comment.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tìm kiếm/lọc học viên trong bài kiểm tra</summary>

{% stepper %}
{% step %}
**Nhập/chọn điều kiện tìm kiếm**

Người dùng nhập hoặc chọn điều kiện tại màn hình chi tiết bài kiểm tra (tên học viên, trạng thái bài làm, người chấm).

<figure><img src="../../.gitbook/assets/image (258)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Search**

Người dùng chọn **Search**. Hệ thống hiển thị danh sách học viên thỏa mãn điều kiện tìm kiếm.
{% endstep %}

{% step %}
**Chọn Reset**

Người dùng chọn **Reset** nếu muốn xóa điều kiện. Hệ thống hiển thị lại danh sách học viên theo trạng thái mặc định.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Cài đặt thời gian truy cập bài kiểm tra cho toàn bộ học viên</summary>

{% stepper %}
{% step %}
**Chọn Action → Edit Access Time**

Người dùng chọn **Action → Edit Access Time** tại bài kiểm tra cần cài đặt trong tab **Test/Quiz**. Hệ thống hiển thị popup cài đặt thời gian truy cập.

<figure><img src="../../.gitbook/assets/image (259)" alt=""><figcaption></figcaption></figure>

Hệ thống hiển thị popup cài đặt thời gian truy cập.

<figure><img src="../../.gitbook/assets/image (261)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn giờ mở và giờ đóng**

Người dùng chọn **giờ mở** và **giờ đóng** cho bài kiểm tra tại popup **Edit Access Time**.
{% endstep %}

{% step %}
**Chọn Save**

Người dùng chọn **Save**. Hệ thống lưu thời gian truy cập và áp dụng cho toàn bộ học viên được làm bài kiểm tra.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Cài đặt thời gian truy cập bài kiểm tra cho một học viên</summary>

{% stepper %}
{% step %}
**Mở chi tiết bài kiểm tra**

Người dùng mở màn hình chi tiết của bài kiểm tra cần cài đặt thời gian riêng.
{% endstep %}

{% step %}
**Chọn Action → Edit Access Time tại dòng học viên**

Người dùng chọn **Action → Edit Access Time** tại dòng học viên cần cài đặt. Hệ thống hiển thị popup cài đặt thời gian truy cập cho học viên.

<figure><img src="../../.gitbook/assets/image (262)" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (261)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn giờ mở và giờ đóng**

Người dùng chọn **giờ mở** và **giờ đóng** cho học viên tại popup **Edit Access Time**.
{% endstep %}

{% step %}
**Chọn Save**

Người dùng chọn **Save**. Hệ thống lưu thời gian truy cập và chỉ áp dụng cho học viên được chọn.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xóa thời gian truy cập bài kiểm tra</summary>

{% stepper %}
{% step %}
**Chọn Action → Delete Access Time**

Người dùng chọn **Action → Delete Access Time** tại bài kiểm tra cần xóa thời gian truy cập trong tab **Test/Quiz**. Hệ thống hiển thị popup xác nhận xóa.

<figure><img src="../../.gitbook/assets/image (263)" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (264)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xác nhận xóa**

Người dùng chọn **Yes** tại popup xác nhận. Hệ thống xóa thời gian truy cập đã cài đặt trước đó của bài kiểm tra.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xuất kết quả bài kiểm tra ra file Excel</summary>

{% stepper %}
{% step %}
**Chọn Action → Export Result**

Người dùng chọn **Action → Export Result** tại bài kiểm tra cần xuất kết quả trong tab **Test/Quiz**. Hệ thống tạo file Excel chứa điểm của toàn bộ học viên theo bài kiểm tra được chọn.

<figure><img src="../../.gitbook/assets/image (265)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Hệ thống tải file về thiết bị**

Hệ thống tải file kết quả về thiết bị. File được đặt tên theo cú pháp: **\[Mã lớp]\_\[Tên bài kiểm tra]**.
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Người dùng cần có quyền xem danh sách bài kiểm tra của lớp để truy cập tab **Test/Quiz**.
2. Khóa học cần được gắn vào lớp thì hệ thống mới hiển thị danh sách bài kiểm tra của khóa học.
3. Danh sách bài kiểm tra lấy theo các bài Test/Quiz đã được cấu hình trong Course Content.
4. Thời gian truy cập bài kiểm tra có thể được cài đặt cho toàn bộ học viên hoặc cho riêng từng học viên; thời gian riêng chỉ áp dụng cho học viên đó.
5. File Export Result hiển thị rỗng thông tin điểm nếu học viên chưa nộp bài hoặc bài làm chưa được chấm xong (với bài chấm thủ công).
{% endhint %}

### Quy tắc trạng thái bài làm của học viên

| Hình thức chấm bài        | Trạng thái       | Ý nghĩa                                 |
| ------------------------- | ---------------- | --------------------------------------- |
| **Hệ thống chấm tự động** | Unsubmitted      | Học viên chưa nộp bài.                  |
| **Hệ thống chấm tự động** | Submitted        | Học viên đã hoàn thành bài kiểm tra.    |
| **Chấm thủ công**         | Unsubmitted      | Học viên chưa nộp bài.                  |
| **Chấm thủ công**         | Awaiting Grading | Học viên đã nộp bài và đang chờ chấm.   |
| **Chấm thủ công**         | Finish Grading   | Bài làm của học viên đã được chấm xong. |

### Quy tắc cài đặt Access Time

| Quy tắc                               | Mô tả                                                                                                        |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **Start date của Access Time**        | Phải lớn hơn hoặc bằng Start Date của Class.                                                                 |
| **End date của Access Time**          | Phải nhỏ hơn hoặc bằng End Date của Class.                                                                   |
| **Khi Start Date của Class thay đổi** | Nếu Start Date mới lớn hơn Start date của Access Time, Access Time sẽ được cập nhật theo Start Date của lớp. |
| **Khi End Date của Class thay đổi**   | Nếu End Date mới nhỏ hơn End Date của Access Time, Access Time sẽ được cập nhật theo End Date của lớp.       |

### Quy tắc Export Result

| Quy tắc                              | Mô tả                                            |
| ------------------------------------ | ------------------------------------------------ |
| **Tên file export**                  | Theo cú pháp **\[Mã lớp]\_\[Tên bài kiểm tra]**. |
| **Học viên chưa nộp bài**            | Thông tin điểm trong file Excel hiển thị rỗng.   |
| **Bài chấm thủ công chưa chấm xong** | Thông tin điểm trong file Excel hiển thị rỗng.   |
| **Bài đã có điểm hợp lệ**            | Hệ thống hiển thị điểm trong file Excel.         |

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                             | Nguyên nhân                                                 | Cách xử lý                                                        |
| -------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------------- |
| Không thấy danh sách bài kiểm tra            | Khóa học chưa được gắn vào lớp                              | Gắn khóa học vào lớp; bài Test/Quiz lấy từ Course Content         |
| Không tìm thấy bài kiểm tra                  | Sai điều kiện tìm kiếm/lọc                                  | Kiểm tra lại bộ lọc, bấm Reset để về danh sách mặc định           |
| Không lưu được Access Time                   | Start/End date ngoài khoảng Start Date – End Date của Class | Đặt Access Time trong khoảng cho phép của lớp                     |
| Access Time tự thay đổi sau khi sửa lịch lớp | Start Date/End Date của Class thay đổi                      | Đây là quy tắc đồng bộ; kiểm tra lại Access Time sau khi đổi lịch |
| File Export Result thiếu điểm                | Học viên chưa nộp bài hoặc bài chấm thủ công chưa chấm xong | Chờ học viên nộp/chấm xong rồi export lại                         |
| Không truy cập được tab Test/Quiz            | Tài khoản chưa có quyền xem bài kiểm tra của lớp            | Liên hệ quản trị để được cấp quyền                                |
