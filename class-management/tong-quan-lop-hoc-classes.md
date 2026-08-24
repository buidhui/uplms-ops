---
description: (Tổng quan)
---

# Tổng quan lớp học (Classes)

#### Module này dùng để làm gì?

Module Class là nơi đội ngũ CX (Vận hành lớp học) tạo và quản lý toàn bộ vòng đời của một lớp học — từ lúc lớp được mở ra cho đến khi kết thúc. Nếu module Course là nơi xây dựng "nội dung cần dạy", thì module Class là nơi quyết định "ai dạy, ai học, học lúc nào và học ở đâu".

Mọi hoạt động diễn ra trong lớp — từ giảng viên được phân công, học viên được xếp vào lớp, bài kiểm tra được giao, cho đến kỳ thi chính thức, đều được quản lý tập trung tại đây.

***

#### 3 bước vận hành chính

<figure><img src="../.gitbook/assets/image (857).png" alt=""><figcaption></figcaption></figure>

### **Business Rule:**

<details>

<summary>Quy tắc chung về Class</summary>

| Mã rule      | Business Rule                                                                                                                                                                  |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| BR-CLASS-001 | Người dùng chỉ được truy cập module **Class** khi đã đăng nhập thành công vào hệ thống UpLMS Operations.                                                                       |
| BR-CLASS-002 | Người dùng chỉ được xem danh sách lớp học nếu tài khoản có quyền truy cập màn hình **Class List**.                                                                             |
| BR-CLASS-003 | Người dùng chỉ được tạo, chỉnh sửa, import hoặc thao tác với lớp học nếu có quyền tương ứng.                                                                                   |
| BR-CLASS-004 | Danh sách lớp học mặc định được hiển thị theo **thời gian tạo giảm dần**.                                                                                                      |
| BR-CLASS-005 | Người dùng có thể tìm kiếm/lọc lớp học theo tên/mã lớp, Code, Program, Subject, Status, Facility, Construction Mode, Type, Class Owner, CX Admin, Sort by và khoảng thời gian. |
| BR-CLASS-006 | Nút **Reset** chỉ xóa điều kiện tìm kiếm/lọc, không xóa dữ liệu lớp học.                                                                                                       |
| BR-CLASS-007 | Người dùng có thể xem chi tiết lớp học bằng cách nhấp vào **tên lớp học** tại màn hình Class List.                                                                             |
| BR-CLASS-008 | Màn hình chi tiết lớp học gồm các tab: **Overview, Settings, Calendar, Progress, Students, Mentors, Teachers, Examinations, Marks, Test/Quiz, Resources**.                     |

</details>

<details>

<summary>Quy tắc tạo lớp học</summary>

| Mã rule       | Business Rule                                                                                                                                           |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-CREATE-001 | Người dùng chỉ được tạo lớp học nếu có quyền **Create Class**.                                                                                          |
| BR-CREATE-002 | Các trường bắt buộc khi tạo lớp bao gồm: **Name, Code, Construction Mode, Type, Số học viên tối đa** và các trường điều kiện khác tùy loại lớp.         |
| BR-CREATE-003 | **Code** của lớp phải là duy nhất trên hệ thống.                                                                                                        |
| BR-CREATE-004 | Theo tài liệu gốc, mã lớp học cần có ký tự **“.”**.                                                                                                     |
| BR-CREATE-005 | Người dùng chỉ có thể tạo thủ công các lớp có Type là **Lesson**, **Trial** hoặc **Revision**.                                                          |
| BR-CREATE-006 | Lớp **Foundation** không tạo thủ công; hệ thống tự động tạo khi lớp Lesson gắn với Normal Course có cấu hình Foundation Course.                         |
| BR-CREATE-007 | Nếu Construction Mode là **Offline** hoặc **Blended**, trường **Facility** là bắt buộc.                                                                 |
| BR-CREATE-008 | Nếu Construction Mode là **Online LMS** hoặc **Live Online**, trường **Facility** không bắt buộc.                                                       |
| BR-CREATE-009 | Nếu Construction Mode là **Online LMS**, hệ thống hiển thị trường **Duration**.                                                                         |
| BR-CREATE-010 | Nếu Construction Mode khác **Online LMS**, hệ thống hiển thị **Standard Schedule**, **Opening Date**, **Start Date** và các thông tin lịch học cố định. |
| BR-CREATE-011 | Nếu nhập **Number of Extended Days**, người dùng bắt buộc nhập **Reason of Extension**.                                                                 |
| BR-CREATE-012 | Sau khi tạo lớp thành công, lớp được hiển thị tại màn hình **Class List**.                                                                              |

</details>

<details>

<summary>Quy tắc Type của lớp học</summary>

