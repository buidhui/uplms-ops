# Tạo hoạt động kiểm tra

## I. Giới thiệu chung

{% hint style="warning" %}
#### Điều kiện tiên quyết

* Khóa học đã được tạo thành công ở bước **Course Info**.
{% endhint %}

## II. Hướng dẫn chi tiết

<details>

<summary>Tạo bài Test</summary>

{% hint style="info" %}
Test là hoạt động kiếm tra, có thể lựa chọn tính điểm và đưa vào điểm thành phần cần để hoàn thành khóa học.
{% endhint %}

Các loại bài Test:

* Section Test

<figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

* Midterm Test
* Final Test

<figure><img src="../../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

{% stepper %}
{% step %}
**Điền thông tin bài Test**

<figure><img src="../../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="180">Tên trường</th><th>Mô tả</th></tr></thead><tbody><tr><td>Name</td><td>Tên bài test</td></tr><tr><td>Type of Test</td><td><p>Loại bài kiểm tra:</p><ul><li>Multiple Choice: dạng trắc nghiệm (Mặc định)</li><li>Constructed: dạng tự luận</li><li>Mixed (Multiple Choice + Constructed): dạng bao gồm cả trắc nghiệm và tự luận</li></ul></td></tr><tr><td>Test Mode</td><td><ul><li>Tutor: làm bài không giới hạn thời gian (Mặc định)</li><li>Timed: giới hạn thời gian làm bài</li></ul></td></tr><tr><td>Manual Grading</td><td><p>Chỉ hiển thị với Type of Test = Constructed hoặc Mixed</p><ul><li>Yes: bài kiểm tra sẽ được chấm điểm thủ công bởi đội vận hành.</li><li>No: bài kiểm tra sẽ được chấm tự động phần trắng nghiệm với loại Mixed và không chấm nếu toàn bộ là tự luận (Constructed)</li></ul></td></tr><tr><td>Graded Assignment</td><td>Đánh dấu bài kiểm tra được sử dụng để tính điểm cho toàn bộ khóa học hay không.</td></tr><tr><td>Grading Preference</td><td><p>Chọn cách hiển thị đáp án và Solution</p><ul><li>After each question: hiển thị sau khi trả lời mỗi câu hỏi</li><li>After all questions: hiển thị sau khi hoàn thành bài Test (Mặc định)</li></ul></td></tr><tr><td>Pass Point</td><td><p>Điểm tiếu thiểu cần đạt để Pass bài Test</p><ul><li>Auto 50%: điểm pass point là 50% (Mặc định)</li><li>Manual: cho phép Admin nhập số điểm pass point</li></ul></td></tr><tr><td>Attempt</td><td><p>Cho phép chọn số lần làm bài</p><ul><li>Unlimited: không giới hạn số lần làm bài (Mặc định)</li><li>Limited: giới hạn số lần làm bài</li></ul></td></tr><tr><td>Total Score</td><td><ul><li>Tổng điểm của bài Test/Quiz, có thể điền khác thang điểm 100.</li><li>Chỉ nhập giá trị lớn hơn 0.</li><li>Phần thập phân tối đa 2 chữ số.</li></ul></td></tr></tbody></table>

{% hint style="info" %}
Khi người dùng chọn Manual Grading = ‘Yes’ thì giá trị của Graded Assignment = ‘Yes’ và Attempt = "1".
{% endhint %}
{% endstep %}

{% step %}
**Thêm câu hỏi vào bài Test**

* Add Question: thêm câu hỏi vào bài Test

<figure><img src="../../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Danh sách câu hỏi hiển thị phụ thuộc vào Type of Test.**

* Type of Test = Multiple Choice: Hệ thống hiển thị toàn bộ câu hỏi trắc nghiệm trên hệ thống.
* Type of Test = Constructed Question: Hệ thống hiển thị toàn bộ câu hỏi tự luận trên hệ thống.
* Type of Test = Mixed: Hệ thống hiển thị cả câu hỏi trắc nghiệm và câu hỏi tự luận.

**Cách sắp xếp:** câu hỏi trắc nghiệm và tự luận có thể hiển thị xen kẽ theo đúng thứ tự tạo.
{% endhint %}

Thứ tự câu hỏi tại bước **Setup Score** và **Reorder** phụ thuộc vào thứ tự người dùng chọn câu hỏi tại bước **Add Question**.

| Trường hợp                                          | Logic hệ thống                                                          |
| --------------------------------------------------- | ----------------------------------------------------------------------- |
| Người dùng chọn đơn lẻ từng câu                     | Câu nào được chọn trước sẽ đứng trước                                   |
| Người dùng chọn toàn bộ câu hỏi trong trang         | Thứ tự câu hỏi giữ nguyên như thứ tự đang hiển thị tại màn Add Question |
| Người dùng chọn một câu, sau đó bỏ chọn và chọn lại | Câu hỏi đó được đưa xuống cuối danh sách                                |

* Setup Score: cài đặt điểm cho từng câu hỏi trong bài Test
* Reorder: sắp xếp thứ tự hiển thị của câu hỏi trong bài Test
{% endstep %}

{% step %}
**Setup Score**

