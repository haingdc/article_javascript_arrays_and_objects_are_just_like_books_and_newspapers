Javascript: Mảng và đối tượng chỉ như là sách và báo

Nếu bạn đã bao giờ đọc sách và báo, bạn có thể hiểu được điểm mà mảng và đối tượng khác nhau.

Khi viết một chương trình, một trong các vấn đề chính mà mỗi chúng ta sẽ bắt gặp là chọn cách phù hợp để tổ chức và lưu trữ dữ liệu.

Mảng và Đối tượng là 2 trong số các dạng dữ liệu cơ bản trong Javascript. Nhận biết được đặc điểm của 2 cấu trúc này sẽ giúp dễ dàng hơn trong việc lựa chọn thời điểm sử dụng chúng. Bài viết này sẽ đem tới một góc nhìn khác khi minh họa giữa mảng và đối tượng với cách mà các cuốn sách báo chứa thông tin.

# Mảng: Thứ tự dữ liệu là quan trọng nhất

Dưới đây là các chương của một cuốn sách, dưới dạng mảng.

```js
var book = ['foreword', 'boyWhoLived', 'vanishingGlass', 'lettersFromNoOne', 'afterword'];
```

![first_Harry_Potter_book](E:/repository/other/groking_algorithm/javascript_arrays_and_objects_are_just_like_books_and_newspapers/book.png)

Bạn muốn sử dụng mảng khi thứ tự là tiêu chí hàng đầu cho việc tổ chức dữ liệu. Để bắt đầu đọc một cuốn sách, đa phần chúng ta sẽ chọn cách lướt qua mục lục rồi nhanh chóng đọc từ đầu tới cuối hơn là, lựa chọn tiêu đề ta thấy thú vị nhất ở mục lục và tiếp cận chương đó trước tiên. Thứ tự của các chương sẽ nói cho bạn biết chương tiếp theo là gì.

Cũng như vậy, khi bạn muốn lấy ra thông tin từ mảng, bạn sẽ dựa trên chỉ mục của nó. Để tìm đến chỉ mục đầu tiên, bạn sẽ sử dụng:

`book[2]`

Và thu được:

`‘foreword’`

Hay muốn biết tiêu đề của chương 3, bạn sẽ dùng:

`book[2]`

Mỗi khi kết thúc một chương, chương tiếp ta đọc tới sẽ dựa trên thứ tự của nó, thay vì dựa trên tên tiêu đề.

# Đối tượng: Tên khóa là quan trọng nhất

```js
var newspaper= {
  sports: 'ARod Hits Home Run',
  business: 'GE Stock Dips Again',
  movies: 'Superman Is A Flop'
}
```

![newspaper](E:/repository/other/groking_algorithm/javascript_arrays_and_objects_are_just_like_books_and_newspapers/newspaper.png)

Các đối tượng sẽ phù hợp khi bạn muốn **tổ chức dữ liệu theo các chủ đề**. Khi bạn đọc một tờ báo, chúng ta thường không hay đọc từ trang trước tới trang sau. Ưu tiên là thường đọc ở những chủ đề mà bản thân quan tâm. Không quan trọng nó nằm ở đâu, chúng ta chỉ muốn tìm tới trang có vấn đề hấp dẫn mình.

Các đối tượng cũng như vậy, chúng tổ chức thông tin theo từng cặp **khóa/giá trị**.

Nếu bạn muốn xem thông tin về chủ đề tài chính, bạn sẽ sử dụng:

`newspaper[‘business’]`

hoặc

`newspaper.business`

Nó sẽ trở lại cho ta giá trị *‘GE Stock Dips Again’*. Vì vậy, nếu muốn dễ dàng lấy ra dữ liệu phân theo **chủ đề/từ khóa**, bạn có thể tổ chức dữ liệu ở dạng đối tượng.