| Mã rule     | Business Rule                                                                       |
| ----------- | ----------------------------------------------------------------------------------- |
| BR-TYPE-001 | **Lesson** là lớp học chính.                                                        |
| BR-TYPE-002 | **Trial** là lớp học thử.                                                           |
| BR-TYPE-003 | **Revision** là lớp ôn tập/luyện tập.                                               |
| BR-TYPE-004 | **Foundation** là lớp nền tảng được hệ thống tự động tạo, không tạo thủ công.       |
| BR-TYPE-005 | Khi chọn Course cho lớp **Lesson**, hệ thống chỉ hiển thị **Normal Course**.        |
| BR-TYPE-006 | Khi chọn Course cho lớp **Revision**, hệ thống chỉ hiển thị **Practice Course**.    |
| BR-TYPE-007 | Khi chọn Course cho lớp **Trial**, hệ thống chỉ hiển thị **Trial Course**.          |
| BR-TYPE-008 | Với lớp **Trial**, mỗi Trial Course chỉ được gắn với một lớp học.                   |
| BR-TYPE-009 | Khi chọn Exam cho lớp, danh sách Exam hiển thị theo **Program của Course** đã chọn. |

</details>

<details>

<summary>Quy tắc Class Owner và CX Admin</summary>

| Mã rule      | Business Rule                                                                                                                                               |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-OWNER-001 | Hai trường **Class Owner** và **CX Admin** bắt buộc khi lớp có **Type = Lesson** và Course thuộc một trong các Program: **ACCA, CFA, CMA, Cert/Dip, CGMA**. |
| BR-OWNER-002 | Class Owner và CX Admin được chọn theo định dạng **Tên nhân viên + Email nhân viên**.                                                                       |
| BR-OWNER-003 | Người dùng có thể tìm kiếm Class Owner/CX Admin bằng tên hoặc email.                                                                                        |
| BR-OWNER-004 | Người dùng luôn có thể chỉnh sửa **Class Owner** và **CX Admin**, ngoại trừ lớp **Foundation** và **Hybrid** vì các lớp này đồng bộ từ lớp chính.           |
| BR-OWNER-005 | Hệ thống gửi mail/tạo ticket cho CX Supervisor để kiểm tra Class Owner/CX Admin theo thời điểm dựa trên Start Date của lớp.                                 |
| BR-OWNER-006 | Nếu **Start Date - Create Date >= 7 ngày**, hệ thống gửi thông báo lúc 9:00 sáng, trước 7 ngày so với Start Date.                                           |
| BR-OWNER-007 | Nếu **Start Date - Create Date < 7 ngày**, hệ thống gửi thông báo lúc 9:00 sáng ngày hôm sau.                                                               |

</details>

<details>

<summary>Quy tắc Standard Schedule</summary>

| Mã rule         | Business Rule                                                                  |
| --------------- | ------------------------------------------------------------------------------ |
| BR-SCHEDULE-001 | Standard Schedule áp dụng với các lớp không phải **Online LMS**.               |
| BR-SCHEDULE-002 | Mỗi lớp cần có tối thiểu **01 lịch học cố định**.                              |
| BR-SCHEDULE-003 | Mỗi lớp có tối đa **03 lịch học cố định**.                                     |
| BR-SCHEDULE-004 | Mỗi lịch học gồm **Day of week** và **Start time - End time**.                 |
| BR-SCHEDULE-005 | Nếu lịch học từ **Thứ 2 đến Thứ 6**, Start time phải từ **18:00** trở đi.      |
| BR-SCHEDULE-006 | Nếu lịch học từ **Thứ 2 đến Thứ 6**, End time không vượt quá **22:00**.        |
| BR-SCHEDULE-007 | Nếu lịch học vào **Thứ 7 hoặc Chủ nhật**, Start time phải từ **08:00** trở đi. |
| BR-SCHEDULE-008 | Nếu lịch học vào **Thứ 7 hoặc Chủ nhật**, End time không vượt quá **22:00**.   |
| BR-SCHEDULE-009 | Thời lượng mỗi lịch học phải từ **2.5h đến 3.5h**.                             |

</details>

<details>

<summary>Quy tắc Duration, Opening Date và Extended Days</summary>

| Mã rule         | Business Rule                                                                                                                      |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| BR-DURATION-001 | Với Construction Mode = **Online LMS**, hệ thống hiển thị trường **Duration**.                                                     |
| BR-DURATION-002 | Duration có 2 kiểu: **Fixed** và **Flexible**.                                                                                     |
| BR-DURATION-003 | Với Duration = **Fixed**, thời hạn lớp được xác định theo Start Date - End Date.                                                   |
| BR-DURATION-004 | Với Duration = **Flexible**, thời hạn học của học viên phụ thuộc vào ngày học viên kích hoạt khóa học.                             |
| BR-DURATION-005 | Nếu nhập **Number of Extended Days**, bắt buộc nhập **Reason of Extension**.                                                       |
| BR-DURATION-006 | Nếu chỉnh sửa **Number of Extended Days = 0** hoặc để trống, hệ thống xóa dữ liệu Number of Extended Days và Reason For Extension. |
| BR-DURATION-007 | Khi Number of Extended Days bị xóa, duration học viên quay về cách tính mặc định.                                                  |
| BR-DURATION-008 | Start Date mặc định của học viên là ngày sớm nhất giữa **Opening Date** và **Class Start Date**.                                   |
| BR-DURATION-009 | End Date mặc định của học viên bằng **Class End Date + Number of Extended Days** nếu lớp có gia hạn.                               |
| BR-DURATION-010 | Nếu học viên đã chọn kỳ thi, End Date có thể được tính theo **Class Revision End Date**.                                           |