Điểm mặc định chia đều cho tất cả câu hỏi (100/ tổng số câu), nhân sự vận hành có thể cài đặt lại điểm cho từng câu hỏi trong bài Test

<figure><img src="../../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Reorder**

**Có 3 cách để thay sắp xếp lại ví trị câu hỏi**

* Kéo thả từng câu theo thứ tự mong muốn
* Chọn câu hỏi cần thay đổi vị trí → Action → Chọn vị trí muốn chuyển đến (Top/ Bottom/ Vị trí cụ thể)

<figure><img src="../../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

* Chọn nhiều câu hỏi cùng lúc → Button -> Chọn vị trí muốn chuyển đến (Top/ Bottom) (Điều kiện là phải chọn các câu hỏi có thứ tự liền kề nhau)
{% endstep %}

{% step %}
**Sau khi hoàn tất sắp xếp câu hỏi, chọn Finish**

Điều hướng quay lại màn hình Test Detail
{% endstep %}

{% step %}
**Chọn Save để hoàn thành tạo bài Test**
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Chỉnh sửa bài Test</summary>

{% hint style="info" %}
Nếu bài Test đã có người làm, người dùng chỉ xem thông tin và chỉ có thể chỉnh sửa thông tin:

* Tên bài Test
* Thứ tự hiển thị câu hỏi trong bài Test tại bước **Reorder**
{% endhint %}

{% stepper %}
{% step %}
**Truy cập vào bài Test cần chỉnh sửa**

Có thể chỉnh sửa các thông tin sau, thao tác tương tự tạo mới.

* Thông tin chung của bài Test.
* Danh sách câu hỏi thông qua **Configure Questions**.
* Điểm của từng câu hỏi tại bước **Setup Score**.
* Thứ tự câu hỏi tại bước **Reorder**.
{% endstep %}

{% step %}
**Sau khi hoàn tất việc chỉnh sửa, chọn Save để lưu thay đổi**
{% endstep %}
{% endstepper %}

</details>

<details>

<summary>Tạo mới và chỉnh sửa Quiz</summary>

{% hint style="info" %}
Quiz là hoạt động ôn tập nằm trong các hoạt động học (Learning Activity), vẫn có thể cài đặt tính điểm hoàn thành Quiz nhưng không dùng để tính hoàn thành khóa học.
{% endhint %}

Các bước tạo và chỉnh sủa Quiz tương tự như Test, chỉ khác một số trường thông tin

<figure><img src="../../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

* Quiz chỉ có dạng trắc nghiệm
* Quiz có trong hoạt động học và trong Video của hoạt động học (tham khảo [#video](tao-cau-phan-hoc-section-subsection-unit-activity.md#video "mention"))

</details>

## III. Lưu ý & Quy tắc nghiệp vụ

{% hint style="warning" %}
### Lưu ý quan trọng

1. **Type of Test** quyết định danh sách câu hỏi được hiển thị tại bước Add Question.
2. Với **Constructed/Mixed**, trường **Manual Grading** được hiển thị.
3. Với **Test** nếu **Manual Grading = Yes** thì **Graded Assignment = Yes** và **Attempt = 1**
4. Chỉ có thể di chuyển nhiều câu hỏi cùng lúc khi các câu hỏi được chọn nằm liền kề nhau.
5. Nếu bài Test đã có học viên làm, Admin chỉ được chỉnh sửa tên bài Test và thứ tự câu hỏi.
{% endhint %}

{% hint style="info" %}
### Mẹo sử dụng

1. Nên kiểm tra lại thứ tự câu hỏi tại bước **Reorder** trước khi bấm **Finish**.
{% endhint %}

## IV. Các lỗi thường gặp & Hướng dẫn xử lý

| Lỗi / Tình huống                       | Nguyên nhân                                                    | Cách xử lý                                                               |
| -------------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Không tạo được Test/ Quiz              | Tài khoản chưa có quyền hoặc chưa truy cập đúng Course Content | Kiểm tra quyền tài khoản và vị trí tạo bài Test                          |
| Không thấy câu hỏi cần chọn            | Type of Test không phù hợp với loại câu hỏi                    | Kiểm tra lại Type of Test hoặc tạo câu hỏi đúng loại trong Question Bank |
| Không tìm thấy câu hỏi                 | Bộ lọc đang quá hẹp hoặc dữ liệu Question Bank chưa có         | Chọn Reset hoặc kiểm tra dữ liệu Question Bank                           |
| Không chuyển được sang Reorder         | Total Score sau khi điều chỉnh có tồng chưa bằng 100.          | Kiểm tra lại Total Score ở bước Setup Score                              |
| Không di chuyển được nhiều câu hỏi     | Các câu hỏi được chọn không liền kề                            | Chọn các câu hỏi liền kề nhau                                            |
| Không chỉnh sửa được danh sách câu hỏi | Bài Test đã có học viên làm                                    | Chỉ xem thông tin hoặc chỉ chỉnh sửa các trường được phép                |
| Thay đổi chưa được lưu                 | Chưa bấm Save ở màn Test/ Quiz Detail                          | Bấm Save sau khi hoàn tất thao tác                                       |
