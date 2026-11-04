# Campaign

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** UpLMS Operator

**Đường dẫn:** Gamification → khối **Campaign** (cuối trang)
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Gamification (Campaign)
* **Module liên quan:** Leaderboard, Points
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Tạo, sửa, xoá campaign: tài khoản có quyền **Sửa cấu hình gamification** và công tắc **Gamification** đang bật.
* Xem và xuất kết quả: tài khoản có quyền **Xem danh sách học viên và hạng**.
* Học viên chỉ thấy campaign khi khối **Leaderboard** đang bật.
{% endhint %}

Campaign là đợt thi đua có thời hạn trên toàn tổ chức, ví dụ "Thi đua học tập tháng 11". Bảng xếp hạng chung là số liệu sống, có thể thay đổi. Campaign thì có kết quả chốt cố định lúc kết thúc, dùng để công bố và trao thưởng.

## II. Hướng dẫn chi tiết

<details>

<summary>Danh sách campaign</summary>

Khối **Campaign** liệt kê mọi campaign của tổ chức với các cột:

* **Name**: tên campaign.
* **Duration**: ngày bắt đầu và ngày kết thúc.
* **Status**: **Not started** (chưa bắt đầu), **In Progress** (đang chạy) hoặc **Expired** (đã kết thúc). Trạng thái tính theo ngày hiện tại.
* **Contribution**: những gì campaign tính, ví dụ `Point (Checkin; Activity); Activity; Course`.
* **Action**: thao tác được phép theo trạng thái.

</details>

<details>

<summary>Tạo campaign</summary>

{% stepper %}
{% step %}
**Mở form tạo**

Bấm **+ Campaign**. Panel **Campaign Settings** mở ra từ cạnh phải.

<figure><img src="../.gitbook/assets/gamification-campaign-settings.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Nhập thông tin**

* **Name:** tên campaign, bắt buộc.
* **Start:** ngày bắt đầu, bắt buộc, sớm nhất là ngày mai.
* **End:** ngày kết thúc, bắt buộc, không trước ngày bắt đầu. Bắt đầu và kết thúc cùng một ngày là hợp lệ.
{% endstep %}

{% step %}
**Chọn hành động được tính điểm**

Trong nhóm **Points**, tick các hành động được tính vào bảng điểm của campaign. Chọn ít nhất một:

* **On each daily check-in**
* **On each activity completion**
* **On each course completion**
* **On each successful test completion**
* **On each badge earned**

Campaign không có số điểm riêng. Mỗi hành động được tính theo số điểm đang cấu hình ở khối **Points**.

Hành động đang tắt ở khối **Points** vẫn chọn được, nhưng chưa sinh điểm cho tới khi được bật lại.
{% endstep %}

{% step %}
**Chọn bảng Activities**

Tick **Activity** nếu muốn campaign có thêm bảng xếp hạng theo số hoạt động hoàn thành. Bảng **Courses** (số khoá hoàn thành) luôn có.
{% endstep %}

{% step %}
**Lưu campaign**

Bấm **Save** để tạo, **Cancel** để huỷ. Khác trang cấu hình, form này không tự lưu.
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Sửa và xoá campaign</summary>

| Trạng thái | Sửa | Xoá |
| --- | --- | --- |
| **Not started** | Sửa được mọi thông tin | Được. Xác nhận bằng popover cạnh nút xoá |
| **In Progress** | Chỉ sửa được tên | Không được. Cũng không dừng sớm được |
| **Expired** | Chỉ xem | Không được |

Campaign đang chạy giữ nguyên luật tới khi kết thúc để học viên đang thi đua không bị đổi luật giữa chừng.

{% hint style="info" %}
Trạng thái được xét lúc bấm **Save**. Ví dụ mở form lúc 23:50 khi campaign còn **Not started** rồi bấm **Save** lúc 00:05 hôm sau, khi campaign đã chạy: chỉ thay đổi tên được lưu, các thay đổi khác bị từ chối kèm thông báo lý do.
{% endhint %}

</details>

<details>

<summary>Xem và xuất kết quả</summary>

{% stepper %}
{% step %}
**Mở kết quả**

Tại cột **Action**, bấm biểu tượng xem của campaign đang chạy hoặc đã kết thúc. Panel kết quả mở ra từ cạnh phải, tiêu đề là tên campaign kèm khoảng thời gian.

<figure><img src="../.gitbook/assets/gamification-campaign-ket-qua.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Xem từng bảng**

Chọn tab **Points**, **Activities** (nếu campaign có) hoặc **Courses**. Mỗi bảng có top 3, 5 dòng đầu và **Show All** để xem toàn bộ học viên.

* Campaign đang chạy: số tạm tính, kèm nhãn **Last updated**. Bảng tính lại khoảng 8 tiếng một lần.
* Campaign đã kết thúc: kết quả chính thức, kèm thời điểm chốt.
{% endstep %}

{% step %}
**Xuất Excel**

Bấm nút xuất để tải file Excel gồm mọi bảng của campaign. Campaign đang chạy vẫn xuất được, file ghi rõ đây là số tạm tính.
{% endstep %}
{% endstepper %}

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Kết quả chốt đúng lúc campaign kết thúc và **không bao giờ thay đổi**. Dùng file xuất từ campaign đã kết thúc để công bố và trao thưởng.
2. Không dùng danh sách học viên để thay kết quả campaign. Danh sách học viên là số liệu sống và không lọc theo loại hành động, nên số sẽ lệch với bảng campaign học viên đã thấy.
3. Bài Test nộp trong campaign nhưng được chấm đạt sau khi campaign kết thúc thì không tính.
4. Học viên bị **Block** hoặc rời tổ chức sau khi campaign kết thúc vẫn nằm trong kết quả. Trước lúc kết thúc thì không xuất hiện.
5. Nhiều campaign được chạy chồng thời gian. Mỗi campaign tính độc lập.
6. Đổi cấu hình khối **Points** trong lúc campaign đang chạy là đổi luật của campaign đó. Cân nhắc trước khi sửa.
7. Hệ thống không gửi thông báo cho học viên khi campaign bắt đầu hay kết thúc. Đội truyền thông tự thông báo qua kênh của tổ chức.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống | Nguyên nhân | Cách xử lý |
| --- | --- | --- |
| Không thấy nút **+ Campaign** | Tài khoản không có quyền **Sửa cấu hình gamification**, hoặc **Gamification** đang tắt | Kiểm tra quyền và công tắc **Gamification** |
| Không chọn được ngày bắt đầu là hôm nay | Ngày bắt đầu sớm nhất là ngày mai | Chọn từ ngày mai trở đi |
| Không sửa được ngày hoặc hành động | Campaign đã bắt đầu | Chỉ sửa được tên. Cần luật khác thì tạo campaign mới |
| Không xoá được campaign | Campaign đang chạy hoặc đã kết thúc | Không xoá được campaign ở hai trạng thái này |
| Không mở được kết quả campaign | Tài khoản không có quyền **Xem danh sách học viên và hạng** | Liên hệ quản trị để được gán quyền |
| Học viên không thấy campaign | Campaign chưa bắt đầu, hoặc khối **Leaderboard** đang tắt | Campaign hiện với học viên từ ngày bắt đầu, khi **Leaderboard** bật |
