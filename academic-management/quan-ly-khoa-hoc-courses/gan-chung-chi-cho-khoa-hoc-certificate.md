# Thêm chứng chỉ khóa học

## I. Giới thiệu chung

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Certificate
* **Module liên quan:**
  * Resource
  * Certificate Template
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Tài khoản người dùng có quyền tạo/ chỉnh sửa khóa học.
* Khóa học đã được tạo thành công tại bước **Course Info**.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Thêm chứng chỉ cho khóa học</summary>

{% hint style="info" %}
* Chứng chỉ được tạo ở bước [certificate-management.md](../certificate-management.md "mention") ở bước này, nhân sự tạo khóa học chỉ thêm chứng chỉ bằng cách chọn từ kho chứng chỉ đã có trên hệ thống.
* Học viên sẽ nhận được chứng chỉ sau khi hoàn thành khóa học.
{% endhint %}

{% stepper %}
{% step %}
**Truy cập bước Certificate**

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Choose Template → Chọn chứng chỉ → Confirm**&#x20;

{% hint style="info" %}
Hệ thống chỉ hiển thị danh sách chứng chỉ có cùng Caegory với Category của khóa học.
{% endhint %}
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Thay đổi mẫu chứng chỉ</summary>

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. **Certificate** là bước cuối cùng trong quy trình tạo khóa học.
2. Nếu chưa có Certificate Template phù hợp, tạo trong chức năng [certificate-management.md](../certificate-management.md "mention")
3. Việc thay đổi chứng chỉ của khóa học có thể ảnh hưởng đến chứng chỉ học viên nhận được sau khi hoàn thành khóa học.
{% endhint %}

{% hint style="info" %}
### Mẹo sử dụng

1. Nên đặt tên Certificate Template rõ ràng theo chương trình, môn học hoặc loại khóa học để dễ phân loại.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                   | Nguyên nhân                                                                                                                   | Cách xử lý                                         |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| Không thấy nút Choose Template     | Tài khoản chưa có quyền chỉnh sửa khóa học.                                                                                   | Liên hệ Admin hệ thống để kiểm tra quyền tài khoản |
| Danh sách template trống           | <ul><li>Chưa có Certificate Template trên hệ thống.</li><li>Chưa có Certificate cùng Category với khóa học đang tạo</li></ul> | Tạo mới Template trong chức năng Certificates      |
| Học viên không nhận đúng chứng chỉ | Khóa học đang gán sai Template hoặc Template chưa được cập nhật                                                               | Kiểm tra lại template đang gán cho khóa học        |
