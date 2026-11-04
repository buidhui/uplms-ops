# Chỉnh sửa thông tin lớp học

## Record of changes

_A - Add | M - Modify | D - Delete_

| Effective Date | Update Person | A,M,D | Change Description             | Version |
| -------------- | ------------- | ----- | ------------------------------ | ------- |
| May 25, 2026   | Lê Xuân Mai   | M     | Chuẩn hóa nội dung lên GitBook | 4.7.0   |

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** Admin, UpLMS Operator, Academic/CX User

**Đường dẫn:** Class → Class List → (Action → Edit) hoặc Class Detail → Settings
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Class
* **Chức năng chính:** Edit Class Info
* **Module liên quan:** Class List, Class Detail, Course, Exam, Classroom, Facility, Hybrid Class, Foundation Class
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Người dùng đã đăng nhập thành công vào hệ thống **UpLMS Operations**.
* Tài khoản có quyền truy cập module **Class**.
* Tài khoản có quyền chỉnh sửa lớp học.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Chỉnh sửa thông tin cơ bản của lớp học</summary>

{% stepper %}
{% step %}
**Chọn Action → Edit**

Người dùng chọn **Action → Edit** tại lớp cần chỉnh sửa trên màn hình **Class List**. Hệ thống mở màn hình chỉnh sửa thông tin lớp học.

<figure><img src="../.gitbook/assets/image (215)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chỉnh sửa các thông tin được phép**

Người dùng chỉnh sửa các thông tin được phép tại màn hình **Edit Class Info**. Các trường được phép chỉnh sửa phụ thuộc vào loại lớp, hình thức học và trạng thái học tập của học viên trong lớp.

<figure><img src="../.gitbook/assets/image (217)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn Save**

Người dùng chọn **Save** tại màn hình **Edit Class Info**. Hệ thống lưu thông tin mới và cập nhật dữ liệu lớp học.

<figure><img src="../.gitbook/assets/image (219)" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa thông tin từ màn Class Detail</summary>

{% stepper %}
{% step %}
**Mở màn hình Class Detail**

Người dùng nhấp vào **tên lớp học** tại màn hình **Class List**. Hệ thống mở màn hình **Class Detail**.
{% endstep %}

{% step %}
**Chọn Edit Class Info tại tab Overview**

Người dùng chọn **Edit Class Info** tại tab **Overview**. Hệ thống mở màn hình chỉnh sửa thông tin lớp học.

<figure><img src="../.gitbook/assets/image (220)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Cập nhật thông tin và Save**

Người dùng cập nhật thông tin cần thay đổi tại màn hình **Edit Class Info**, sau đó chọn **Save** để lưu.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa thông tin lớp tại tab Settings</summary>

{% stepper %}
{% step %}
**Mở màn hình Class Detail**

Người dùng nhấp vào **tên lớp học** tại màn hình **Class List**.

<figure><img src="../.gitbook/assets/image (221)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn tab Settings**

Người dùng chọn tab **Settings** tại màn hình **Class Detail**. Hệ thống hiển thị các thông tin lớp học có thể chỉnh sửa.
{% endstep %}

{% step %}
**Cập nhật thông tin và Save**

Người dùng cập nhật thông tin cần thay đổi tại tab **Settings**, sau đó chọn **Save** để lưu thay đổi.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa Classroom</summary>

{% stepper %}
{% step %}
**Chọn trường Classroom**

Người dùng chọn trường **Classroom** tại màn hình **Edit Class Info**. Hệ thống chuyển đến màn hình chọn phòng học.
{% endstep %}

{% step %}
**Tìm kiếm phòng học**

Người dùng tìm kiếm phòng học bằng **Search** hoặc bộ lọc **Type** nếu cần. Hệ thống hiển thị danh sách phòng học phù hợp với điều kiện của lớp.

<figure><img src="../.gitbook/assets/image (222)" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Chọn phòng học và Add**

Người dùng chọn một phòng học trong danh sách, sau đó chọn **Add** để thêm phòng học vào lớp. Hệ thống quay lại màn hình chỉnh sửa lớp và hiển thị phòng học đã chọn.
{% endstep %}

{% step %}
**Nhập lại Link Meeting (nếu Live Online / Hybrid)**

Người dùng nhập lại **Link Meeting** nếu lớp có Construction Mode là **Live Online** hoặc **Hybrid**. Khi chỉnh sửa Classroom của các lớp này, hệ thống tự động làm rỗng Link Meeting và yêu cầu nhập lại.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa Create Hybrid Class đối với lớp Lesson</summary>

{% stepper %}
{% step %}
**Mở màn hình Edit Class Info của lớp Lesson**

Người dùng mở màn hình **Edit Class Info** của lớp Lesson cần chỉnh sửa.
{% endstep %}

{% step %}
**Tick / bỏ tick Create Hybrid Class**

