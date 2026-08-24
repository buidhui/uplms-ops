# Email và Thông báo hệ thống

## I. Thông tin chung

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Notification & Email
* **Module liên quan:** Recipients List
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Tài khoản có quyền truy cập nhóm chức năng **Notice & Email**.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Xem danh sách thông báo &#x26; Email</summary>

{% stepper %}
{% step %}
**Truy cập Notification List & Email List**

Tại thanh Menu, truy cập **Engagement & Support** → chọn **Notice & Email** → **Notification List & Email List**.

<figure><img src="../.gitbook/assets/image (365)" alt=""><figcaption></figcaption></figure>

Các trường thông tin hiển thị bao gồm:

* Số thứ tự
* Tiêu đề của Thông báo (Title)
* Loại Thông báo (Type) bao gồm:
  * Notification: thông báo được gửi trên hệ thống LMS Student.
  * Email: thông báo được gửi vào Email của học viên.
  * Noti & Email: thông báo được gửi trên hệ thống LMS Student và Email của học viên.
  * Pinned Notification: thông báo được ghim ở đầu trang tại giao diện học viên, sẽ hiển thị ở mọi màn hình.
* Send to: Nhóm người nhận thông báo
* Status:
  * Đối với thông báo có Type = Notification/Email/Noti & Email
    * Hẹn giờ gửi: thời gian gửi của thông báo được cài đặt trước, và chưa đến thời gian gửi thông báo.
    * Đã gửi: thông báo đã được gửi đi.
    * Hủy: hủy không gửi những thông báo đang có Status = ‘Hẹn giờ gửi’.
    * Thu hồi: thu hồi những thông báo có Status = ‘Đã gửi’ và có Type = ‘Notification’.
  * Đối với thông báo có Type = Pinned Notification
    * Hẹn giờ gửi: thời gian hiển thị của thông báo được cài đặt trước, và chưa đến thời gian hiển thị thông báo.
    * Đang hiển thị: thông báo đang hiển thị bên hệ thống UpLMS.
    * Hủy: hủy không hiển thị những thông báo đang có Status = ‘Hẹn giờ gửi’.
    * Thu hồi: thu hồi những thông báo có Status = ‘Đang hiển thị'.
    * Kết thúc: những thông báo đã hết thời gian hiển thị.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tìm kiếm thông báo</summary>

{% stepper %}
{% step %}
**Sử dụng bộ lọc để tìm kiếm**

<figure><img src="../.gitbook/assets/image (367)" alt=""><figcaption></figcaption></figure>

Tìm kiếm theo các trường:

* Tiêu đề của Thông báo (Title)
* Loại Thông báo (Type) bao gồm:
  * Notification: thông báo được gửi trên hệ thống LMS Student.
  * Email: thông báo được gửi vào Email của học viên.
  * Noti & Email: thông báo được gửi trên hệ thống LMS Student và Email của học viên.
  * Pinned Notification: thông báo được ghim ở đầu trang tại giao diện học viên, sẽ hiển thị ở mọi màn hình.
* Send to: Nhóm người nhận thông báo
* Trạng thái của thông báo (Status)
* Thứ tự sắp xếp (Sort by)
* Thời gian cập nhật (From Date – To Date)

Chọn **Search** để hiển thị các Thông báo theo điều kiện tìm kiếm.

Chọn **Reset** để xóa tất cả giá trị tìm kiếm và hiển thị danh sách theo thời gian tạo.

✅ Kết quả: Hiển thị danh sách các thông báo theo điều kiện bộ lọc:

<figure><img src="../.gitbook/assets/image (368)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xem chi tiết thông báo</summary>

{% stepper %}
{% step %}
**Click vào Tiêu đề thông báo để xem chi tiết**

<figure><img src="../.gitbook/assets/image (370)" alt=""><figcaption></figcaption></figure>

✅ Kết quả: Màn hình hiển thị chi tiết thông báo: Title, Type, Send to (với Notification/Email/Noti & Email), Action (thời gian gửi), Nội dung thông báo, Tài liệu đính kèm.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tạo mới Notification / Email / Noti &#x26; Email</summary>

