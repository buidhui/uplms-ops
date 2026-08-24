# Quản lý tài liệu trong lớp

## Record of changes

_A - Add | M - Modify | D - Delete_

| Effective Date | Update Person | A,M,D | Change Description             | Version |
| -------------- | ------------- | ----- | ------------------------------ | ------- |
| May 29, 2026   | Lê Xuân Mai   | M     | Chuẩn hóa nội dung lên GitBook | 4.7.0   |

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** Admin CX, CX Admin

**Đường dẫn:** Academic Management → Class → Class List → Class Detail → Resources
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Academic Management / Class
* **Chức năng chính:** Class Detail / Resources
* **Module liên quan:** Class List, Class Detail, Resources, Lesson, Student UpLMS, Teacher UpLMS
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Người dùng đã đăng nhập thành công vào hệ thống **UpLMS Operations**.
* Tài khoản có quyền truy cập module **Class**, quyền xem chi tiết lớp học và truy cập tab **Resources** trong Class Detail.
* Lớp học đã được tạo trên hệ thống.
* Nếu cần upload: có quyền tạo thư mục hoặc tải tài liệu lên hệ thống.
* Nếu cần chỉnh sửa/xóa/tải tài liệu: có quyền tương ứng với từng thao tác.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Xem danh sách học liệu</summary>

{% stepper %}
{% step %}
**Truy cập màn hình Class Resources**

Đường dẫn: Academic Management / Class / Class List / Class Detail / Resources.

<figure><img src="../.gitbook/assets/image (266)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xem thông tin tài liệu**

Các thông tin hiển thị trong danh sách:

<table data-search="false"><thead><tr><th>Cột thông tin</th><th>Mô tả</th></tr></thead><tbody><tr><td>File name</td><td>Tên tài liệu hoặc thư mục.</td></tr><tr><td>Size</td><td>Dung lượng tài liệu.</td></tr><tr><td>Date</td><td>Thời gian tạo mới hoặc chỉnh sửa tài liệu.</td></tr><tr><td>Owner</td><td>Người upload tài liệu.</td></tr><tr><td>Lesson</td><td>Buổi học được gắn với tài liệu.</td></tr><tr><td>Location</td><td>Vị trí lưu trữ của tài liệu trong thư mục Class Resources.</td></tr><tr><td>Access</td><td>Đối tượng được chia sẻ tài liệu (Student, Teacher).</td></tr></tbody></table>

Danh sách tài liệu được sắp xếp theo thời gian tạo giảm dần.
{% endstep %}

{% step %}
**Mở thư mục để xem nội dung bên trong**

Đối với các thư mục, chọn vào từng thư mục để xem các thư mục con/tài liệu thuộc thư mục đó.

<figure><img src="../.gitbook/assets/image (267)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tìm kiếm học liệu</summary>

{% stepper %}
{% step %}
**Nhập/chọn điều kiện tìm kiếm**

<figure><img src="../.gitbook/assets/image (268)" alt=""><figcaption></figcaption></figure>

Tìm kiếm theo các trường:

* **Search:** tên tài liệu.
* **Type:** loại tài liệu, chọn 1 giá trị (Media, Image, Sheet, Document, Presentation, Zip).
* **Access:** đối tượng chia sẻ, chọn 1 hoặc nhiều giá trị (Student, Teacher).
* **Lesson:** Tìm kiếm theo buổi học
{% endstep %}

{% step %}
**Áp dụng Search / Reset**

* Chọn **Search** để hiển thị tài liệu theo điều kiện tìm kiếm.
* Chọn **Reset** để xóa tất cả giá trị tìm kiếm và hiển thị danh sách theo thời gian tạo.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tạo mới thư mục / Tải tài liệu lên hệ thống</summary>

{% stepper %}
{% step %}
**Tạo mới thư mục**

Tại nơi muốn tạo thư mục mới, chọn **New Folder** → nhập tên thư mục → click **Save** để lưu.

<figure><img src="../.gitbook/assets/image (269)" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (270)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Mở hộp thoại Upload**