Người dùng tick hoặc bỏ tick checkbox **Create Hybrid Class**. Checkbox này chỉ áp dụng cho lớp **Lesson** có Construction Mode là **Offline** hoặc **Blended**.
{% endstep %}

{% step %}
**Nhập Hybrid Class Code (nếu tick)**

Người dùng nhập **Hybrid Class Code** nếu tick checkbox **Create Hybrid Class**. Hệ thống tạo bổ sung lớp Hybrid sau khi lưu thành công.
{% endstep %}

{% step %}
**Nhập Block Reason (nếu bỏ tick)**

Người dùng nhập **Block Reason** nếu bỏ tick checkbox **Create Hybrid Class** khi lớp Hybrid đã được tạo trước đó. Hệ thống khóa lớp Hybrid đã tạo và làm rỗng thông tin Classroom, Link Meeting của lớp Hybrid.
{% endstep %}

{% step %}
**Chọn Save**

Người dùng chọn **Save** để lưu thay đổi.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa Class Owner và CX Admin</summary>

{% stepper %}
{% step %}
**Mở màn hình Edit Class Info**

Người dùng mở màn hình **Edit Class Info** của lớp cần chỉnh sửa.
{% endstep %}

{% step %}
**Nhập và chọn Class Owner**

Người dùng nhập tên hoặc email nhân viên tại trường **Class Owner**, sau đó chọn nhân viên phù hợp trong danh sách gợi ý.
{% endstep %}

{% step %}
**Nhập và chọn CX Admin**

Người dùng nhập tên hoặc email nhân viên tại trường **CX Admin**, sau đó chọn nhân viên phù hợp trong danh sách gợi ý.
{% endstep %}

{% step %}
**Chọn Save**

Người dùng chọn **Save** để lưu thông tin Class Owner và CX Admin.
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Lớp học có trạng thái **Ended** không được chỉnh sửa.
2. Việc chỉnh sửa lớp học phụ thuộc vào **Construction Mode**, **Type** và tiến độ học của học viên trong lớp.
3. Lớp có Construction Mode là **Hybrid** chỉ được chỉnh sửa: Class name, Class code, Classroom, Link meeting, Description. Các thông tin còn lại đồng bộ từ lớp gốc.
4. Người dùng luôn có thể chỉnh sửa **Class Owner** và **CX Admin** bất kể trạng thái lớp học.
5. Hệ thống chặn chỉnh sửa **Class Owner** và **CX Admin** đối với lớp **Foundation** và **Hybrid** (đồng bộ từ lớp chính).
6. Khi chuyển trạng thái lớp Lesson sang **Block**, lớp Hybrid gắn với lớp đó (nếu có) cũng chuyển sang **Block**.
7. Nếu nhập **Number of Extended Days = 0** hoặc để trống, hệ thống xóa dữ liệu **Number of Extended Days** và **Reason For Extension**, duration học viên quay lại cách tính mặc định.
{% endhint %}

### Quy tắc chỉnh sửa theo loại lớp

**Lớp Hybrid**

| Nhóm thông tin           | Quy tắc                                                       |
| ------------------------ | ------------------------------------------------------------- |
| Thông tin được sửa       | Class name, Class code, Classroom, Link meeting, Description. |
| Thông tin không được sửa | Các thông tin còn lại vì được đồng bộ từ lớp gốc.             |

**Lớp Foundation**

| Tình trạng lớp           | Quy tắc chỉnh sửa                                                                       |
| ------------------------ | --------------------------------------------------------------------------------------- |
| **Đã có học viên học**   | Chỉ được chỉnh sửa Name, Code, Area, Số học viên tối đa, Lecturer, Mentor, Description. |
| **Chưa có học viên học** | Được chỉnh sửa tất cả thông tin, ngoại trừ Type, Course, Class Owner, CX Admin.         |

**Lớp Trial / Revision / Lesson**

| Tình trạng lớp                                                | Quy tắc chỉnh sửa                                                                                                                                                    |
| ------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Chưa có học viên học**                                      | Được chỉnh sửa tất cả thông tin.                                                                                                                                     |
| **Đã có học viên nhưng lớp chưa bắt đầu / học viên chưa học** | Không được chỉnh sửa Status, Construction Mode, Facility, Type, Course, Exam.                                                                                        |
| **Đã có học viên đang học hoặc lớp đã bắt đầu**               | Không được chỉnh sửa Status, Construction Mode, Facility, Type, Create Hybrid Class, Course, Exam, Standard Schedule, Number of Extended Days, Reason For Extension. |

### Quy tắc chọn Classroom