{% stepper %}
{% step %}
**Mở màn hình tạo mới**

Tại màn hình danh sách thông báo, chọn **Create Notification**.

<figure><img src="../.gitbook/assets/image (373)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Điền thông tin thông báo**

Điền các thông tin (trường có **(\*)** là bắt buộc):

* **Title** (\*): Tiêu đề thông báo.
* **Pinned Notification** (\*): chọn **No**.
* **Type** (\*): được phép chọn 1 hoặc nhiều giá trị (Notification, Email, Noti & Email).
* **Send to** (\*): Nhóm người nhận.
* **Action** (\*):
  * **Hẹn giờ gửi:** cài đặt ngày giờ theo định dạng dd/mm/yyyy hh:mm với mm = 00 hoặc mm = 30.
  * **Gửi ngay:** gửi thông báo ngay tại thời điểm tạo.
* **Nội dung thông báo** (\*).
* **Tệp đính kèm** (áp dụng với Email): chọn Upload File từ thiết bị hoặc tài liệu có sẵn trên hệ thống.

<figure><img src="../.gitbook/assets/image (378)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Lưu thông tin**

Chọn **Save** để lưu thông báo. Hệ thống hiển thị thông báo tạo mới thành công.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tạo mới Pinned Notification</summary>

_**Pinned Notification là các thông báo được ghim tại đầu trang giao diện học viên UpLMS, hiển thị ở mọi màn hình.**_

{% stepper %}
{% step %}
**Mở màn hình tạo mới**

Tại mục Notification, chọn **Create Notification/Email**.

<figure><img src="../.gitbook/assets/image (379)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Điền thông tin**

* **Title** (\*): tên thông báo.
* **Pinned Notification** (\*): chọn **Yes**.
* **Action** (\*):
  * **Hẹn giờ gửi:** chọn thời gian bắt đầu và kết thúc hiển thị (dd/mm/yyyy hh:mm với mm = 00 hoặc mm = 30).
  * **Gửi ngay:** chỉ chọn thời gian kết thúc hiển thị (dd/mm/yyyy hh:mm với mm = 00 hoặc mm = 30).
* **Nội dung** (\*): Nội dung thông báo

Những trường có (\*) là những trường thông tin bắt buộc.

<figure><img src="../.gitbook/assets/image (380)" alt=""><figcaption></figcaption></figure>

⚠️ Khoảng thời gian xuất hiện của Pinned Notification mới tạo **không được trùng** với khoảng thời gian hiển thị của các Pinned Notification đã tạo trước đó. Nội dung hiển thị cho **Tất cả** học viên UpLMS nên không có lựa chọn Send to.
{% endstep %}

{% step %}
**Lưu thông tin**

Chọn **Save** để lưu.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa trạng thái thông báo</summary>

Áp dụng cho:

* Tất cả Thông báo có trạng thái **'Hẹn giờ gửi'**.
* Notification có trạng thái **'Đã gửi'**.
* Pinned Notification có trạng thái **'Đang hiển thị'**.

{% stepper %}
{% step %}
**Click vào giá trị trường Status để chọn trạng thái mới**

<figure><img src="../.gitbook/assets/image (381)" alt=""><figcaption></figcaption></figure>

Quy tắc:

* **Type = Notification / Email / Noti & Email:**
  * 'Hẹn giờ gửi' → 'Hủy': hủy gửi thông báo đến học viên.
  * 'Đã gửi' → 'Thu hồi': thu hồi Notification đã gửi.
  * Các trường hợp khác không được thay đổi.
* **Type = Pinned Notification:**
  * 'Hẹn giờ gửi' → 'Hủy': hủy hiển thị thông báo.
  * 'Đang hiển thị' → 'Thu hồi': thu hồi thông báo đang hiển thị.
  * Các trường hợp khác không được thay đổi.
{% endstep %}

{% step %}
**Xác nhận thay đổi trạng thái**

<figure><img src="../.gitbook/assets/image (382)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa thông tin khác của thông báo</summary>

Áp dụng cho các thông báo có trạng thái **'Hẹn giờ gửi'**.

