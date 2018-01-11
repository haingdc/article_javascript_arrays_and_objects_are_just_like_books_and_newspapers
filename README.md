Javascript: Mảng và đối tượng chỉ như là sách và báo

Nếu bạn đã bao giờ đọc sách và báo, bạn có thể hiểu được điểm mà mảng và đối tượng khác nhau.

Khi viết một chương trình, một trong các vấn đề chính mà mỗi chúng ta sẽ bắt gặp là chọn cách phù hợp để tổ chức và lưu trữ dữ liệu.

Mảng và Đối tượng là 2 trong số các dạng dữ liệu cơ bản trong Javascript. Nhận biết được đặc điểm của 2 cấu trúc này sẽ giúp dễ dàng hơn trong việc lựa chọn thời điểm sử dụng chúng. Bài viết này sẽ đem tới một góc nhìn khác khi minh họa giữa mảng và đối tượng với cách mà các cuốn sách báo chứa thông tin.

# Mảng: Thứ tự dữ liệu là quan trọng nhất

Dưới đây là các chương của một cuốn sách, dưới dạng mảng.

```js
var book = ['foreword', 'boyWhoLived', 'vanishingGlass', 'lettersFromNoOne', 'afterword'];
```

![first Harry Potter book](https://cdn-images-1.medium.com/max/1500/1*FQ6CJaawGTIB_oa8M-Z7GQ.png)

Bạn muốn sử dụng mảng khi thứ tự là tiêu chí hàng đầu cho việc tổ chức dữ liệu. Để bắt đầu đọc một cuốn sách, đa phần chúng ta sẽ chọn cách lướt qua mục lục rồi nhanh chóng đọc từ đầu tới cuối hơn là, lựa chọn tiêu đề ta thấy thú vị nhất ở mục lục và tiếp cận chương đó trước tiên. Thứ tự của các chương sẽ nói cho bạn biết chương tiếp theo là gì.

Cũng như vậy, khi bạn muốn lấy ra thông tin từ mảng, bạn sẽ dựa trên chỉ mục của nó. Để tìm đến chỉ mục đầu tiên, bạn sẽ sử dụng:

`book[2]`

Và thu được:

`‘foreword’`

Hay muốn biết tiêu đề của chương 3, bạn sẽ dùng:

`book[2]`

Mỗi khi kết thúc một chương, chương tiếp ta đọc tới sẽ dựa trên thứ tự của nó, thay vì dựa trên tên tiêu đề.

