# Quản lý học viên trong lớp (Student)

## Record of changes

_A - Add | M - Modify | D - Delete_

| Effective Date | Update Person | A,M,D | Change Description             | Version |
| -------------- | ------------- | ----- | ------------------------------ | ------- |
| May 25, 2026   | Lê Xuân Mai   | M     | Chuẩn hóa nội dung lên GitBook | 4.7.0   |

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** Admin, UpLMS Operator, CX

**Đường dẫn:** LMS → Class List → Chọn lớp học → Student
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Class
* **Chức năng chính:** Student
* **Module liên quan:** Class List, Class Detail, Course Content, Foundation Class, Revision Class, HubSpot Deal, Import Student
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Người dùng đã đăng nhập thành công vào hệ thống **UpLMS Operations**.
* Tài khoản có quyền truy cập module **Class** và quyền quản lý học viên trong lớp.
* Lớp học đã được tạo trên hệ thống.
* Học viên cần thêm đã tồn tại trên hệ thống.
{% endhint %}

{% hint style="info" %}
Trong thực tế, học viên thường được tự động thêm vào lớp sau khi Deal trên HubSpot chuyển sang trạng thái **Won**. Tài liệu này tập trung hướng dẫn các thao tác quản lý thủ công tại tab **Student** trong chi tiết lớp học.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Thêm học viên thủ công vào lớp</summary>

{% stepper %}
{% step %}
**Mở màn hình Class Detail**

Người dùng nhấp vào **tên lớp học** tại màn hình **Class List**. Hệ thống mở màn hình **Class Detail**.
{% endstep %}

{% step %}
**Mở tab Student**

Người dùng mở tab **Student** tại màn hình **Class Detail**.

<figure><img src="../.gitbook/assets/image (223)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Add Student**

Người dùng chọn **Add Student** tại tab **Student**. Hệ thống chuyển đến màn hình **Add Student**.

<figure><img src="../.gitbook/assets/image (224)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tìm kiếm học viên**

Người dùng tìm kiếm học viên tại khu vực tìm kiếm của màn hình **Add Student** nếu cần.

<figure><img src="../.gitbook/assets/image (225)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Tick chọn học viên**

Người dùng tick chọn học viên cần thêm vào lớp tại danh sách học viên.
{% endstep %}

{% step %}
**Chọn Add**

Người dùng chọn **Add** tại màn hình **Add Student**. Hệ thống thêm học viên đã chọn vào lớp và quay lại danh sách học viên của lớp.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Import học viên vào lớp</summary>

{% stepper %}
{% step %}
**Mở tab Student**

Người dùng mở tab **Student** trong màn hình **Class Detail**.
{% endstep %}

{% step %}
**Chọn Import Student**

Người dùng chọn **Import Student** tại tab **Student**. Hệ thống hiển thị popup **Import Student**.

<figure><img src="../.gitbook/assets/image (226)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Browse để chọn file**

Người dùng chọn **Browse** tại popup **Import Student** để chọn file từ thiết bị. Hệ thống chỉ chấp nhận file định dạng **.csv** hoặc **.xlsx**.

<figure><img src="../.gitbook/assets/image (227)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn đúng file import**

Người dùng chọn đúng file import cần tải lên. Mỗi lần import, hệ thống chỉ cho phép chọn **01 file**.
{% endstep %}

{% step %}
**Chọn Import**

Người dùng chọn **Import** tại popup **Import Student**. Hệ thống tải file lên và xử lý dữ liệu học viên trong file.
{% endstep %}

{% step %}
**Xem kết quả import**

Hệ thống hiển thị hộp thoại kết quả import: tên file, tổng số bản ghi, số học viên thêm thành công và số học viên thêm thất bại.
{% endstep %}

{% step %}
**Xem chi tiết lỗi (nếu cần)**

Người dùng chọn **View Log** để mở màn hình **Import Detail**. Các trường không hợp lệ được bôi đỏ và lý do lỗi hiển thị tại cột **Errors**.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xóa một học viên khỏi lớp</summary>

{% stepper %}
{% step %}
**Mở tab Student**

Người dùng mở tab **Student** trong màn hình **Class Detail**.
{% endstep %}

{% step %}
**Chọn Action → Delete**

Người dùng chọn **Action → Delete** tại dòng học viên cần xóa. Hệ thống hiển thị popup xác nhận xóa.

