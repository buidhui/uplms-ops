# Danh sách lớp học

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** Admin, UpLMS Operator, CX User

**Đường dẫn:** Academic Management → Class → Class List
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Class
* **Chức năng chính:** Class List / Class Detail
* **Module liên quan:** Course, Student, Mentor, Teacher, Test/Quiz, Resources, Examination, Marks
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Người dùng đã đăng nhập thành công vào hệ thống **UpLMS Operations**.
* Tài khoản có quyền truy cập module **Class**.
* Tài khoản có quyền xem danh sách lớp học.
* Tài khoản có quyền xem thông tin chi tiết lớp học.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Xem danh sách lớp học</summary>

{% stepper %}
{% step %}
**Chọn Class List tại menu Class**

Người dùng chọn **Class List** tại menu **Class**. Hệ thống hiển thị màn hình **Class List**.

<figure><img src="../../.gitbook/assets/image (188)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xem danh sách lớp học**

Người dùng xem danh sách lớp học tại bảng dữ liệu trên màn hình **Class List**. Hệ thống hiển thị danh sách theo thời gian tạo giảm dần.

Các cột thông tin trong bảng danh sách:

<table data-search="false"><thead><tr><th>Cột thông tin</th><th>Mô tả</th></tr></thead><tbody><tr><td><strong>#</strong></td><td>Số thứ tự của lớp học trên danh sách.</td></tr><tr><td><strong>Class</strong></td><td>Tên lớp học. Người dùng có thể nhấp vào tên lớp để xem chi tiết.</td></tr><tr><td><strong>Code</strong></td><td>Mã lớp học.</td></tr><tr><td><strong>Construction Mode</strong></td><td>Hình thức học của lớp.</td></tr><tr><td><strong>Number Of Students</strong></td><td>Số lượng học viên hiện có trong lớp.</td></tr><tr><td><strong>Status</strong></td><td>Trạng thái hiện tại của lớp học.</td></tr><tr><td><strong>Class Foundation</strong></td><td>Hiển thị lớp Foundation liên quan nếu lớp có gắn Foundation.</td></tr><tr><td><strong>Action/Menu ba chấm</strong></td><td>Cho phép thao tác với lớp học tương ứng.</td></tr></tbody></table>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tìm kiếm/lọc lớp học</summary>

{% stepper %}
{% step %}
**Nhập/chọn điều kiện tìm kiếm**

Người dùng nhập hoặc chọn điều kiện tìm kiếm tại vùng bộ lọc của màn hình **Class List**.

<figure><img src="../../.gitbook/assets/image (189)" alt=""><figcaption></figcaption></figure>

Có thể lọc theo các trường: tên/mã lớp (Search by name and code), Code, Program, Subject, Status, Facility, Construction Mode (Blended, Hybrid, Online, Recorded Online...), Type, Class Owner, CX Admin, Sort by hoặc khoảng thời gian (From date - To date).
{% endstep %}

{% step %}
**Chọn Search để áp dụng**

Người dùng chọn **Search** để áp dụng điều kiện. Hệ thống hiển thị danh sách lớp học thỏa mãn điều kiện đã nhập.
{% endstep %}

{% step %}
**Chọn Reset để xóa điều kiện**

Người dùng chọn **Reset** để xóa toàn bộ điều kiện tìm kiếm. Hệ thống hiển thị lại danh sách lớp học theo trạng thái mặc định.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xem thông tin chi tiết lớp học</summary>

{% stepper %}
{% step %}
**Mở màn hình Class Detail**

Người dùng nhấp vào **tên lớp học** tại màn hình **Class List**. Hệ thống mở màn hình **Class Detail** của lớp được chọn.

<figure><img src="../../.gitbook/assets/image (190)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tab Overview — thông tin tổng quan**

<figure><img src="../../.gitbook/assets/image (191)" alt=""><figcaption></figcaption></figure>