</details>

<details>

<summary>Quy tắc tạo và quản lý lớp Hybrid</summary>

| Mã rule       | Business Rule                                                                                                                                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-HYBRID-001 | Checkbox **Create Hybrid Class** chỉ hiển thị khi lớp có Construction Mode là **Offline** hoặc **Blended** và Type là **Lesson**.                                                                             |
| BR-HYBRID-002 | Khi tick **Create Hybrid Class**, người dùng bắt buộc nhập **Hybrid Class Code**.                                                                                                                             |
| BR-HYBRID-003 | Sau khi lưu lớp gốc thành công, hệ thống tự động tạo thêm lớp Hybrid.                                                                                                                                         |
| BR-HYBRID-004 | Tên lớp Hybrid = **Tên lớp gốc + “Hybrid”**.                                                                                                                                                                  |
| BR-HYBRID-005 | Construction Mode của lớp Hybrid mặc định là **Hybrid**.                                                                                                                                                      |
| BR-HYBRID-006 | Origin Class của lớp Hybrid là mã lớp gốc.                                                                                                                                                                    |
| BR-HYBRID-007 | Lớp Hybrid đồng bộ từ lớp gốc các thông tin: Status, Facility, Type, Duration, Start Date, End Date, Standard Schedule, Course, Class Owner, CX Admin, Exam, Mentor, Teacher, lịch học và tiến độ giảng viên. |
| BR-HYBRID-008 | Các trường Classroom, Link Meeting, Description và Max Students của lớp Hybrid để trống khi tạo tự động.                                                                                                      |
| BR-HYBRID-009 | Lớp Hybrid lưu danh sách học viên riêng, không tự động dùng chung danh sách học viên của lớp gốc.                                                                                                             |
| BR-HYBRID-010 | Lịch học Offline của lớp gốc được đồng bộ sang lớp Hybrid với Learning Mode = **Live Online**, ngoại trừ thông tin phòng học.                                                                                 |
| BR-HYBRID-011 | Lịch học Online LMS/Live Online của lớp gốc được đồng bộ toàn bộ sang lớp Hybrid.                                                                                                                             |
| BR-HYBRID-012 | Nếu bỏ tick **Create Hybrid Class** khi lớp Hybrid đã được tạo, lớp Hybrid sẽ bị khóa.                                                                                                                        |
| BR-HYBRID-013 | Khi bỏ tick Create Hybrid Class, người dùng bắt buộc nhập **Block Reason**.                                                                                                                                   |
| BR-HYBRID-014 | Khi lớp Hybrid bị khóa do bỏ tick, hệ thống làm rỗng Classroom và Link Meeting của lớp Hybrid.                                                                                                                |
| BR-HYBRID-015 | Nếu chỉnh sửa Type sang **Trial** hoặc **Revision**, lớp Hybrid đã tạo trước đó sẽ tự động bị xóa.                                                                                                            |
| BR-HYBRID-016 | Nếu chỉnh sửa Construction Mode sang **Online** hoặc **Live Online**, lớp Hybrid đã tạo trước đó sẽ tự động bị xóa.                                                                                           |
| BR-HYBRID-017 | Nếu lớp có Status = **Block**, checkbox Create Hybrid Class bị disable.                                                                                                                                       |
| BR-HYBRID-018 | Khi lớp Lesson chuyển sang **Block**, lớp Hybrid gắn với lớp đó nếu có cũng chuyển sang **Block**.                                                                                                            |

</details>

<details>

<summary>Quy tắc chỉnh sửa thông tin lớp học</summary>