<figure><img src="../.gitbook/assets/image (228)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xác nhận xóa**

Người dùng chọn **Yes** tại popup xác nhận. Hệ thống xóa học viên khỏi lớp.

<figure><img src="../.gitbook/assets/image (229)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Xóa nhiều học viên khỏi lớp</summary>

{% stepper %}
{% step %}
**Mở tab Student**

Người dùng mở tab **Student** trong màn hình **Class Detail**.
{% endstep %}

{% step %}
**Tick chọn các học viên cần xóa**

Người dùng tick chọn các học viên cần xóa tại danh sách học viên.
{% endstep %}

{% step %}
**Chọn Delete Selected**

Người dùng chọn **Delete Selected** tại tab **Student**. Hệ thống hiển thị popup xác nhận xóa.

<figure><img src="../.gitbook/assets/image (230)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xác nhận xóa**

Người dùng chọn **Yes** tại popup xác nhận. Hệ thống xóa các học viên đã chọn khỏi lớp.

<figure><img src="../.gitbook/assets/image (231)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Cập nhật thời hạn học cho từng học viên</summary>

{% stepper %}
{% step %}
**Mở tab Student**

Người dùng mở tab **Student** trong màn hình **Class Detail**.
{% endstep %}

{% step %}
**Chọn Action → Update Duration**

Người dùng chọn **Action → Update Duration** tại dòng học viên cần cập nhật thời hạn học. Hệ thống hiển thị popup **Update Duration**.

<figure><img src="../.gitbook/assets/image (232)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Nhập thông tin thời hạn học**

Người dùng nhập **Start Date**, **End Date** và **Reason For Extension** tại popup **Update Duration**.

<figure><img src="../.gitbook/assets/image (233)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Save**

Người dùng chọn **Save** tại popup **Update Duration**. Hệ thống lưu thời hạn học mới cho học viên được chọn.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa cấu phần học của từng học viên</summary>

{% stepper %}
{% step %}
**Mở tab Student**

Người dùng mở tab **Student** trong màn hình **Class Detail**.
{% endstep %}

{% step %}
**Chọn Action → Edit Course Content**

Người dùng chọn **Action → Edit Course Content** tại dòng học viên cần chỉnh sửa nội dung học. Hệ thống mở màn hình **Edit Course Content** của học viên.

<figure><img src="../.gitbook/assets/image (234)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Điều chỉnh cấu phần học**

Người dùng tick thêm hoặc bỏ tick các cấu phần học cần điều chỉnh tại màn hình **Edit Course Content**.

<figure><img src="../.gitbook/assets/image (235)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Save**

Người dùng chọn **Save** tại màn hình **Edit Course Content**. Hệ thống lưu thay đổi và chỉ áp dụng cấu phần học đã chỉnh sửa cho học viên đó.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Cho học viên hoàn thành khóa Foundation</summary>

{% stepper %}
{% step %}
**Mở tab Student của lớp Lesson có gắn Foundation**

Người dùng mở tab **Student** trong màn hình **Class Detail** của lớp Lesson có gắn Foundation.
{% endstep %}

{% step %}
**Chọn Action → Allow Pass Foundation**

Người dùng chọn **Action → Allow Pass Foundation** tại dòng học viên chưa hoàn thành khóa Foundation. Hệ thống đánh dấu học viên hoàn thành khóa Foundation.

<figure><img src="../.gitbook/assets/image (236)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Hệ thống cập nhật trạng thái**

