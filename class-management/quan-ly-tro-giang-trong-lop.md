# Quản lý trợ giảng trong lớp (Mentor)

## Record of changes

_A - Add | M - Modify | D - Delete_

| Effective Date | Update Person | A,M,D | Change Description             | Version |
| -------------- | ------------- | ----- | ------------------------------ | ------- |
| May 25, 2026   | Lê Xuân Mai   | M     | Chuẩn hóa nội dung lên GitBook | 4.7.0   |

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** Admin, UpLMS Operator, CX

**Đường dẫn:** LMS → Class List → Chọn lớp học → Mentors
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Class
* **Chức năng chính:** Mentors
* **Module liên quan:** Class List, Class Detail, Staff List, Foundation Class, Lesson Class
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Người dùng đã đăng nhập thành công vào hệ thống **UpLMS Operations**.
* Tài khoản có quyền truy cập module **Class** và quyền xem chi tiết lớp học.
* Tài khoản có quyền thêm/xóa trợ giảng trong lớp.
* Lớp học đã được tạo trên hệ thống.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Thêm trợ giảng vào lớp</summary>

{% stepper %}
{% step %}
**Mở màn hình Class Detail**

Người dùng nhấp vào **tên lớp học** tại màn hình **Class List**. Hệ thống mở màn hình **Class Detail**.
{% endstep %}

{% step %}
**Mở tab Mentors**

Người dùng mở tab **Mentors** tại màn hình **Class Detail**.

<figure><img src="../.gitbook/assets/image (237)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Add Mentor**

Người dùng chọn **Add Mentor** tại tab **Mentors**. Hệ thống chuyển đến màn hình **Add Mentor**.

<figure><img src="../.gitbook/assets/image (238)" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (239)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tìm kiếm trợ giảng**

Người dùng tìm kiếm trợ giảng tại khu vực tìm kiếm của màn hình **Add Mentor** nếu cần.
{% endstep %}

{% step %}
**Tick chọn trợ giảng**

Người dùng tick chọn trợ giảng cần thêm vào lớp tại danh sách trợ giảng.
{% endstep %}

{% step %}
**Chọn Add**

Người dùng chọn **Add** tại màn hình **Add Mentor**. Hệ thống thêm trợ giảng đã chọn vào lớp và quay lại danh sách trợ giảng của lớp.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chọn trợ giảng chính</summary>

{% stepper %}
{% step %}
**Mở tab Mentors**

Người dùng mở tab **Mentors** trong màn hình **Class Detail**.
{% endstep %}

{% step %}
**Xác định trợ giảng chính**

Người dùng xác định trợ giảng cần đặt làm trợ giảng chính tại danh sách **Mentors**.
{% endstep %}

{% step %}
**Tick cột Main Responsible**

Người dùng tick vào ô tương ứng tại cột **Main Responsible**. Hệ thống ghi nhận trợ giảng được chọn là trợ giảng chính của lớp.

<figure><img src="../.gitbook/assets/image (240)" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Trường **Main Responsible** liên quan đến tính năng chấm điểm.
{% endhint %}
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xóa một trợ giảng khỏi lớp</summary>

{% stepper %}
{% step %}
**Mở tab Mentors**

Người dùng mở tab **Mentors** trong màn hình **Class Detail**.
{% endstep %}

{% step %}
**Chọn Action → Delete**

Người dùng chọn **Action → Delete** tại dòng trợ giảng cần xóa. Hệ thống hiển thị popup xác nhận xóa.

<figure><img src="../.gitbook/assets/image (241)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xác nhận xóa**

Người dùng chọn **Yes** tại popup xác nhận. Hệ thống xóa trợ giảng khỏi lớp.

<figure><img src="../.gitbook/assets/image (242)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xóa nhiều trợ giảng khỏi lớp</summary>

{% stepper %}
{% step %}
**Mở tab Mentors**

Người dùng mở tab **Mentors** trong màn hình **Class Detail**.
{% endstep %}

{% step %}
**Tick chọn các trợ giảng cần xóa**

Người dùng tick chọn các trợ giảng cần xóa tại danh sách **Mentors**.
{% endstep %}

{% step %}
**Chọn Delete Selected**

Người dùng chọn **Delete Selected** tại tab **Mentors**. Hệ thống hiển thị popup xác nhận xóa.

<figure><img src="../.gitbook/assets/image (243)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xác nhận xóa**

Người dùng chọn **Yes** tại popup xác nhận. Hệ thống xóa các trợ giảng đã chọn khỏi lớp.

<figure><img src="../.gitbook/assets/image (245)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Người dùng cần có quyền quản lý trợ giảng trong lớp để thêm hoặc xóa trợ giảng.
2. Danh sách trợ giảng được lấy từ **Staff List** trên hệ thống.
3. Người dùng có thể thêm một hoặc nhiều trợ giảng vào lớp; có thể xóa từng trợ giảng hoặc nhiều trợ giảng cùng lúc.
4. Trợ giảng được chọn tại cột **Main Responsible** được hiểu là trợ giảng chính của lớp.
5. Nếu lớp **Lesson** có gắn với lớp **Foundation**, khi thêm/xóa trợ giảng khỏi lớp Lesson thì trợ giảng đó cũng được thêm/xóa tại lớp Foundation.
6. Việc thêm/xóa trợ giảng ở lớp Foundation không tác động ngược lại lớp Lesson.
{% endhint %}

### Quy tắc đồng bộ trợ giảng giữa Lesson và Foundation

| Trường hợp                                      | Quy tắc                                                |
| ----------------------------------------------- | ------------------------------------------------------ |
| Thêm trợ giảng vào lớp Lesson có gắn Foundation | Trợ giảng cũng được thêm vào lớp Foundation tương ứng. |
| Xóa trợ giảng khỏi lớp Lesson có gắn Foundation | Trợ giảng cũng được xóa khỏi lớp Foundation tương ứng. |
| Thao tác tại lớp không gắn Foundation           | Chỉ áp dụng cho lớp đang thao tác.                     |

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                              | Nguyên nhân                                             | Cách xử lý                                                  |
| --------------------------------------------- | ------------------------------------------------------- | ----------------------------------------------------------- |
| Không tìm thấy trợ giảng cần thêm             | Trợ giảng chưa có trong **Staff List**                  | Kiểm tra/đảm bảo nhân sự đã tồn tại trong Staff List        |
| Xóa trợ giảng ở lớp Lesson ảnh hưởng lớp khác | Lớp Lesson đồng bộ trợ giảng với lớp Foundation gắn kèm | Hiểu rõ ràng buộc: thao tác ở Lesson áp dụng cho Foundation |
| Không chọn được Main Responsible              | Chưa thêm trợ giảng vào lớp hoặc thiếu quyền            | Thêm trợ giảng trước; kiểm tra quyền quản lý trợ giảng      |
| Không thực hiện được thêm/xóa trợ giảng       | Tài khoản chưa có quyền quản lý trợ giảng trong lớp     | Liên hệ quản trị để được cấp quyền                          |
