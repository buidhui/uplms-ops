# Tạo lớp học

## I. Thông tin chung

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Class
* **Module liên quan:** Course, Exam, Student, Mentor, Foundation Class
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Tài khoản có quyền truy cập nhóm chức năng **Class.**
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Tạo lớp học</summary>

{% stepper %}
{% step %}
**Chọn Create Class tại Danh sách lớp học**

<figure><img src="../../.gitbook/assets/image (103) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Điền thông tin**

<figure><img src="../../.gitbook/assets/image (104) (1).png" alt=""><figcaption></figcaption></figure>

Các trường thông tin:

* Name (bắt buộc): tên lớp học.
* Code: mã lớp.
* Construction Mode (bắt buộc): hình thức lớp, mặc định là Online.
* Type (bắt buộc): loại lớp, mặc định là Lesson

{% hint style="info" %}
Người dùng chỉ có thể tạo các lớp có Type là **Lesson.** Lớp **Foundation** sẽ do hệ thống tạo tự động khi khóa học Normal thuộc Lesson Class có gắn với Foundation Course.
{% endhint %}

* Số học viên tối đa
* Duration: thời gian lớp diễn ra

| Duration     | Mô tả                                                                         |
| ------------ | ----------------------------------------------------------------------------- |
| **Fixed**    | Lớp diễn ra trong khoảng Start Date - End Date.                               |
| **Flexible** | Lớp học diễn ra trong N ngày, tính kể từ ngày học viên chọn bắt đầu khóa học. |
{% endstep %}

{% step %}
**Gán khóa học cho lớp**

Chọn Add Course → Chọn khóa muốn gán → Add

<figure><img src="../../.gitbook/assets/image (105) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Save để lưu**
{% endstep %}

{% step %}
**Thêm học viên vào lớp (Optional)**

Sau khi lưu thông tin lớp, nhân sự vận hành có thể thêm học viên ngay ở bước tạo lớp, hoặc thêm sau theo hướng dẫn [quan-ly-hoc-vien-student.md](../../user-management/quan-ly-hoc-vien-student.md "mention")

<figure><img src="../../.gitbook/assets/image (106) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa lớp học</summary>

*
* Cách 1:

<figure><img src="../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

* Cách 2:

<figure><img src="../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

Các trường được phép chỉnh sửa phụ thuộc vào loại lớp, hình thức học và trạng thái học tập của học viên trong lớp.

**Lớp Foundation:**

| Tình trạng lớp           | Quy tắc chỉnh sửa                                        |
| ------------------------ | -------------------------------------------------------- |
| **Đã có học viên học**   | Chỉ được chỉnh sửa Name, Code, Số học viên tối đa.       |
| **Chưa có học viên học** | Được chỉnh sửa tất cả thông tin, ngoại trừ Type, Course. |

**Lớp Lesson:**

| Tình trạng lớp                                                | Quy tắc chỉnh sửa                                             |
| ------------------------------------------------------------- | ------------------------------------------------------------- |
| **Chưa có học viên học**                                      | Được chỉnh sửa tất cả thông tin.                              |
| **Đã có học viên nhưng lớp chưa bắt đầu / học viên chưa học** | Không được chỉnh sửa Status, Construction Mode, Type, Course. |
| **Đã có học viên đang học hoặc lớp đã bắt đầu**               | Không được chỉnh sửa Status, Construction Mode, Type, Course. |



</details>

<details>

<summary>Tạo lớp hàng loạt (Import)</summary>



</details>

## III. Lưu ý & Quy tắc nghiệp vụ

<details>

<summary>Tạo lớp hàng loạt (Import)</summary>

{% stepper %}
{% step %}
**Chọn Import Class tại Danh sách lớp học**

<figure><img src="../../.gitbook/assets/image (113) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn file danh sách lớp cần Import**

<figure><img src="../../.gitbook/assets/image (114) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Nên tải **file mẫu** trước khi nhập dữ liệu import; dữ liệu cần tuân thủ đúng cấu trúc và định dạng của template.
{% endhint %}
{% endstep %}

{% step %}
**Xem kết quả Import**

Hộp thoại kết quả import hiển thị sau khi xử lý file:

* Tên file
* Tổng số bản ghi
* Số lớp tạo thành công và số lớp tạo thất bại
{% endstep %}

{% step %}
**Xem View Log**

Chọn **View Log** tại hộp thoại kết quả import để xem chi tiết trạng thái từng bản ghi.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa thông tin lớp học</summary>

* Lớp học có trạng thái **Ended** không được chỉnh sửa.
* Quy tắc chỉnh sửa theo loại lớp

Lớp Foundation:

| Tình trạng lớp           | Quy tắc chỉnh sửa                                        |
| ------------------------ | -------------------------------------------------------- |
| **Đã có học viên học**   | Chỉ được chỉnh sửa Name, Code, Số học viên tối đa.       |
| **Chưa có học viên học** | Được chỉnh sửa tất cả thông tin, ngoại trừ Type, Course. |

Lớp Lesson:

| Tình trạng lớp                                                | Quy tắc chỉnh sửa                                             |
| ------------------------------------------------------------- | ------------------------------------------------------------- |
| **Chưa có học viên học**                                      | Được chỉnh sửa tất cả thông tin.                              |
| **Đã có học viên nhưng lớp chưa bắt đầu / học viên chưa học** | Không được chỉnh sửa Status, Construction Mode, Type, Course. |
| **Đã có học viên đang học hoặc lớp đã bắt đầu**               | Không được chỉnh sửa Status, Construction Mode, Type, Course. |

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Chức năng **Import Class** dùng để tạo nhiều lớp học cùng lúc.
2. File import chỉ chấp nhận định dạng **.csv** hoặc **.xlsx**.
3. Mỗi lần import chỉ được chọn **1 file**.
4. Các bản ghi hợp lệ sẽ được hệ thống tạo lớp thành công; các bản ghi không hợp lệ sẽ không được tạo lớp và được ghi nhận lỗi trong log.
5. Các trường không hợp lệ trong file import được bôi đỏ tại màn hình chi tiết log; lý do lỗi hiển thị tại cột **Errors**.
{% endhint %}

{% hint style="info" %}
### Mẹo sử dụng

1. Sau khi import, nên mở **View Log** để xử lý các dòng bị bôi đỏ (lý do lỗi) rồi import lại.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                     | Nguyên nhân                                    | Cách xử lý                                                           |
| ------------------------------------ | ---------------------------------------------- | -------------------------------------------------------------------- |
| Không chọn được file để import       | File sai định dạng (không phải .csv/.xlsx)     | Chuyển file về định dạng .csv hoặc .xlsx rồi chọn lại                |
| Không import được nhiều file một lúc | Mỗi lần import chỉ cho phép 01 file            | Chọn từng file một để import                                         |
| Một số bản ghi import thất bại       | Dữ liệu không đúng cấu trúc/định dạng template | Mở View Log, sửa các trường bị bôi đỏ theo cột Errors rồi import lại |
| Dữ liệu lệch cột sau khi import      | Dùng sai phiên bản file mẫu                    | Tải lại file mẫu mới nhất và nhập đúng cấu trúc                      |
| Không thực hiện được import          | Tài khoản chưa có quyền import lớp học         | Liên hệ quản trị để được cấp quyền import lớp học                    |