| Mã rule     | Business Rule                                                                                                                                                                                                                                     |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-EDIT-001 | Người dùng chỉ được chỉnh sửa lớp nếu có quyền **Edit Class**.                                                                                                                                                                                    |
| BR-EDIT-002 | Lớp có trạng thái **Ended** không được chỉnh sửa.                                                                                                                                                                                                 |
| BR-EDIT-003 | Việc chỉnh sửa lớp phụ thuộc vào **Type**, **Construction Mode** và tiến độ học của học viên trong lớp.                                                                                                                                           |
| BR-EDIT-004 | Lớp **Hybrid** chỉ được chỉnh sửa các trường: Class name, Class code, Classroom, Link meeting, Description.                                                                                                                                       |
| BR-EDIT-005 | Các thông tin còn lại của lớp Hybrid không được chỉnh sửa trực tiếp vì đồng bộ từ lớp gốc.                                                                                                                                                        |
| BR-EDIT-006 | Với lớp **Foundation** đã có học viên học, chỉ được chỉnh sửa Name, Code, Area, Số học viên tối đa, Lecturer, Mentor và Description.                                                                                                              |
| BR-EDIT-007 | Với lớp **Foundation** chưa có học viên học, được chỉnh sửa tất cả thông tin, ngoại trừ Type, Course, Class Owner và CX Admin.                                                                                                                    |
| BR-EDIT-008 | Với lớp Trial/Revision/Lesson chưa có học viên học, người dùng được chỉnh sửa tất cả thông tin.                                                                                                                                                   |
| BR-EDIT-009 | Với lớp Trial/Revision/Lesson đã có học viên nhưng lớp chưa bắt đầu hoặc học viên chưa học, không được chỉnh sửa Status, Construction Mode, Facility, Type, Course và Exam.                                                                       |
| BR-EDIT-010 | Với lớp Trial/Revision/Lesson đã có học viên đang học hoặc lớp đã bắt đầu, không được chỉnh sửa Status, Construction Mode, Facility, Type, Create Hybrid Class, Course, Exam, Standard Schedule, Number of Extended Days và Reason For Extension. |

</details>

<details>

<summary>Quy tắc chọn Classroom</summary>

| Mã rule     | Business Rule                                                                                                                        |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| BR-ROOM-001 | Người dùng có thể chọn hoặc thay đổi Classroom tại màn hình chỉnh sửa lớp.                                                           |
| BR-ROOM-002 | Nếu Construction Mode = **Live Online** hoặc **Hybrid**, hệ thống chỉ hiển thị phòng học có Mode = **Virtual**.                      |
| BR-ROOM-003 | Nếu Construction Mode = **Offline** hoặc **Blended**, hệ thống chỉ hiển thị phòng học có Mode = **Physical** thuộc Facility của lớp. |
| BR-ROOM-004 | Chỉ hiển thị phòng học có Status = **Active**.                                                                                       |
| BR-ROOM-005 | Với phòng học vật lý, số học viên của lớp phải nhỏ hơn sức chứa của phòng.                                                           |
| BR-ROOM-006 | Hệ thống chỉ hiển thị các phòng có số buổi trùng lịch với lịch học tự động nhỏ hơn hoặc bằng **3 buổi**.                             |
| BR-ROOM-007 | Danh sách phòng học được sắp xếp theo số lượng buổi bị trùng lịch tự động.                                                           |
| BR-ROOM-008 | Nếu lớp chưa có lịch phòng học, hệ thống không hiển thị giá trị phòng học nào.                                                       |
| BR-ROOM-009 | Khi chỉnh sửa Classroom của lớp Live Online hoặc Hybrid, hệ thống tự động làm rỗng **Link Meeting** và yêu cầu người dùng nhập lại.  |

</details>

<details>

<summary>Quy tắc Import Class</summary>

| Mã rule       | Business Rule                                                                      |
| ------------- | ---------------------------------------------------------------------------------- |
| BR-IMPORT-001 | Người dùng chỉ được import lớp học nếu có quyền **Import Class**.                  |
| BR-IMPORT-002 | Chức năng Import Class dùng để tạo nhiều lớp học cùng lúc.                         |
| BR-IMPORT-003 | File import chỉ chấp nhận định dạng **.csv** hoặc **.xlsx**.                       |
| BR-IMPORT-004 | Mỗi lần import chỉ được chọn **01 file**.                                          |
| BR-IMPORT-005 | Người dùng nên tải file mẫu từ hệ thống trước khi nhập dữ liệu import.             |
| BR-IMPORT-006 | Dữ liệu trong file import cần tuân thủ đúng template và rule tạo lớp học.          |
| BR-IMPORT-007 | Các dòng hợp lệ trong file sẽ được tạo lớp thành công.                             |
| BR-IMPORT-008 | Các dòng không hợp lệ sẽ không được tạo lớp và được ghi nhận tại log import.       |
| BR-IMPORT-009 | Sau khi import, hệ thống hiển thị kết quả gồm Source, Data, Successfully và Error. |
| BR-IMPORT-010 | Người dùng có thể chọn **View Log** để xem chi tiết lỗi từng dòng.                 |
| BR-IMPORT-011 | Các trường không hợp lệ trong file import được bôi đỏ tại màn hình Import Detail.  |
| BR-IMPORT-012 | Lý do lỗi được hiển thị tại cột **Errors**.                                        |

</details>

<details>

<summary>Quy tắc quản lý học viên trong lớp</summary>

