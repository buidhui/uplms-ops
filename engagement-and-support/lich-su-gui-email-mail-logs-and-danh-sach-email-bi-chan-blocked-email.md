---
hidden: true
---

# Lịch sử gửi Email của hệ thống

## Record of changes

_A - Add | M - Modify | D - Delete_

| Effective Date | Update Person | A,M,D | Change Description                | Version | Effective Date |
| -------------- | ------------- | ----- | --------------------------------- | ------- | -------------- |
| 30 May 2026    | Lê Thị Huế    | M     | Tái cấu trúc tài liệu lên gitbook | 1.5.0   | 30 May 2026    |

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** Admin, UpLMS Operator

**Đường dẫn:**

* Mail Logs: Engagement & Support → Mail Logs
* Blocked Mail: Engagement & Support → Blocked Mail
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Notification & Email — Mail Logs, Blocked Mail
* **Module liên quan:** Notification List & Email List (nguồn gốc các email được gửi)
* **Hệ thống tích hợp:** Hệ thống Email (gửi email tới học viên và phản hồi trạng thái bị chặn)
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Đã đăng nhập thành công vào hệ thống UpLMS Ops.
* Đã được cấp quyền tương ứng (xem Mail Logs, gửi lại email, xem và gỡ chặn Blocked Mail).
* Đã có email được gửi từ hệ thống để hiển thị lịch sử trong Mail Logs.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Xem danh sách Mail Logs</summary>

**Truy cập Mail Log List**

Tại thanh Menu, truy cập **Engagement & Support** → click vào **Mail Logs**.

<figure><img src="../.gitbook/assets/image (384)" alt=""><figcaption></figcaption></figure>

Các trường thông tin hiển thị gồm:

* **Số thứ tự**
* **Title:** Tiêu đề của Mail.
* **Receiver:** Người nhận.
* **Status:** Trạng thái gửi của Mail.
  * **Đã gửi:** Mail đã được gửi thành công cho học viên.
  * **Thất bại:** Mail chưa được gửi cho học viên.
* **Sent time:** Thời gian gửi Mail.

</details>

<details>

<summary>Tìm kiếm Mail</summary>

**Sử dụng bộ lọc tìm kiếm**

Tìm kiếm theo các trường: Người nhận, Loại Mail (Action), Trạng thái (Status), From Date – To Date.

* Chọn **Search** để hiển thị các Mail theo điều kiện tìm kiếm.
* Chọn **Reset** để xóa các giá trị tìm kiếm và hiển thị danh sách theo thời gian tạo.

<figure><img src="../.gitbook/assets/image (385)" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Xem chi tiết Mail Logs</summary>

**Click vào Title Mail để xem chi tiết**

Tại danh sách Mail Logs, click vào **Title Mail** để xem chi tiết.

<figure><img src="../.gitbook/assets/image (1369).png" alt=""><figcaption></figcaption></figure>

Màn hình hiển thị thông tin chi tiết của Mail:

<figure><img src="../.gitbook/assets/image (386)" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Resend Email</summary>

**Gửi lại email cho người nhận**

Tại màn hình danh sách Mail Logs, chọn **Action** → chọn **Resend** để gửi lại email cho người nhận.

<figure><img src="../.gitbook/assets/image (387)" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Xem danh sách Email bị chặn</summary>

**Truy cập Blocked Mail**

Tại thanh Menu, truy cập **Engagement & Support** → chọn **Blocked Mail**.

<figure><img src="../.gitbook/assets/image (388)" alt=""><figcaption></figcaption></figure>

Màn hình hiển thị danh sách Email bị chặn với các thông tin:

* **Địa chỉ email**
* **Date:** Thời gian email được gửi đi.
* **Reason:** Lý do email bị chặn.

</details>

<details>

<summary>Tìm kiếm Email bị chặn</summary>

**Sử dụng bộ lọc tìm kiếm**

<figure><img src="../.gitbook/assets/image (389)" alt=""><figcaption></figcaption></figure>

Tại danh sách Blocked Mail, sử dụng bộ lọc để tìm kiếm email.

* Chọn **Search** để hiển thị kết quả.
* Chọn **Reset** để xóa các giá trị tìm kiếm.

