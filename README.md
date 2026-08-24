---
cover: >-
  https://images.unsplash.com/photo-1785228861910-afa6c4197203?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3ODcyODc0NDZ8&ixlib=rb-4.1.0&q=85
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: hero
    mask: none
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Welcome to UpLMS Ops - UpBase

#### UpLMS Ops là gì?

UpLMS Ops là hệ thống vận hành đào tạo nội bộ của UpBase. Học viên học trên **UpLMS**; còn toàn bộ phần cấu hình và vận hành phía sau — xây dựng khóa học, mở lớp, quản lý tài khoản, chấm điểm, gửi thông báo — diễn ra tại **UpLMS Ops**.

Các bộ phận làm việc trên cùng một nguồn dữ liệu: khóa học tạo ở Academic Management được gắn vào lớp ở Class Management, học viên tạo ở User Management được thêm vào lớp đó, và kết quả học tập chảy về Grading và Dashboard.

***

#### Tài liệu này dành cho ai?

| Vai trò                       | Phần tài liệu liên quan                                                                 |
| ----------------------------- | --------------------------------------------------------------------------------------- |
| **UpLMS Operator**            | Xuất hiện ở hầu hết các mục: User Management, Academic Management, Class, Dashboard, Engagement & Support |
| **Admin**                     | Bài kiểm tra trong lớp, Dashboard, Email và Thông báo hệ thống                          |
| **L\&D**                      | Danh sách khóa học, Tạo khóa học                                                        |
| **SX**                        | Storyline                                                                               |
| **Mentor / Mentor chính**     | Toàn bộ mục Chấm điểm                                                                   |
| **CX**                        | Bài kiểm tra trong lớp                                                                  |
| **Giảng viên, Quản lý chương trình** | SIS Operational Dashboard                                                        |

Mỗi trang đều có trường **Dành cho** ở đầu — nếu vai trò của bạn không nằm trong đó, khả năng cao bạn không có quyền thao tác trên màn hình được mô tả.

***

#### Tài liệu gồm những gì?

| Mục                                                                | Nội dung                                                                                        |
| ------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------- |
| [User Management](user-management/quan-ly-ho-so-ca-nhan-profile.md) | Hồ sơ cá nhân, tài khoản học viên và tài khoản nhân viên vận hành                               |
| [Academic Management](academic-management/quan-ly-khoa-hoc-courses/README.md) | Khóa học, nội dung học, ngân hàng câu hỏi, Case Study, Storyline, danh mục và chứng chỉ |
| [Class Management](class-management/tong-quan-lop-hoc-classes.md)  | Tạo và vận hành lớp: học viên, trợ giảng, tài liệu, bài kiểm tra trong lớp                      |
| [Chấm điểm](cham-diem-grading/cham-diem-thu-cong/README.md)        | Chấm bài tự luận thủ công, phân công người chấm, chấm lại và lịch sử chấm                       |
| [Dashboard](dashboard/sis-operational-dashboard.md)                | Biểu đồ theo dõi chuyên cần, điểm đầu vào, phân phối điểm và tiến độ học                        |
| [Engagement & Support](engagement-and-support/nhan-su-ho-tro-tra-loi-binh-luan.md) | Email và thông báo hệ thống, nhóm người nhận, nhân sự trả lời bình luận          |

<figure><img src=".gitbook/assets/image (1)" alt=""><figcaption><p>Luồng tổng quan quản lý hành trình học tập của học viên trên UpLMS Ops</p></figcaption></figure>

***

#### Cách dùng tài liệu này

**Tra cứu theo công việc, không cần đọc tuần tự.** Tài liệu được tổ chức theo module, mỗi module tương ứng một nhóm chức năng trên hệ thống. Dùng thanh điều hướng bên trái để đi thẳng đến màn hình bạn đang làm việc.

**Mỗi trang có cùng một cấu trúc.** Phần I cho biết trang dành cho ai và đường dẫn tới màn hình; phần II là các bước thao tác; phần III là quy tắc nghiệp vụ cần nhớ; phần IV là các lỗi thường gặp kèm cách xử lý. Khi gặp sự cố, đọc phần IV trước.

**Thứ tự nhập liệu có ràng buộc.** Nhiều thao tác phụ thuộc bước trước: khóa học phải có nội dung và chứng chỉ mới publish được, lớp phải gắn khóa học mới thêm được học viên, câu hỏi phải thuộc một cấu phần học mới gắn được vào bài kiểm tra. Nếu một nút hoặc một trường không hiện, thường là do bước trước chưa hoàn tất — không phải lỗi hệ thống.

{% hint style="info" %}
Nếu tài liệu chưa khớp với giao diện bạn đang thấy, hoặc thiếu hướng dẫn cho một màn hình, hãy phản hồi lại để đội vận hành cập nhật.
{% endhint %}
