# Quản lý học viên trong lớp

## I. Thông tin chung

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Class
* **Module liên quan:** Student
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Thêm học viên vào lớp</summary>

{% stepper %}
{% step %}
**Chọn Tab Students** → **Add Students**

<figure><img src="../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn học viên cần thêm vào lớp → Add**

<figure><img src="../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Import học viên vào lớp</summary>

{% stepper %}
{% step %}
**Chọn Tab Students** → **Import Student**

<figure><img src="../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn file danh sách học viên cần Import vào lớp → Import**

<figure><img src="../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Nên tải **file mẫu** trước khi nhập dữ liệu import; dữ liệu cần tuân thủ đúng cấu trúc và định dạng của template.
{% endhint %}
{% endstep %}

{% step %}
**Xem kết quả Import**

Hộp thoại kết quả import hiển thị sau khi xử lý file:

* Tên file
* Tổng số bản ghi
* Số học viên thêm thành công và số học viên thêm thất bại
{% endstep %}

{% step %}
**Xem View Log**

Chọn **View Log** tại hộp thoại kết quả import để xem chi tiết trạng thái từng bản ghi.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xóa học viên khỏi lớp</summary>

**Xóa một học viên**

<figure><img src="../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

**Xóa nhiều học viên**

<figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Chỉnh sửa thời hạn truy cập cho từng học viên</summary>

{% stepper %}
{% step %}
**Class Detail → Student → Action → Update Duration**

<figure><img src="../.gitbook/assets/2026-08-24_11-17-18.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Cập nhật thời hạn mới → Save**

<figure><img src="../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Điều chỉnh cấu phần học theo từng học viên</summary>

{% stepper %}
{% step %}
**Class Detail → Student → Action → Edit Course Content**

<figure><img src="../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Điều chỉnh cấu phần → Save**

<figure><img src="../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

**Quy tắc chọn/ bỏ chọn cấu phần học của học viên**

<table data-search="false"><thead><tr><th>Thao tác</th><th>Quy tắc</th></tr></thead><tbody><tr><td><strong>Chọn/ Bỏ chọn All</strong></td><td>Tất cả checkbox cấu phần học được tick hoặc bỏ tick.</td></tr><tr><td><strong>Chọn Section</strong></td><td>Tất cả Activity, Test, Quiz thuộc Section được chọn.</td></tr><tr><td><strong>Chọn Activity</strong></td><td>Section chứa Activity đó được chọn.</td></tr><tr><td><strong>Bỏ chọn cấu phần học</strong></td><td>Cấu phần bị bỏ chọn sẽ không xuất hiện trong chương trình học của học viên và học viên không cần học cấu phần đó.</td></tr><tr><td><strong>Xóa cấu phần đã học</strong></td><td>Không được phép xóa khỏi chương trình học của học viên.</td></tr><tr><td><strong>Xóa cấu phần chưa học</strong></td><td>Được phép xóa khỏi chương trình học của học viên.</td></tr></tbody></table>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Cho học viên hoàn thành khóa Foundation</summary>

**Tại lớp Lesson có gắn Foundation → Student → Action → Allow Pass Foundation**

<figure><img src="../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Sau khi Allow Pass Foundation, học viên không bắt buộc phải hoàn thành khóa học nền tảng và có thể bắt đầu học luôn khóa học chính.
{% endhint %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Khi thêm/ xóa học viên khỏi lớp **Type = Lesson**, học viên đó cũng được thêm/ xóa ở lớp **Foundation** gắn với lớp ban đầu.
2. Với lớp có **Duration = Flexible**, nếu học viên chưa kích hoạt khóa học thì không thể cập nhật thời hạn học của học viên đó.
3. Thời hạn học riêng của học viên có thể dài hơn hoặc ngắn hơn thời hạn mặc định của lớp.
4. Chỉnh sửa cấu phần học của từng học viên chỉ áp dụng cho học viên được chọn, không ảnh hưởng đến toàn bộ lớp.
5. Chỉ được xóa cấu phần học khỏi chương trình của học viên nếu học viên chưa học cấu phần đó; nếu đã học thì hệ thống không cho phép xóa.
6. Chức năng **Allow Pass Foundation** chỉ áp dụng khi lớp Lesson có gắn lớp Foundation và học viên cần được đánh dấu hoàn thành Foundation để học khóa chính.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                           | Nguyên nhân                                                 | Cách xử lý                                            |
| ------------------------------------------ | ----------------------------------------------------------- | ----------------------------------------------------- |
| Không cập nhật được thời hạn học           | Lớp Duration = Flexible và học viên chưa kích hoạt khóa học | Chờ học viên kích hoạt khóa học rồi cập nhật thời hạn |
| Không xóa được cấu phần học của học viên   | Học viên đã học cấu phần đó                                 | Chỉ được xóa cấu phần học viên chưa học               |
| Không thực hiện được thao tác với học viên | Tài khoản chưa có quyền quản lý học viên trong lớp          | Liên hệ Admin hệ thống để kiểm tra phân quyền         |