| Mã rule        | Business Rule                                                                                                                       |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| BR-STUDENT-001 | Học viên thường được tự động thêm vào lớp sau khi Deal trên HubSpot chuyển sang trạng thái **Won**.                                 |
| BR-STUDENT-002 | Người dùng có thể thêm học viên thủ công bằng chức năng **Add Student** nếu có quyền.                                               |
| BR-STUDENT-003 | Người dùng có thể import học viên bằng file nếu có quyền.                                                                           |
| BR-STUDENT-004 | File import học viên chỉ chấp nhận định dạng **.csv** hoặc **.xlsx**.                                                               |
| BR-STUDENT-005 | Mỗi lần import học viên chỉ được chọn **01 file**.                                                                                  |
| BR-STUDENT-006 | Với lớp Foundation, chỉ được thêm học viên có level trùng với level của lớp Foundation.                                             |
| BR-STUDENT-007 | Khi thêm học viên vào lớp **Lesson**, học viên đó cũng được thêm vào lớp **Foundation** và **Revision** gắn với lớp ban đầu.        |
| BR-STUDENT-008 | Khi xóa học viên khỏi lớp **Lesson**, học viên đó cũng được xóa khỏi lớp **Foundation** và **Revision** gắn với lớp ban đầu.        |
| BR-STUDENT-009 | Khi thêm hoặc xóa học viên khỏi lớp **Foundation** hoặc **Revision**, thao tác này không ảnh hưởng đến học viên của lớp **Lesson**. |
| BR-STUDENT-010 | Người dùng có thể xóa một học viên hoặc nhiều học viên khỏi lớp nếu có quyền.                                                       |
| BR-STUDENT-011 | Khi xóa học viên, hệ thống hiển thị popup xác nhận trước khi thực hiện.                                                             |
| BR-STUDENT-012 | Với lớp có Duration = Flexible, nếu học viên chưa kích hoạt khóa học thì không thể cập nhật thời hạn học của học viên đó.           |
| BR-STUDENT-013 | Thời hạn học riêng của học viên có thể dài hơn hoặc ngắn hơn thời hạn mặc định của lớp.                                             |
| BR-STUDENT-014 | Người dùng có thể chỉnh sửa Course Content riêng cho từng học viên.                                                                 |
| BR-STUDENT-015 | Việc chỉnh sửa Course Content riêng chỉ áp dụng cho học viên được chọn, không ảnh hưởng toàn bộ lớp.                                |
| BR-STUDENT-016 | Người dùng luôn được thêm mới cấu phần học cho học viên.                                                                            |
| BR-STUDENT-017 | Người dùng chỉ được xóa cấu phần học khỏi chương trình học của học viên nếu học viên chưa học cấu phần đó.                          |
| BR-STUDENT-018 | Nếu học viên đã học cấu phần đó, hệ thống không cho phép xóa cấu phần khỏi chương trình học của học viên.                           |
| BR-STUDENT-019 | Chức năng **Allow Pass Foundation** chỉ áp dụng khi lớp Lesson có gắn lớp Foundation.                                               |
| BR-STUDENT-020 | Allow Pass Foundation dùng để đánh dấu học viên hoàn thành khóa Foundation và cho phép học viên chuyển sang học khóa chính.         |

</details>

<details>

<summary>Quy tắc chọn/bỏ chọn cấu phần học của học viên</summary>

| Mã rule                | Business Rule                                                                                              |
| ---------------------- | ---------------------------------------------------------------------------------------------------------- |
| BR-STUDENT-CONTENT-001 | Khi chọn/bỏ chọn **All**, tất cả checkbox cấu phần học được tick hoặc bỏ tick.                             |
| BR-STUDENT-CONTENT-002 | Khi chọn **Section**, tất cả Subsection, Unit, Activity và Quiz thuộc Section được chọn.                   |
| BR-STUDENT-CONTENT-003 | Khi chọn **Subsection**, Section cha, các Unit, Activity và Case Study liên quan đến Subsection được chọn. |
| BR-STUDENT-CONTENT-004 | Khi chọn **Unit**, Section, Subsection và các Activity liên quan đến Unit được chọn.                       |
| BR-STUDENT-CONTENT-005 | Khi chọn **Activity**, Section, Subsection và Unit chứa Activity đó được chọn.                             |
| BR-STUDENT-CONTENT-006 | Cấu phần bị bỏ chọn sẽ không xuất hiện trong chương trình học của học viên.                                |
| BR-STUDENT-CONTENT-007 | Học viên không cần học các cấu phần đã bị bỏ chọn khỏi chương trình học cá nhân.                           |
| BR-STUDENT-CONTENT-008 | Không được xóa cấu phần học viên đã học.                                                                   |
| BR-STUDENT-CONTENT-009 | Được phép xóa cấu phần học viên chưa học.                                                                  |

</details>

<details>

<summary>Quy tắc quản lý trợ giảng trong lớp</summary>