Tại vị trí muốn tải học liệu, chọn **Upload → Upload File/Media** và chọn hình thức Upload là File hoặc Media.

<figure><img src="../.gitbook/assets/image (271)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn tài liệu để tải lên**

<figure><img src="../.gitbook/assets/image (272)" alt=""><figcaption></figcaption></figure>

Tùy chọn Upload Media hay Upload File, người dùng upload loại tài liệu tương ứng:

* Kích cỡ tối đa của Media (video, file âm thanh) là **20GB**; mỗi lần upload chỉ được chọn 1 media.
* Kích cỡ tối đa của các tài liệu khác là **500MB**; được chọn tối đa 10 tài liệu/lần.

**TH1 — Tải tài liệu mới:** Tại màn hình Upload, ấn **Browse** để chọn tài liệu từ thiết bị.

**TH2 — Chọn tài liệu có sẵn từ hệ thống:** Tại màn hình Resource, chọn tài liệu để thêm vào lớp học. Có thể lọc theo Search, Course → Part → Chapter → Unit → Activity, Type, From/To date.
{% endstep %}

{% step %}
**Gắn tài liệu với buổi học**

Tại trường **Attach to the Lesson**, người dùng chọn buổi học cần gắn với tài liệu (có thể chọn nhiều buổi).
{% endstep %}

{% step %}
**Chọn đối tượng chia sẻ và quyền hiển thị**

Tại mục **Share Resource**, người dùng chọn đối tượng chia sẻ và quyền:

| Trường     | Mô tả                                                                                                                                  |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Student    | Mặc định được tích chọn. Tích chọn nếu muốn chia sẻ tài liệu cho học viên; tài liệu hiển thị trên Class Resource của UpLMS học viên.     |
| Teacher    | Mặc định được tích chọn. Tích chọn nếu muốn chia sẻ tài liệu cho giảng viên; tài liệu hiển thị trên Class Resource của UpLMS giảng viên. |
| Permission | **Viewer:** chỉ được xem trên UpLMS, không tải về. **Downloader:** được xem và tải tài liệu.                                             |

* Đối với tài liệu không phải mp3/mp4: mặc định quyền **Downloader**.
* Đối với Video/file âm thanh mp3: chỉ có quyền **Viewer**, không thể chuyển sang Downloader.
{% endstep %}

{% step %}
**Lưu tài liệu**

Sau khi chọn tài liệu và điền đầy đủ thông tin, chọn **Save** để tải lên hệ thống. Tài liệu tải lên thành công sẽ hiển thị thông báo Success và xuất hiện trong danh mục.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa tài liệu</summary>

{% stepper %}
{% step %}
**Đổi tên tài liệu/thư mục**

Tại danh sách tài liệu, chọn **Action → Rename** tại thư mục/tài liệu muốn đổi tên → nhập tên mới → chọn **Save**.

<figure><img src="../.gitbook/assets/image (273)" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (274)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Thay đổi thư mục lưu trữ (Move to Folder)**

Chọn **Action → Move to Folder** tại thư mục/tài liệu muốn di chuyển → chọn thư mục mới (chỉ chọn 1 thư mục) → chọn **Save** → chọn **Yes** tại hộp thoại xác nhận.

<figure><img src="../.gitbook/assets/image (275)" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (276)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chỉnh sửa buổi học, quyền và đối tượng hiển thị**

Chọn **Action → Edit** tại tài liệu muốn chỉnh sửa, sau đó điều chỉnh:

<figure><img src="../.gitbook/assets/image (277)" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (278)" alt=""><figcaption></figcaption></figure>

| Trường               | Mô tả                                                                                                           |
| -------------------- | --------------------------------------------------------------------------------------------------------------- |
| Attach to the lesson | Mặc định theo cấu hình hiện tại. Chọn buổi học cần gắn với tài liệu (có thể chọn nhiều buổi).                   |
| Student              | Mặc định theo cấu hình hiện tại. Tích chọn nếu muốn chia sẻ tài liệu cho học viên.                              |
| Teacher              | Mặc định theo cấu hình hiện tại. Tích chọn nếu muốn chia sẻ tài liệu cho giảng viên.                            |
| Permission           | **Viewer:** chỉ xem trên UpLMS, không tải. **Downloader:** xem và tải. Video/mp3 mặc định Viewer, không đổi được. |