</details>

<details>

<summary>Gỡ chặn Email bị chặn</summary>

**Thực hiện Unblock email**

Tại danh sách Blocked Mail, truy cập **Action** → chọn **Unblock** để bỏ chặn email.

<figure><img src="../.gitbook/assets/image (390)" alt=""><figcaption></figcaption></figure>

✅ Kết quả: Bỏ chặn email thành công, các thông báo có thể được gửi tới địa chỉ email này.

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. **Mail Logs** chỉ ghi nhận các email **đã được hệ thống gửi đi** — không bao gồm Notification trên LMS Student.
2. Mail có trạng thái **'Thất bại'** thường do email người nhận sai, bị bounce, hoặc đã bị chặn — cần kiểm tra **Blocked Mail** để xác định nguyên nhân.
3. Khi **Resend** email, hệ thống sẽ gửi lại nội dung gốc đã ghi nhận trong Mail Logs cho cùng người nhận.
4. Email bị chặn (Blocked Mail) là email **không thể gửi đến học viên** do hệ thống email từ chối (bounce, spam, invalid, v.v.).
5. Sau khi **Unblock** một email, các thông báo tiếp theo có thể được gửi đến địa chỉ này nhưng vẫn có thể bị chặn lại nếu nguyên nhân chưa được xử lý.
{% endhint %}

{% hint style="info" %}
### Mẹo sử dụng

1. **Kiểm tra Mail Logs định kỳ** để phát hiện sớm các email gửi Thất bại và xử lý kịp thời.
2. Khi phát hiện email Thất bại, **đối chiếu với Blocked Mail** để xác định email đó có bị chặn hay không.
3. Sử dụng bộ lọc theo **Status = Thất bại** + **From Date – To Date** để lọc nhanh các email cần xử lý.
4. Theo dõi **Blocked Mail** để cảnh báo học viên về email bị chặn (nếu cần) — đề nghị học viên cập nhật email khác hoặc kiểm tra hộp thư.
5. Trước khi **Unblock** email, kiểm tra **Reason** để biết nguyên nhân và đảm bảo đã được xử lý trước khi gửi lại.
6. Đối với email Thất bại tạm thời (lỗi server, timeout), dùng chức năng **Resend** để gửi lại mà không cần tạo thông báo mới.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                                | Nguyên nhân                                                       | Cách xử lý                                                                                              |
| ----------------------------------------------- | ----------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Mail có Status = 'Thất bại' trong Mail Logs     | Email người nhận sai, bị bounce, hoặc bị chặn                     | Kiểm tra Blocked Mail; xác nhận lại địa chỉ email của học viên; dùng Resend sau khi xử lý nguyên nhân.  |
| Resend email không thành công                   | Email vẫn còn trong danh sách Blocked Mail                        | Vào **Blocked Mail**, click **Unblock** cho địa chỉ email tương ứng, sau đó Resend lại.                 |
| Không tìm thấy Mail trong Mail Logs             | Sai bộ lọc tìm kiếm hoặc Mail nằm ngoài khoảng thời gian lọc      | Click **Reset** và tìm kiếm lại với điều kiện rộng hơn (mở rộng From Date – To Date).                   |
| Không tìm thấy email trong Blocked Mail         | Sai bộ lọc tìm kiếm                                               | Click **Reset** và tìm lại; kiểm tra chính tả địa chỉ email.                                            |
| Email vừa được Unblock vẫn không nhận được mail | Nguyên nhân gốc chưa được xử lý (hộp thư đầy, email không hợp lệ) | Kiểm tra **Reason** trong Blocked Mail trước khi Unblock; liên hệ học viên xác nhận hộp thư.            |
| Email bị chặn liên tục sau khi Unblock          | Hệ thống email vẫn đánh dấu spam hoặc bounce                      | Đề nghị học viên kiểm tra hộp thư rác, whitelist domain gửi; cân nhắc cập nhật email khác cho học viên. |
| Không thể Resend hoặc Unblock                   | Người dùng không có quyền tương ứng                               | Liên hệ Admin để được cấp quyền.                                                                        |