| Mã rule       | Business Rule                                                                                                           |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| BR-MENTOR-001 | Người dùng chỉ được thêm/xóa trợ giảng nếu có quyền quản lý Mentor trong lớp.                                           |
| BR-MENTOR-002 | Danh sách trợ giảng được lấy từ **Staff List** trên hệ thống.                                                           |
| BR-MENTOR-003 | Người dùng có thể thêm một hoặc nhiều trợ giảng vào lớp.                                                                |
| BR-MENTOR-004 | Người dùng có thể xóa một trợ giảng hoặc nhiều trợ giảng cùng lúc.                                                      |
| BR-MENTOR-005 | Khi xóa trợ giảng, hệ thống hiển thị popup xác nhận trước khi thực hiện.                                                |
| BR-MENTOR-006 | Trợ giảng được chọn tại cột **Main Responsible** được hiểu là trợ giảng chính của lớp.                                  |
| BR-MENTOR-007 | Theo tài liệu gốc, Main Responsible liên quan đến tính năng chấm điểm sẽ được ra mắt trong thời gian tới.               |
| BR-MENTOR-008 | Nếu lớp Lesson có gắn Foundation, khi thêm trợ giảng vào lớp Lesson thì trợ giảng đó cũng được thêm vào lớp Foundation. |
| BR-MENTOR-009 | Nếu lớp Lesson có gắn Foundation, khi xóa trợ giảng khỏi lớp Lesson thì trợ giảng đó cũng bị xóa khỏi lớp Foundation.   |
| BR-MENTOR-010 | Thao tác thêm/xóa trợ giảng tại lớp không gắn Foundation chỉ áp dụng cho lớp đang thao tác.                             |

</details>

<details>

<summary>Quy tắc quản lý giảng viên trong lớp</summary>

| Mã rule        | Business Rule                                                                                                                                          |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| BR-TEACHER-001 | Giảng viên được gắn theo từng **Section**, không gắn chung cho toàn bộ lớp.                                                                            |
| BR-TEACHER-002 | Người dùng cần có quyền thao tác Teacher để gắn, thay đổi hoặc xóa giảng viên trong lớp.                                                               |
| BR-TEACHER-003 | Lớp cần có lịch học tự động trước khi chọn giảng viên.                                                                                                 |
| BR-TEACHER-004 | Nếu lớp chưa có lịch học tự động, hệ thống báo lỗi **“Please add learning schedule before choosing teacher”**.                                         |
| BR-TEACHER-005 | Danh sách giảng viên của lớp hiển thị theo thời gian gắn giảng viên, từ sớm nhất đến muộn nhất.                                                        |
| BR-TEACHER-006 | Màn hình chọn giảng viên hiển thị danh sách giảng viên theo thời gian tạo mới nhất trước.                                                              |
| BR-TEACHER-007 | Người dùng được phép chỉnh sửa giảng viên khi request đặt lịch có trạng thái **Pending**, **Approved**, **Rejected** hoặc **Cancelled**.               |
| BR-TEACHER-008 | Người dùng chỉ được xóa giảng viên khi request đặt lịch dạy có trạng thái **Pending**.                                                                 |
| BR-TEACHER-009 | Khi thay đổi giảng viên với request có trạng thái **Approved**, người dùng bắt buộc nhập lý do thay đổi.                                               |
| BR-TEACHER-010 | Khi xóa giảng viên thành công, Section gắn với giảng viên đó sẽ trống trường **Responsibility**.                                                       |
| BR-TEACHER-011 | Khi xóa giảng viên thành công, request đặt lịch của giảng viên cũ bị xóa và không hiển thị ở phía giảng viên cũ.                                       |
| BR-TEACHER-012 | Với Section có tất cả buổi học là **Online LMS**, hệ thống vẫn cho phép gắn giảng viên nhưng không gửi email, không gửi request và không có status.    |
| BR-TEACHER-013 | Khi gắn giảng viên vào Section, hệ thống gửi request đặt lịch cho các buổi trong Section có Learning Mode là **Offline** hoặc **Live Online**.         |
| BR-TEACHER-014 | Với request đặt lịch giảng viên có trạng thái Approved, hệ thống cập nhật giảng viên tại các buổi có lịch tự động được gắn với Section của giảng viên. |
| BR-TEACHER-015 | Hệ thống chỉ cập nhật giảng viên cho các buổi có lịch tự động, không cập nhật cho các buổi lịch thủ công.                                              |

</details>

<details>

<summary>Quy tắc hiển thị giảng viên tại màn chọn Teacher</summary>

