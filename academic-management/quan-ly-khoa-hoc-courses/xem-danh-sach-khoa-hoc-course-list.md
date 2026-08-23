# Danh sách khóa học

## I. Giới thiệu chung

{% hint style="info" %}
**Dành cho:** UpLMS Operator, L\&D

**Đường dẫn:** UpLMS Ops → Academic Management → Course & Materials → Courses
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Người dùng đã đăng nhập thành công vào hệ thống vận hành UpLMS Ops.
* Tài khoản có quyền truy cập nhóm chức năng **Course**.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Danh sách khóa học</summary>

**Academic Management → Course & Materials → Course List**

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

Thông tin tổng quan của từng khóa học tại bảng danh sách, bao gồm:

* Course name
* Type
* Course Category
* Status
* Created date
* Updated date

</details>

<details>

<summary>Tìm kiếm khóa học</summary>

{% stepper %}
{% step %}
**Tìm kiếm theo tên khóa học**

Tại ô **Search course name**, nhập tên khóa học cần tìm.

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tìm kiếm bằng bộ lọc**

<figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Khóa học ở trạng thái **Block** không thể được thêm vào lớp học.
2. Khóa học ở trạng thái **Lock** là khóa học đã có ít nhất một học viên đã bắt đầu học khóa học đó.
3. Các thao tác trong **Action** phụ thuộc vào quyền tài khoản và trạng thái hiện tại của khóa học.
{% endhint %}

{% hint style="info" %}
### Mẹo sử dụng

1. Dùng bộ lọc **Status = Draft** để kiểm tra các khóa học đang tạo dở/ chưa publish.
2. Dùng bộ lọc **Status = Publish** để kiểm tra các khóa học đã sẵn sàng thêm vào lớp học.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                    | Nguyên nhân                                                              | Cách xử lý                                          |
| ----------------------------------- | ------------------------------------------------------------------------ | --------------------------------------------------- |
| Không thấy menu Course List         | Tài khoản chưa được cấp quyền truy cập                                   | Liên hệ Admin hệ thống để kiểm tra phân quyền       |
| Không thấy nút Create Course        | Tài khoản chưa có quyền tạo khóa học                                     | Liên hệ Admin hệ thống để kiểm tra phân quyền       |
| Không thao tác được tại menu Action | Tài khoản chưa có quyền hoặc trạng thái khóa học không cho phép thao tác | Liên hệ Admin hệ thống để kiểm tra phân quyền       |
| Khóa học không thêm được vào lớp    | Khóa học đang ở trạng thái Block hoặc Draft                              | Kiểm tra trạng thái khóa học trước khi thêm vào lớp |