{% stepper %}
{% step %}
**Mở thông báo cần chỉnh sửa**

Click vào **Tiêu đề** thông báo muốn chỉnh sửa hoặc click **Action** → chọn **Edit**.

<figure><img src="../.gitbook/assets/image (383)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Nhập giá trị mới**

Các trường có thể chỉnh sửa:

* **Title** (\*).
* **Pinned Notification:** không được chỉnh sửa.
* **Type** (\*): chỉ chỉnh sửa được với Notification / Email / Noti & Email.
* **Send to** (\*).
* **Action** (\*): Hẹn giờ gửi hoặc Gửi ngay.
* **Nội dung thông báo** (\*).
* **Tệp đính kèm:** kích cỡ tối đa 500MB/file.
{% endstep %}

{% step %}
**Lưu thông tin**

Chọn **Save** để lưu thông tin đã chỉnh sửa.
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Khoảng thời gian hiển thị của **Pinned Notification** mới không được trùng với khoảng thời gian của Pinned Notification đã tạo trước đó.
2. Chỉ thông báo có **Type = Notification** và **Status = 'Đã gửi'** mới được phép **Thu hồi** (không áp dụng cho Email).
3. Chỉ thông báo có **Status = 'Hẹn giờ gửi'** mới được **chỉnh sửa thông tin**.
4. Trường **Pinned Notification** không được chỉnh sửa sau khi tạo.
5. Kích cỡ file đính kèm tối đa: **500MB/file** (khi chỉnh sửa thông báo).
6. Định dạng thời gian gửi/hiển thị: dd/mm/yyyy hh:mm với phút **mm = 00 hoặc mm = 30**.
{% endhint %}

{% hint style="info" %}
### Mẹo sử dụng

1. **Tạo Nhóm người nhận** trước tại Recipients List, sau đó tạo Thông báo để gán Nhóm — tránh phải tạo Nhóm giữa luồng.
2. Sử dụng **Hẹn giờ gửi** để chuẩn bị thông báo trước, kiểm tra lại nội dung trước khi đến giờ gửi tự động.
3. Khi cần truyền thông quan trọng tới toàn bộ học viên, dùng **Pinned Notification** thay vì gửi nhiều Notification riêng lẻ.
4. Trước khi tạo Pinned Notification mới, kiểm tra danh sách Pinned đang **'Hẹn giờ gửi'** / **'Đang hiển thị'** để tránh trùng khoảng thời gian.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                                     | Nguyên nhân                                                        | Cách xử lý                                                                                          |
| ---------------------------------------------------- | ------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| Không tạo được Pinned Notification mới               | Khoảng thời gian hiển thị trùng với Pinned Notification đã tồn tại | Điều chỉnh Start time / End time để không bị trùng.                                                 |
| Không thể Thu hồi Email đã gửi                       | Tính năng Thu hồi chỉ áp dụng cho Type = Notification              | Chỉ áp dụng Thu hồi với Notification; Email không thể thu hồi sau khi gửi.                          |
| Không thể chỉnh sửa thông báo                        | Thông báo không ở trạng thái 'Hẹn giờ gửi'                         | Chỉ thông báo 'Hẹn giờ gửi' mới được chỉnh sửa thông tin; thông báo khác chỉ chỉnh sửa được Status. |
| Không lưu được thời gian Hẹn giờ gửi                 | Phút không hợp lệ (khác 00 và 30)                                  | Chỉnh lại định dạng dd/mm/yyyy hh:mm với phút mm = 00 hoặc mm = 30.                                 |
| Không chọn được Nhóm người nhận khi tạo Notification | Chưa có Nhóm người nhận trong hệ thống                             | Tạo Nhóm người nhận tại **Recipients List** trước, sau đó quay lại tạo thông báo.                   |
| Không tìm thấy thông báo trong danh sách             | Sai bộ lọc tìm kiếm                                                | Click **Reset** và tìm kiếm lại với điều kiện rộng hơn.                                             |
| Không upload được tệp đính kèm                       | File vượt quá 500MB                                                | Giảm kích thước file hoặc tách thành nhiều file nhỏ trước khi upload.                               |