| Mã rule             | Business Rule                                                                                                                    |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| BR-TEACHER-LIST-001 | Chỉ hiển thị giảng viên có **Teaching Status = Đang dạy**.                                                                       |
| BR-TEACHER-LIST-002 | Chỉ hiển thị giảng viên có gắn với cơ sở diễn ra buổi học.                                                                       |
| BR-TEACHER-LIST-003 | Chỉ hiển thị giảng viên có **Belong To** trùng với nội dung/Section giảng dạy.                                                   |
| BR-TEACHER-LIST-004 | Chỉ hiển thị giảng viên có lịch cá nhân trùng lịch học của Section tối đa **3 buổi**.                                            |
| BR-TEACHER-LIST-005 | Chỉ hiển thị giảng viên không vượt định mức tuần khi nhận thêm lịch dạy này.                                                     |
| BR-TEACHER-LIST-006 | Nếu lịch giảng viên trùng nhiều hơn **3 buổi**, giảng viên không hiển thị tại màn Add Teacher.                                   |
| BR-TEACHER-LIST-007 | Nếu lịch giảng viên trùng từ **1 đến 3 buổi**, hệ thống vẫn cho phép chọn nhưng hiển thị popup cảnh báo danh sách buổi bị trùng. |
| BR-TEACHER-LIST-008 | Nếu lịch giảng viên không trùng, giảng viên hiển thị và có thể được chọn bình thường.                                            |

</details>

<details>

<summary>Quy tắc trạng thái request đặt lịch giảng viên</summary>

| Mã rule            | Business Rule                                                                                       |
| ------------------ | --------------------------------------------------------------------------------------------------- |
| BR-TEACHER-REQ-001 | **Pending** là trạng thái request đang chờ giảng viên duyệt.                                        |
| BR-TEACHER-REQ-002 | Nếu request ở trạng thái Pending, người dùng có thể xóa giảng viên khỏi Section.                    |
| BR-TEACHER-REQ-003 | **Approved** là trạng thái giảng viên đã duyệt request.                                             |
| BR-TEACHER-REQ-004 | Nếu request đã Approved và người dùng đổi giảng viên, người dùng phải nhập lý do thay đổi.          |
| BR-TEACHER-REQ-005 | **Rejected** là trạng thái giảng viên đã từ chối request. Hệ thống hiển thị Reason.                 |
| BR-TEACHER-REQ-006 | **Cancelled** là trạng thái request đã bị hủy. Hệ thống hiển thị Reason.                            |
| BR-TEACHER-REQ-007 | Người dùng có thể xem lịch sử request/giảng viên đã từng gắn với Section tại chức năng **History**. |

</details>

<details>

<summary>Quy tắc quản lý bài kiểm tra trong lớp</summary>

| Mã rule     | Business Rule                                                                                                  |
| ----------- | -------------------------------------------------------------------------------------------------------------- |
| BR-TEST-001 | Tab **Test/Quiz** hiển thị danh sách bài kiểm tra thuộc Course đã gắn với lớp.                                 |
| BR-TEST-002 | Nếu Course chưa có bài kiểm tra trong Course Content, tab Test/Quiz không hiển thị dữ liệu bài kiểm tra.       |
| BR-TEST-003 | Người dùng có thể tìm kiếm/lọc bài kiểm tra theo tên bài kiểm tra, loại bài kiểm tra và Manual Grading.        |
| BR-TEST-004 | Người dùng có thể xem chi tiết bài kiểm tra bằng cách nhấp vào tên bài kiểm tra hoặc chọn **Action → Detail**. |
| BR-TEST-005 | Màn hình chi tiết bài kiểm tra hiển thị danh sách học viên được làm bài kiểm tra đó.                           |
| BR-TEST-006 | Thời gian truy cập bài kiểm tra có thể được cài đặt cho toàn bộ học viên hoặc cho từng học viên.               |
| BR-TEST-007 | Thời gian truy cập riêng của từng học viên chỉ áp dụng cho học viên đó.                                        |
| BR-TEST-008 | Khi xóa Access Time của bài kiểm tra, hệ thống hiển thị popup xác nhận trước khi thực hiện.                    |
| BR-TEST-009 | Người dùng có thể xuất kết quả bài kiểm tra ra file Excel bằng chức năng **Export Result**.                    |
| BR-TEST-010 | File Export Result được đặt tên theo cú pháp **\[Mã lớp]\_\[Tên bài kiểm tra]**.                               |
| BR-TEST-011 | Nếu học viên chưa nộp bài, thông tin điểm trong file Excel hiển thị rỗng.                                      |
| BR-TEST-012 | Nếu bài kiểm tra chấm thủ công chưa chấm xong, thông tin điểm trong file Excel hiển thị rỗng.                  |

</details>

<details>

<summary>Quy tắc trạng thái bài làm Test/Quiz</summary>