Người dùng chọn tab **Overview** để xem thông tin tổng quan của lớp học.

<table data-search="false"><thead><tr><th>Thông tin</th><th>Mô tả</th></tr></thead><tbody><tr><td><strong>Name</strong></td><td>Tên lớp học.</td></tr><tr><td><strong>Code</strong></td><td>Mã lớp học.</td></tr><tr><td><strong>Status</strong></td><td>Trạng thái lớp học.</td></tr><tr><td><strong>Construction Mode</strong></td><td>Hình thức học của lớp.</td></tr><tr><td><strong>Facility</strong></td><td>Cơ sở của lớp học.</td></tr><tr><td><strong>Type</strong></td><td>Loại lớp học.</td></tr><tr><td><strong>No. of Students</strong></td><td>Số lượng học viên hiện tại / số lượng học viên tối đa.</td></tr><tr><td><strong>Opening at</strong></td><td>Ngày mở khóa học online.</td></tr><tr><td><strong>Start Date</strong></td><td>Ngày bắt đầu lớp học.</td></tr><tr><td><strong>End Date</strong></td><td>Ngày kết thúc lớp học.</td></tr><tr><td><strong>Expire Date</strong></td><td>Ngày hết hạn truy cập lớp học.</td></tr><tr><td><strong>Number of Extended Days</strong></td><td>Số ngày gia hạn thêm cho học viên sau khi lớp kết thúc.</td></tr><tr><td><strong>Reason For Extension</strong></td><td>Lý do gia hạn.</td></tr><tr><td><strong>Standard Schedule</strong></td><td>Lịch học cố định của lớp.</td></tr><tr><td><strong>Classroom name</strong></td><td>Tên phòng học.</td></tr><tr><td><strong>Course</strong></td><td>Khóa học được gắn với lớp.</td></tr><tr><td><strong>Exam</strong></td><td>Kỳ thi được gắn với lớp.</td></tr><tr><td><strong>Class Owner</strong></td><td>Người phụ trách lớp.</td></tr><tr><td><strong>CX Admin</strong></td><td>Người phụ trách CX Admin của lớp.</td></tr><tr><td><strong>Description</strong></td><td>Mô tả lớp học.</td></tr></tbody></table>
{% endstep %}

{% step %}
**Tab Calendar — lịch học của lớp**

Người dùng chọn tab **Calendar** để xem lịch học theo dạng Calendar. (Chỉ hiển thị với lớp có Construction Mode = Offline, Blended, Live\_Online, Hybrid)

<figure><img src="../../.gitbook/assets/image (192)" alt=""><figcaption></figcaption></figure>

| Thành phần              | Mô tả                                            |
| ----------------------- | ------------------------------------------------ |
| **Generate Schedule**   | Tạo lịch học tự động cho lớp nếu có quyền.       |
| **Add Lesson**          | Thêm buổi học mới vào lịch.                      |
| **Bộ điều hướng tháng** | Chuyển sang tháng trước hoặc tháng sau.          |
| **Today**               | Quay về ngày hiện tại.                           |
| **Month view**          | Hiển thị lịch theo tháng.                        |
| **Legend**              | Chú thích màu/biểu tượng của từng loại buổi học. |

Ý nghĩa chú thích trên Calendar:

| Chú thích       | Ý nghĩa                                 |
| --------------- | --------------------------------------- |
| **Online**      | Buổi học online.                        |
| **Live Online** | Buổi học live online.                   |
| **Offline**     | Buổi học offline.                       |
| **Cancelled**   | Buổi học đã bị hủy.                     |
| **Holiday**     | Ngày nghỉ/lịch nghỉ lễ.                 |
| **Case Study**  | Buổi học hoặc nội dung có Case Study.   |
| **Test**        | Buổi học hoặc nội dung có bài kiểm tra. |
| **Key Content** | Nội dung học trọng tâm.                 |
{% endstep %}

