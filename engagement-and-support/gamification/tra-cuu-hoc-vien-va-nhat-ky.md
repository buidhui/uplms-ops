# Tra cứu học viên và nhật ký

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** UpLMS Operator

**Đường dẫn:** Gamification → danh sách học viên, Gamification → **Achievement history**
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Gamification
* **Module liên quan:** User Management (Students)
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Tài khoản có quyền **Xem danh sách học viên và hạng**.
* Xem được cả khi **Gamification** đang tắt, với dữ liệu đã ghi trước đó.
{% endhint %}

Hai màn này chỉ để tra cứu, không có thao tác sửa. Vận hành không cộng trừ điểm, không sửa hạng và không trao hay gỡ huy hiệu bằng tay.

## II. Hướng dẫn chi tiết

<details>

<summary>Danh sách học viên</summary>

{% stepper %}
{% step %}
**Mở danh sách**

Trong khu vực **Gamification**, mở danh sách học viên. Danh sách gồm mọi học viên của tổ chức, kể cả người chưa có điểm nào.

| Cột | Ý nghĩa |
| --- | --- |
| **Learner** | Ảnh đại diện và tên học viên |
| **Level** | Hạng hiện tại. Ẩn khi khối **Levels** tắt |
| **Points** | Điểm tích luỹ. Ẩn khi khối **Points** tắt |
| **Badges** | Số huy hiệu đã đạt của các loại đang bật. Ẩn khi khối **Badges** tắt |
| **Activities** | Số hoạt động học đã hoàn thành |
| **Courses** | Số khoá đã hoàn thành |
| **Last activity** | Ngày gần nhất học viên vào hệ thống |
{% endstep %}

{% step %}
**Lọc, tìm kiếm và sắp xếp**

* **Search:** tìm theo tên học viên.
* **Khoảng ngày:** chọn tự do **Start time → End time**, hoặc nút nhanh **All time** · **This week** · **This month** · **This quarter** · **This year**. Mặc định **All time**. Chọn một khoảng thì **Points**, **Activities**, **Courses** tính trong khoảng đó, còn cột **Level** và **Badges** ẩn đi.
* **Sắp xếp:** bấm tiêu đề cột. Mặc định sắp theo hạng giảm dần.
{% endstep %}

{% step %}
**Xuất Excel**

Bấm **Export** để tải file Excel. File gồm mọi dòng theo bộ lọc và thứ tự sắp xếp hiện tại, không chỉ trang đang xem.

{% hint style="info" %}
Số liệu trong file là ảnh chụp tại thời điểm xuất. Xuất lại cùng khoảng ngày vào lúc khác có thể ra số khác. Giữ lại file đã dùng để công bố làm căn cứ.
{% endhint %}
{% endstep %}

{% step %}
**Xem nhật ký của một học viên**

Bấm tên học viên để mở nhật ký ghi nhận đã lọc sẵn theo người đó.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Nhật ký ghi nhận (Achievement history)</summary>

Nhật ký liệt kê mọi lần hệ thống ghi nhận điểm, huy hiệu và lên hạng của cả tổ chức. Đây là công cụ chính trong giai đoạn chạy ngầm, khi học viên chưa thấy gì và vận hành cần kiểm tra điểm có được ghi đúng không.

{% stepper %}
{% step %}
**Mở nhật ký**

Trong khu vực **Gamification**, chọn **Achievement history**.

| Cột | Ý nghĩa |
| --- | --- |
| **Time** | Thời điểm ghi nhận, dạng `HH:mm dd/mm/yyyy` |
| **Learner** | Ảnh đại diện và tên học viên |
| **Event** | **Points**, **Badge** hoặc **Level up** |
| **Details** | Nguồn cụ thể, ví dụ `Completed activity {tên hoạt động} in {tên khoá}`, `Daily check-in · day 3 of streak`, `Reached Level 4` |
| **Points** | Số điểm của sự kiện **Points**. Để trống với **Badge** và **Level up** |

Dòng mới nhất ở trên cùng.
{% endstep %}

{% step %}
**Lọc nhật ký**

* **Học viên:** tìm theo tên để chỉ xem lịch sử của một người.
* **Loại sự kiện:** chọn một hoặc nhiều trong **Points**, **Badge**, **Level up**. Với **Points** có thể lọc thêm theo hành động: check-in, hoạt động, khoá, bài Test.
* **Khoảng ngày:** chọn tự do hoặc nút nhanh như danh sách học viên.
{% endstep %}

{% step %}
**Trả lời thắc mắc của học viên**

Ví dụ học viên hỏi "sao tuần này tôi chỉ có 40 điểm": lọc theo tên học viên và **This week**, rồi đối chiếu từng dòng với việc học viên đã làm.

Dòng có đuôi `· points off` và cột **Points** bằng `0` là lần ghi nhận khi khối **Points** hoặc hành động đó đang tắt. Học viên không thấy những dòng này trong lịch sử của họ.
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Danh sách học viên và nhật ký cập nhật **ngay**. Bảng xếp hạng phía học viên tính lại khoảng 8 tiếng một lần, nên hai nơi có thể lệch nhau trong vòng 8 tiếng.
2. Nhật ký hiện đầy đủ kể cả khi **Visibility in UpLMS** đang tắt.
3. Nhật ký giữ toàn bộ, không sửa, không xoá và không xuất file được. Số liệu để công bố lấy từ danh sách học viên hoặc kết quả campaign.
4. Học viên bị **Block** hoặc đã rời tổ chức không có trong danh sách học viên, nhưng các dòng đã ghi của họ vẫn còn trong nhật ký.
5. Tài khoản kiểm thử (**Test Account**) không có trong cả hai màn.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống | Nguyên nhân | Cách xử lý |
| --- | --- | --- |
| Không mở được hai màn này | Tài khoản không có quyền **Xem danh sách học viên và hạng** | Liên hệ quản trị để được gán quyền |
| Không thấy cột **Level** hoặc **Badges** | Đang chọn khoảng ngày khác **All time**, hoặc khối tương ứng đang tắt | Chọn **All time** và kiểm tra công tắc khối |
| Điểm trong danh sách khác điểm trên bảng xếp hạng | Bảng xếp hạng chưa tới lượt tính lại | Chờ lượt tính kế tiếp, xem nhãn **Last updated** trên bảng xếp hạng |
| Không tìm thấy một học viên | Học viên bị **Block**, đã rời tổ chức, hoặc là tài khoản kiểm thử | Kiểm tra trạng thái tài khoản ở **User Management → Students** |
| Học viên học mà không có dòng điểm nào | Nội dung đã hoàn thành trước khi bật Gamification, hoặc đã được tính trong lượt học này | Mỗi nội dung chỉ được điểm một lần trong một lượt học |