| Mã rule            | Business Rule                                                                                                       |
| ------------------ | ------------------------------------------------------------------------------------------------------------------- |
| BR-TEST-STATUS-001 | Với bài kiểm tra hệ thống chấm tự động, trạng thái bài làm gồm **Unsubmitted** và **Submitted**.                    |
| BR-TEST-STATUS-002 | **Unsubmitted** nghĩa là học viên chưa nộp bài.                                                                     |
| BR-TEST-STATUS-003 | **Submitted** nghĩa là học viên đã hoàn thành bài kiểm tra.                                                         |
| BR-TEST-STATUS-004 | Với bài kiểm tra chấm thủ công, trạng thái bài làm gồm **Unsubmitted**, **Awaiting Grading** và **Finish Grading**. |
| BR-TEST-STATUS-005 | **Awaiting Grading** nghĩa là học viên đã nộp bài và đang chờ chấm.                                                 |
| BR-TEST-STATUS-006 | **Finish Grading** nghĩa là bài làm của học viên đã được chấm xong.                                                 |

</details>

<details>

<summary>Quy tắc Access Time của Test/Quiz</summary>

| Mã rule       | Business Rule                                                                                                                                    |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| BR-ACCESS-001 | Start date của Access Time phải lớn hơn hoặc bằng **Opening Date** của Class.                                                                    |
| BR-ACCESS-002 | End date của Access Time phải nhỏ hơn hoặc bằng **End Date** của Class.                                                                          |
| BR-ACCESS-003 | Nếu Opening Date của Class thay đổi và Opening Date mới lớn hơn Opening Date của Access Time, Access Time được cập nhật theo Start Date của lớp. |
| BR-ACCESS-004 | Nếu End Date của Class thay đổi và End Date mới nhỏ hơn End Date của Access Time, Access Time được cập nhật theo End Date của lớp.               |
| BR-ACCESS-005 | Học viên chỉ truy cập được bài kiểm tra trong khoảng thời gian Access Time được cấu hình.                                                        |
| BR-ACCESS-006 | Nếu chưa đến thời gian mở hoặc đã quá thời hạn nộp, học viên không thể truy cập bài kiểm tra.                                                    |

</details>

<details>

<summary>Quy tắc Calendar của lớp</summary>

| Mã rule         | Business Rule                                                                                                              |
| --------------- | -------------------------------------------------------------------------------------------------------------------------- |
| BR-CALENDAR-001 | Tab Calendar hiển thị lịch học của lớp theo dạng lịch.                                                                     |
| BR-CALENDAR-002 | Người dùng có thể generate schedule nếu có quyền.                                                                          |
| BR-CALENDAR-003 | Người dùng có thể thêm lesson thủ công nếu có quyền.                                                                       |
| BR-CALENDAR-004 | Calendar hiển thị các loại buổi học như Online, Live Online, Offline, Cancelled, Holiday, Case Study, Test và Key Content. |
| BR-CALENDAR-005 | Lịch học của lớp chịu ảnh hưởng từ Standard Schedule, Course Content, Learning Schedule và lịch nghỉ lễ nếu có.            |
| BR-CALENDAR-006 | Nếu lớp chưa được generate schedule hoặc chưa có lesson, tab Calendar có thể không có dữ liệu lịch học.                    |

</details>

<details>

<summary>Quy tắc trạng thái và kết thúc lớp</summary>

| Mã rule       | Business Rule                                                                                         |
| ------------- | ----------------------------------------------------------------------------------------------------- |
| BR-STATUS-001 | Lớp có trạng thái **Ended** không được chỉnh sửa.                                                     |
| BR-STATUS-002 | Một số thao tác với lớp phụ thuộc vào trạng thái lớp và việc học viên đã học hay chưa.                |
| BR-STATUS-003 | Khi lớp Lesson bị chuyển sang Block, lớp Hybrid liên quan cũng bị chuyển sang Block nếu có.           |
| BR-STATUS-004 | Lớp Foundation và Hybrid có nhiều thông tin đồng bộ từ lớp chính nên bị giới hạn chỉnh sửa trực tiếp. |

</details>

<details>

<summary>Quy tắc dữ liệu đồng bộ giữa các lớp liên quan</summary>

| Mã rule     | Business Rule                                                                                            |
| ----------- | -------------------------------------------------------------------------------------------------------- |
| BR-SYNC-001 | Lớp Hybrid đồng bộ phần lớn thông tin từ lớp gốc.                                                        |
| BR-SYNC-002 | Lớp Foundation được tạo và đồng bộ theo logic từ lớp Lesson gắn Normal Course có Foundation Course.      |
| BR-SYNC-003 | Khi thêm/xóa học viên ở lớp Lesson, hệ thống đồng bộ học viên sang lớp Foundation và Revision liên quan. |
| BR-SYNC-004 | Khi thêm/xóa học viên ở lớp Foundation hoặc Revision, hệ thống không đồng bộ ngược về lớp Lesson.        |
| BR-SYNC-005 | Khi thêm/xóa Mentor ở lớp Lesson có gắn Foundation, hệ thống đồng bộ Mentor sang lớp Foundation.         |
| BR-SYNC-006 | Khi thao tác Mentor tại lớp không gắn Foundation, hệ thống chỉ áp dụng cho lớp đang thao tác.            |

</details>