Sau khi chỉnh sửa, chọn **Save** để lưu.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xóa thư mục/tài liệu</summary>

{% stepper %}
{% step %}
**Xóa 1 thư mục/tài liệu**

Chọn **Action → Delete** tại thư mục/tài liệu muốn xóa → chọn **Yes** tại hộp thoại xác nhận.

<figure><img src="../.gitbook/assets/image (279)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xóa nhiều thư mục/tài liệu**

Tick chọn các thư mục/tài liệu muốn xóa → chọn **Delete** → chọn **Yes** tại hộp thoại xác nhận.

<figure><img src="../.gitbook/assets/image (280)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tải tài liệu về thiết bị</summary>

{% stepper %}
{% step %}
**Tải một tài liệu**

Chọn **Action → Download File** tại tài liệu muốn tải.

<figure><img src="../.gitbook/assets/image (281)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tải nhiều tài liệu**

Tick chọn các tài liệu muốn tải → chọn **Download**.

<figure><img src="../.gitbook/assets/image (282)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Người dùng cần có quyền tương ứng để xem, tạo, chỉnh sửa, xóa, tải lên hoặc tải xuống tài liệu.
2. Danh sách tài liệu mặc định sắp xếp theo thời gian tạo giảm dần.
3. Kích cỡ tối đa của **Media** (video, file âm thanh) là **20GB**; mỗi lần upload chỉ chọn **1 media**.
4. Kích cỡ tối đa của các **tài liệu khác** là **500MB**; được chọn tối đa **10 tài liệu/lần**.
5. Tài liệu không phải mp3/mp4: mặc định quyền **Downloader**.
6. Video/file âm thanh mp3: chỉ có quyền **Viewer**, không thể chuyển sang **Downloader**.
7. Có thể gắn tài liệu với một hoặc nhiều buổi học qua trường **Attach to the Lesson**.
8. Khi di chuyển (Move to Folder), chỉ được chọn một thư mục đích.
{% endhint %}

{% hint style="info" %}
### Mẹo sử dụng

1. Nên tạo thư mục phân loại học liệu trước khi upload để dễ quản lý theo buổi học/chủ đề.
2. Khi chọn tài liệu có sẵn từ hệ thống, nên dùng bộ lọc Course → Part → Chapter → Unit → Activity để tìm đúng tài nguyên.
3. Kiểm tra kỹ đối tượng chia sẻ (Student/Teacher) và quyền (Viewer/Downloader) trước khi lưu để tránh chia sẻ nhầm.
4. Với video/mp3, lưu ý quyền mặc định là Viewer nên học viên/giảng viên không tải về được.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                               | Nguyên nhân                                          | Cách xử lý                                              |
| ---------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------- |
| Không upload được Media                        | File media vượt quá 20GB hoặc chọn nhiều hơn 1 media | Đảm bảo media ≤ 20GB và chỉ chọn 1 media mỗi lần        |
| Không upload được tài liệu                     | File vượt quá 500MB hoặc chọn quá 10 tài liệu/lần    | Đảm bảo file ≤ 500MB và chọn tối đa 10 tài liệu mỗi lần |
| Không chuyển được Video/mp3 sang Downloader    | Video/mp3 mặc định quyền Viewer                      | Đây là quy tắc hệ thống; Video/mp3 chỉ có quyền Viewer  |
| Không tìm thấy tài liệu                        | Sai điều kiện tìm kiếm/lọc                           | Kiểm tra lại bộ lọc, bấm Reset để về danh sách mặc định |
| Học viên/giảng viên không thấy tài liệu        | Chưa tích chọn đối tượng Student/Teacher khi chia sẻ | Mở Edit, tích đúng đối tượng chia sẻ rồi Save           |
| Không thực hiện được thao tác quản lý tài liệu | Tài khoản chưa có quyền tương ứng với thao tác       | Liên hệ quản trị để được cấp quyền                      |