Hệ thống cập nhật trạng thái học Foundation của học viên. Sau khi cập nhật thành công, học viên có thể chuyển sang học khóa chính theo logic của hệ thống.
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Trong thực tế, học viên thường được tự động thêm vào lớp sau khi Deal trên HubSpot chuyển sang trạng thái **Won**; **Add Student** chỉ dùng khi cần thêm thủ công.
2. Người dùng cần có quyền quản lý học viên trong lớp để thêm, xóa, import hoặc cập nhật thông tin học viên.
3. File import học viên chỉ chấp nhận định dạng **.csv** hoặc **.xlsx**.
4. Đối với lớp **Foundation**, chỉ được thêm học viên có level trùng với level của lớp Foundation.
5. Khi thêm/xóa học viên khỏi lớp **Type = Lesson**, học viên đó cũng được thêm/xóa ở lớp **Foundation** và **Revision** gắn với lớp ban đầu.
6. Khi thêm/xóa học viên khỏi lớp **Type = Foundation** hoặc **Revision**, thao tác này không ảnh hưởng đến học viên của lớp **Lesson**.
7. Với lớp có **Duration = Flexible**, nếu học viên chưa kích hoạt khóa học thì không thể cập nhật thời hạn học của học viên đó.
8. Thời hạn học riêng của học viên có thể dài hơn hoặc ngắn hơn thời hạn mặc định của lớp.
9. Chỉnh sửa cấu phần học của từng học viên chỉ áp dụng cho học viên được chọn, không ảnh hưởng đến toàn bộ lớp.
10. Chỉ được xóa cấu phần học khỏi chương trình của học viên nếu học viên chưa học cấu phần đó; nếu đã học thì hệ thống không cho phép xóa.
11. Chức năng **Allow Pass Foundation** chỉ áp dụng khi lớp Lesson có gắn lớp Foundation và học viên cần được đánh dấu hoàn thành Foundation để học khóa chính.
{% endhint %}

### Công thức tính Duration mặc định của học viên

| Thành phần                                            | Công thức / Quy tắc                                                       |
| ----------------------------------------------------- | ------------------------------------------------------------------------- |
| **Start Date**                                        | Ngày sớm nhất giữa **Opening Date** và **Class Start Date**.              |
| **End Date**                                          | **Class End Date + Number of Extended Days** nếu lớp có gia hạn.          |
| **End Date trong trường hợp học viên đã chọn kỳ thi** | Có thể tính theo **Class Revision End Date** nếu học viên đã chọn kỳ thi. |

### Quy tắc chọn/bỏ chọn cấu phần học của học viên

<table data-search="false"><thead><tr><th>Thao tác</th><th>Quy tắc</th></tr></thead><tbody><tr><td><strong>Chọn/Bỏ chọn All</strong></td><td>Tất cả checkbox cấu phần học được tick hoặc bỏ tick.</td></tr><tr><td><strong>Chọn Section</strong></td><td>Tất cả Subsection, Unit, Activity, Quiz thuộc Section được chọn.</td></tr><tr><td><strong>Chọn Subsection</strong></td><td>Section, các Unit, Activity, Case Study liên quan đến Subsection được chọn.</td></tr><tr><td><strong>Chọn Unit</strong></td><td>Section, Subsection và các Activity liên quan đến Unit được chọn.</td></tr><tr><td><strong>Chọn Activity</strong></td><td>Section, Subsection và Unit chứa Activity đó được chọn.</td></tr><tr><td><strong>Bỏ chọn cấu phần học</strong></td><td>Cấu phần bị bỏ chọn sẽ không xuất hiện trong chương trình học của học viên và học viên không cần học cấu phần đó.</td></tr><tr><td><strong>Xóa cấu phần đã học</strong></td><td>Không được phép xóa khỏi chương trình học của học viên.</td></tr><tr><td><strong>Xóa cấu phần chưa học</strong></td><td>Được phép xóa khỏi chương trình học của học viên.</td></tr></tbody></table>

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                               | Nguyên nhân                                                           | Cách xử lý                                                           |
| ---------------------------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Không thêm được học viên vào lớp Foundation    | Học viên có level không trùng với level của lớp Foundation            | Chỉ thêm học viên có level trùng với lớp Foundation                  |
| Không import được học viên                     | File sai định dạng (không phải .csv/.xlsx) hoặc chọn nhiều hơn 1 file | Dùng file .csv/.xlsx, chọn 01 file mỗi lần; xem View Log để sửa lỗi  |
| Không cập nhật được thời hạn học               | Lớp Duration = Flexible và học viên chưa kích hoạt khóa học           | Chờ học viên kích hoạt khóa học rồi cập nhật thời hạn                |
| Không xóa được cấu phần học của học viên       | Học viên đã học cấu phần đó                                           | Chỉ được xóa cấu phần học viên chưa học                              |
| Xóa học viên ở lớp Lesson ảnh hưởng lớp khác   | Lớp Lesson đồng bộ với lớp Foundation/Revision gắn kèm                | Hiểu rõ ràng buộc: thao tác ở Lesson áp dụng cho Foundation/Revision |
| Không thực hiện được thao tác quản lý học viên | Tài khoản chưa có quyền quản lý học viên trong lớp                    | Liên hệ quản trị để được cấp quyền                                   |