{% step %}
**Tab Progress — tiến độ học tập**

Người dùng chọn tab **Progress** để xem tiến độ học tập của lớp. Hệ thống hiển thị thông tin tiến độ giảng dạy theo dữ liệu giảng viên đã khai báo.

<figure><img src="../../.gitbook/assets/image (194)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tab Students — danh sách học viên**

Người dùng chọn tab **Students** để xem danh sách học viên đang thuộc lớp học.

<figure><img src="../../.gitbook/assets/image (196)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tab Mentors — danh sách trợ giảng**

Người dùng chọn tab **Mentors** để xem danh sách trợ giảng đang được gắn với lớp học.

<figure><img src="../../.gitbook/assets/image (198)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tab Teachers — danh sách giảng viên**

Người dùng chọn tab **Teachers** để xem danh sách giảng viên đang được gắn với lớp học.

<figure><img src="../../.gitbook/assets/image (200)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tab Test/Quiz — danh sách bài kiểm tra**

Người dùng chọn tab **Test/Quiz** để xem danh sách bài kiểm tra trong khóa học gắn với lớp (nếu khóa học có cấu hình Test/Quiz).

<figure><img src="../../.gitbook/assets/image (202)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Người dùng cần có quyền xem danh sách lớp học để truy cập màn hình **Class List**.
2. Người dùng cần có quyền xem chi tiết lớp học để mở màn hình **Class Detail**.
3. Danh sách lớp học mặc định hiển thị theo thời gian tạo giảm dần.
4. Có thể tìm kiếm/lọc lớp học theo nhiều điều kiện: tên/mã lớp, Program, Subject, Status, Facility, Construction Mode, Type, Class Owner, CX Admin và khoảng thời gian.
5. Khi nhấp vào tên lớp học, hệ thống mở màn hình chi tiết lớp học.
6. Tab **Calendar** chỉ hiển thị với lớp có Construction Mode = Offline, Blended, Live\_Online, Hybrid.
{% endhint %}

{% hint style="info" %}
### Mẹo sử dụng

1. Khi cần tìm nhanh một lớp cụ thể, nên nhập một phần tên lớp hoặc mã lớp vào ô **Search by name and code**.
2. Khi có nhiều lớp cùng chương trình, nên kết hợp bộ lọc **Program + Subject** để thu hẹp kết quả.
3. Nên dùng **Construction Mode** để phân biệt nhanh lớp Blended, Hybrid, Online hoặc Offline.
4. Có thể kiểm tra cột **Class Foundation** để biết lớp có liên quan đến lớp Foundation hay không.
5. Khi cần kiểm tra lịch học, nên vào tab **Calendar** thay vì chỉ xem ngày bắt đầu/kết thúc ở Overview.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                        | Nguyên nhân                                                              | Cách xử lý                                                  |
| --------------------------------------- | ------------------------------------------------------------------------ | ----------------------------------------------------------- |
| Không tìm thấy lớp học                  | Điều kiện tìm kiếm/lọc chưa đúng hoặc quá hẹp                            | Kiểm tra lại bộ lọc, bấm Reset để về danh sách mặc định     |
| Danh sách không hiển thị dữ liệu mới    | Danh sách đang bị lọc theo điều kiện trước đó                            | Chọn Reset để xóa bộ lọc                                    |
| Không mở được màn hình Class Detail     | Tài khoản chưa có quyền xem chi tiết lớp học                             | Liên hệ quản trị để được cấp quyền xem chi tiết lớp học     |
| Không thấy tab Calendar                 | Lớp có Construction Mode không thuộc Offline/Blended/Live\_Online/Hybrid | Tab Calendar chỉ áp dụng cho các Construction Mode nói trên |
| Không truy cập được màn hình Class List | Tài khoản chưa có quyền xem danh sách lớp học                            | Liên hệ quản trị để được cấp quyền truy cập module Class    |
