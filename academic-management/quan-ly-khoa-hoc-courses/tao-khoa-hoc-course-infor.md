# Tạo khóa học

## I. Giới thiệu chung

{% hint style="info" %}
**Dành cho:** UpLMS Operator, L\&D

**Đường dẫn:** UpLMS Ops → Academic Management → Course & Materials → Courses
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Academic Management > Course & Materials
* **Chức năng chính:** Create Course Info
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Người dùng đã đăng nhập thành công vào hệ thống UpLMS Ops.
* Tài khoản có quyền truy cập nhóm chức năng **Course**.
{% endhint %}

## II. Hướng dẫn chi tiết

{% stepper %}
{% step %}
**Truy cập Academic Management → Course & Materials → Course List → Create Course**

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Điền thông tin và tạo khóa học**

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

Các trường thông tin:

* Course Name (bắt buộc): tên khóa học.
* Describe: thông tin mô tả nội dung hoặc mục tiêu chính của khóa học.
* Code: mã khóa học, không được trùng với với code của khóa học khác.
* Tag: chọn tag đã có hoặc tạo tag mới.
* Course Category (bắt buộc): danh mục của khóa học.
* Type (bắt buộc):
  * Normal Course: khóa học bình thường.
  * Foundation Course: khóa học nền tảng.
* Pass Point (bắt buộc): mức điểm tối thiểu học viên cần đạt để hoàn thành khóa học.
* Điểm thành phần (bắt buộc): tỷ trọng tạo thành tổng điểm để đánh giá hoàn thành khóa học khi so sánh với pass point

Chọn Save để hệ thống tạo khóa học mới với thông tin đã nhập, trước khi chuyển sang bước tạo nội dung chi tiết trong khóa học.

{% hint style="info" %}
* Một Normal Course có thể gắn với một Foundation Course, khi đó học viên bắt buộc phải hoàn thành khóa học Foundation trước khi học khóa học chính.
* Normal Course có thể gắn với Foundation Course hoặc không.
{% endhint %}
{% endstep %}
{% endstepper %}

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Course Info là bước đầu tiên trong quy trình tạo khóa học.
2. Các trường có dấu **(\*)** là trường bắt buộc.
3. **Code** là mã định danh khóa học và không được trùng với mã khóa học đã tồn tại.
4. **Type** là trường bắt buộc và ảnh hưởng đến các thông tin cần cấu hình tiếp theo. Nếu chọn **Type** là **Normal Course**, hệ thống hiển thị danh sách Foundation Course có thể chọn đi kèm.
5. Tổng điểm thành phần bắt buộc phải bằng **100**.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                    | Nguyên nhân                                                                            | Cách xử lý                                                                      |
| ----------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Không thấy nút Create Course        | Tài khoản chưa có quyền tạo khóa học                                                   | Liên hệ Admin hệ thống để kiểm tra phân quyền                                   |
| Không lưu được Course Info          | Thiếu trường bắt buộc                                                                  | Kiểm tra và nhập đầy đủ các trường có dấu **(\*)**                              |
| Hệ thống báo mã khóa học đã tồn tại | Code bị trùng với khóa học đã có                                                       | Nhập mã khóa học khác                                                           |
| Không hiển thị Foundation Course    | Hệ thống chỉ hiện thị các khóa Foundation có cùng Category với Normal Course đang tạo. | Kiểm tra danh sách Foundation Course cùng Category với Normal Course đang tạo.  |
| Không lưu được điểm thành phần      | Tổng điểm các thành phần không bằng 100                                                | Kiểm tra và điều chỉnh lại tỷ trọng điểm                                        |
