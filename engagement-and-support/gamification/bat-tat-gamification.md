# Bật tắt Gamification

## I. Thông tin chung

{% hint style="info" %}
**Dành cho:** UpLMS Operator

**Đường dẫn:** Gamification
{% endhint %}

{% hint style="info" %}
#### Phạm vi & Module liên quan

* **Module chính:** Gamification
* **Module liên quan:** Phân quyền Ops, UpLMS (phía học viên)
{% endhint %}

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Đã có tài khoản và được cấp quyền truy cập hệ thống UpLMS Ops.
* Tài khoản có quyền **Sửa cấu hình gamification** để bật tắt. Chỉ có quyền **Xem cấu hình gamification** thì xem được trang nhưng không thao tác được.
{% endhint %}

Gamification ghi nhận việc học của học viên thành điểm, huy hiệu, hạng và bảng xếp hạng. Toàn bộ cấu hình nằm trên một trang, gồm hai công tắc chung ở đầu trang, bốn khối chức năng **Points**, **Badges**, **Levels**, **Leaderboard** và khối **Campaign** ở cuối trang.

## II. Hướng dẫn chi tiết

<details>

<summary>Hai công tắc và ba trạng thái</summary>

{% stepper %}
{% step %}
**Mở trang cấu hình**

Chọn **Gamification** tại menu sidebar của Ops.

<figure><img src="../../.gitbook/assets/gamification-tat.png" alt=""><figcaption><p>Khi Gamification đang tắt, trang chỉ còn một công tắc</p></figcaption></figure>
{% endstep %}

{% step %}
**Bật Gamification**

Bật công tắc **Gamification**. Hệ thống bắt đầu ghi nhận: cộng điểm, trao huy hiệu, xét hạng và tính bảng xếp hạng. Công tắc **Visibility in UpLMS** và bốn khối chức năng hiện ra bên dưới.

<figure><img src="../../.gitbook/assets/gamification-cau-hinh.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Bật hiển thị cho học viên**

Bật công tắc **Visibility in UpLMS** để học viên nhìn thấy điểm, huy hiệu, hạng và bảng xếp hạng trên UpLMS.

Lần đầu bật công tắc này, hệ thống hiện popover xác nhận. Đây là thời điểm ra mắt: toàn bộ học viên thấy ngay mọi thứ đã tích luỹ trước đó, và hệ thống **không gửi thông báo** cho những thành tích đã có.
{% endstep %}
{% endstepper %}

Hai công tắc tạo ra ba trạng thái:

| Trạng thái | **Gamification** | **Visibility in UpLMS** | Hệ thống làm gì |
| --- | --- | --- | --- |
| Tắt hẳn | Tắt | (không hiện) | Không ghi nhận, học viên không thấy gì |
| Chạy ngầm | Bật | Tắt | Ghi nhận đầy đủ, học viên chưa thấy gì và không nhận thông báo |
| Bật đầy đủ | Bật | Bật | Ghi nhận và hiển thị cho học viên |

</details>

<details>

<summary>Chạy ngầm trước khi ra mắt</summary>

Nên chạy ngầm 2 đến 4 tuần trước khi mở cho học viên:

1. Bật **Gamification**, để **Visibility in UpLMS** tắt.
2. Cấu hình bốn khối chức năng, xem [Cấu hình Gamification](cau-hinh-gamification.md).
3. Theo dõi điểm thật của học viên ở danh sách học viên và nhật ký ghi nhận, xem [Tra cứu học viên và nhật ký](tra-cuu-hoc-vien-va-nhat-ky.md).
4. Chỉnh số điểm và mức lên hạng cho phù hợp với nhịp học thực tế.
5. Bật **Visibility in UpLMS** để ra mắt.

{% hint style="info" %}
Đổi cấu hình trong lúc chạy ngầm cũng chỉ áp dụng cho các lần ghi nhận sau đó. Điểm đã ghi theo cấu hình cũ giữ nguyên.
{% endhint %}

</details>

<details>

<summary>Tắt Gamification</summary>

Tắt công tắc **Gamification**, hệ thống hiện popover xác nhận cạnh công tắc. Chọn xác nhận để tắt, chọn huỷ thì công tắc giữ nguyên.

Khi tắt:

* Hệ thống ngừng ghi nhận mọi thứ. Học viên không thấy Gamification trên UpLMS.
* Bốn khối chức năng khoá lại, giữ nguyên giá trị đã cấu hình.
* Dữ liệu đã có giữ nguyên. Danh sách học viên, nhật ký ghi nhận và kết quả campaign vẫn xem được.
* Campaign đang chạy không nhận thêm gì trong thời gian tắt.

Bật lại thì hệ thống chỉ tính từ lúc bật. Khoảng thời gian tắt **không được tính bù**, chuỗi ngày vào học của học viên bắt đầu lại từ đầu.

</details>

<details>

<summary>Phân quyền</summary>

Quản trị gán quyền tại màn phân quyền hiện có của Ops, trong nhóm quyền **Gamification**.

| Màn hoặc thao tác | Xem cấu hình gamification | Sửa cấu hình gamification | Xem danh sách học viên và hạng |
| --- | --- | --- | --- |
| Xem trang cấu hình | Có | Có | Không |
| Sửa cấu hình, bật tắt | Không | Có | Không |
| Xem danh sách campaign | Có | Có | Có |
| Tạo, sửa, xoá campaign | Không | Có | Không |
| Xem và xuất kết quả campaign | Không | Không | Có |
| Xem và xuất danh sách học viên | Không | Không | Có |
| Xem nhật ký ghi nhận | Không | Không | Có |

Một vai trò có thể được gán nhiều quyền. Không có quyền nào trong ba quyền trên thì vai trò đó không thấy mục **Gamification** trên menu Ops.

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. Trang cấu hình **tự lưu, không có nút Save**. Ô nhập số lưu khi rời ô hoặc bấm Enter, công tắc lưu ngay khi bấm. Lưu xong có báo nhỏ **Saved**.
2. Mọi thay đổi có hiệu lực ngay và chỉ áp dụng từ thời điểm lưu trở đi. Điểm, huy hiệu, hạng học viên đã nhận không bị tính lại hay lấy lại.
3. Chỉ hai thao tác cần xác nhận: tắt **Gamification** và bật **Visibility in UpLMS** lần đầu. Các công tắc khác lưu ngay khi bấm, không hỏi lại.
4. Ngày và chuỗi ngày vào học tính theo múi giờ của tổ chức (UTC+7).
5. Tài khoản kiểm thử (**Test Account**) không phát sinh dữ liệu gamification và không xuất hiện trên bảng xếp hạng.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống | Nguyên nhân | Cách xử lý |
| --- | --- | --- |
| Không thấy mục **Gamification** trên menu | Tài khoản chưa được gán quyền nào trong nhóm Gamification | Liên hệ quản trị để được gán quyền |
| Thấy trang cấu hình nhưng không bấm được công tắc | Tài khoản chỉ có quyền **Xem cấu hình gamification** | Liên hệ quản trị nếu cần quyền sửa |
| Không thấy công tắc **Visibility in UpLMS** | **Gamification** đang tắt | Bật **Gamification** trước |
| Học viên báo không thấy Gamification | **Visibility in UpLMS** đang tắt, hoặc tài khoản là tài khoản kiểm thử | Kiểm tra công tắc và trường **Test Account** của học viên |
| Học viên hỏi vì sao không có điểm trong những ngày Gamification tắt | Thời gian tắt không được ghi nhận và không tính bù | Đây là quy tắc của hệ thống. Tránh tắt **Gamification** khi không cần thiết |