| Điều kiện                                    | Quy tắc                                                                                     |
| -------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **Construction Mode = Live Online / Hybrid** | Chỉ hiển thị phòng học ảo có Mode = Virtual.                                                |
| **Construction Mode = Offline / Blended**    | Chỉ hiển thị phòng học vật lý có Mode = Physical tại Facility của lớp.                      |
| **Status phòng học**                         | Chỉ hiển thị phòng học có Status = Active.                                                  |
| **Sức chứa phòng học vật lý**                | Số học viên của lớp phải nhỏ hơn sức chứa của phòng.                                        |
| **Trùng lịch phòng học**                     | Chỉ hiển thị các phòng có số buổi trùng lịch với lịch học tự động nhỏ hơn hoặc bằng 3 buổi. |
| **Sắp xếp phòng học**                        | Danh sách phòng học được sort theo số lượng buổi tự động bị trùng.                          |
| **Lớp chưa có lịch phòng học**               | Không hiển thị giá trị phòng học nào.                                                       |

### Quy tắc chỉnh sửa Create Hybrid Class

| Thao tác                                        | Quy tắc                                                                       |
| ----------------------------------------------- | ----------------------------------------------------------------------------- |
| **Bỏ tick Create Hybrid Class**                 | Lớp Hybrid đã được tạo trước đó sẽ bị khóa. Người dùng cần nhập Block Reason. |
| **Bỏ tick Create Hybrid Class**                 | Classroom và Link Meeting của lớp Hybrid sẽ được làm rỗng.                    |
| **Tick Create Hybrid Class**                    | Hệ thống tạo bổ sung lớp Hybrid sau khi lưu thành công.                       |
| **Edit Type = Trial/Revision**                  | Lớp Hybrid đã được tạo trước đó sẽ tự động bị xóa.                            |
| **Edit Construction Mode = Online/Live Online** | Lớp Hybrid đã được tạo trước đó sẽ tự động bị xóa.                            |
| **Lớp có Status = Block**                       | Checkbox Create Hybrid Class bị disable.                                      |

### Quy tắc gửi thông báo kiểm tra Class Owner/CX Admin

Hệ thống gửi mail và tạo ticket trên HubSpot cho **CX Supervisor** theo từng BU để kiểm tra lại thông tin **Class Owner/CX Admin**.

| Điều kiện                              | Thời điểm gửi mail/tạo ticket                      |
| -------------------------------------- | -------------------------------------------------- |
| **Start Date - Create Date >= 7 ngày** | Gửi lúc 9:00 sáng, trước 7 ngày so với Start Date. |
| **Start Date - Create Date < 7 ngày**  | Gửi lúc 9:00 sáng ngày hôm sau.                    |

Đối với các ticket được tạo ra do học viên chọn kỳ thi trên UpLMS, hệ thống tự động assign ticket về **Class Owner** của lớp chính.

{% hint style="info" %}
### Mẹo sử dụng

1. Trước khi chỉnh sửa lớp, nên kiểm tra **Type**, **Construction Mode** và trạng thái học tập của học viên để biết trường nào được phép chỉnh sửa.
2. Với lớp Hybrid, phần lớn thông tin được đồng bộ từ lớp gốc nên không chỉnh sửa trực tiếp được.
3. Khi đổi Classroom cho lớp Live Online hoặc Hybrid, cần chuẩn bị sẵn Link Meeting mới vì hệ thống sẽ làm rỗng link cũ.
4. Với các lớp đã bắt đầu, nên hạn chế thay đổi thông tin lịch học hoặc thời gian học để tránh ảnh hưởng đến học viên.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                          | Nguyên nhân                                                     | Cách xử lý                                                            |
| ----------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------------- |
| Không chỉnh sửa được lớp học              | Lớp có trạng thái **Ended**                                     | Lớp Ended không được chỉnh sửa; kiểm tra lại trạng thái lớp           |
| Một số trường bị khóa, không sửa được     | Phụ thuộc Construction Mode, Type và tiến độ học của học viên   | Đối chiếu quy tắc chỉnh sửa theo loại lớp ở mục III                   |
| Không sửa được Class Owner / CX Admin     | Lớp là **Foundation** hoặc **Hybrid** (đồng bộ từ lớp chính)    | Chỉnh sửa Class Owner/CX Admin tại lớp chính                          |
| Link Meeting bị mất sau khi đổi Classroom | Hệ thống tự làm rỗng Link Meeting với lớp Live Online/Hybrid    | Nhập lại Link Meeting mới sau khi đổi Classroom                       |
| Không chọn được phòng học mong muốn       | Phòng không thỏa điều kiện (Mode, Status, sức chứa, trùng lịch) | Chọn phòng đúng Mode/Active, đủ sức chứa, ít trùng lịch               |
| Checkbox Create Hybrid Class bị disable   | Lớp có Status = Block                                           | Bỏ trạng thái Block trước nếu cần bật lại Create Hybrid Class         |
| Mất dữ liệu gia hạn sau khi lưu           | Nhập Number of Extended Days = 0 hoặc để trống                  | Nhập số ngày gia hạn > 0 kèm Reason For Extension nếu cần giữ gia hạn |
