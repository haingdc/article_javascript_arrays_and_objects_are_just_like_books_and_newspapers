Javascript: Mảng và đối tượng - như sách với báo

Nếu bạn đã bao giờ đọc sách và báo, bạn có thể hiểu được điểm mà mảng và đối tượng khác nhau.

Khi viết một chương trình, một trong các vấn đề chính mà mỗi chúng ta sẽ bắt gặp là chọn cách phù hợp để tổ chức và lưu trữ dữ liệu.

Mảng và Đối tượng là 2 trong số các dạng dữ liệu cơ bản trong Javascript.

> Có bao giờ bạn thắc mắc nên tổ chức dữ liệu theo mảng hay đối tượng?

Nhận biết được đặc điểm của 2 cấu trúc này sẽ giúp dễ dàng hơn trong việc lựa chọn thời điểm sử dụng chúng. Thông qua sự minh họa giữa mảng và đối tượng với cách mà sách báo chứa thông tin, bài viết sẽ trả lời cho câu hỏi trên.

# Mảng: Thứ tự dữ liệu là quan trọng nhất

Dưới đây là các chương của một cuốn sách, ở dạng mảng.

```js
var book = ['foreword', 'boyWhoLived', 'vanishingGlass', 'lettersFromNoOne', 'afterword'];
```

![first_Harry_Potter_book](E:/repository/other/groking_algorithm/javascript_arrays_and_objects_are_just_like_books_and_newspapers/book.png)

Bạn muốn sử dụng mảng khi thứ tự là tiêu chí hàng đầu cho việc tổ chức dữ liệu. Để bắt đầu đọc một cuốn sách, đa phần chúng ta sẽ chọn cách đọc từ đầu tới cuối hơn là, xem mục lục, chọn tiêu đề ta thấy thú vị nhất và tiếp cận chương đó trước tiên.

Các phần tử của mảng cũng tương tự như các chương trong một cuốn sách. Để tìm đến chỉ mục đầu tiên, bạn sẽ sử dụng:

`book[2]`

Và thu được:

`‘foreword’`

Hay muốn biết tiêu đề của chương 3, bạn sẽ dùng:

`book[2]`

Bạn chọn chương tiếp theo để đọc dựa trên thứ tự của cuốn sách, thay vì dựa trên tiêu đề của chương.

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

Nó sẽ trở lại cho ta giá trị *‘GE Stock Dips Again’*. Vì vậy, nếu muốn dễ dàng lấy ra dữ liệu phân theo **chủ đề (khóa)**, bạn có thể tổ chức dữ liệu ở dạng đối tượng.

# Kết hợp giữa đối tượng và mảng

Ở phần trên, chúng ta đã lưu các chuỗi vào trong mảng và đối tượng. Thêm vào đó, chúng ta cũng có thể lưu các kiểu dữ liệu khác như số, boolean, hay thậm chí lưu:

1. các mảng bên trong đối tượng
2. các đối tượng bên trong mảng
3. các mảng bên trong mảng
4. các đối tượng bên trong đối tượng

Trở lại ví dụ về sách ở trên. Làm thế nào nếu chúng ta cũng muốn lưu thông về số lượng trang ở mỗi chương?

Ở đây chúng ta phải đảm bảo thứ tự của các chương và thêm thông tin về số lượng trang cho mỗi một chương.

🤔 Bạn sẽ muốn lưu theo kiểu nào trong 2 kiểu sau?

```js
var book =[
  [‘foreword’, 14],
  [‘boywholived’, 18],
  [‘vanishingGlass’, 13],
  [‘lettersFromNoOne’, 17],
  [‘afterword’, 19]
]
```

hay

```js
var book = [
  {name:'foreword', pageCount: 14},
  {name:'boyWhoLived', pageCount: 18},
  {name:'vanishingGlass', pageCount: 13},
  {name:'lettersFromNoOne', pageCount: 17},
  {name:'afterword', pageCount: 19}
];
```

Thực tế, ta có thể chọn cái nào cũng được. Tuy nhiên, để biết số lượng trang của chương hai, ta thấy sử dụng `book[1][‘pageCount’]` sẽ trực quan hơn so với `book[1][1]`.

Giả sử bạn muốn thấy xếp hạng các tác giả hàng đầu dựa theo chủ đề của một tờ báo. Bạn có thể để thông tin về xếp hạng này trong một mảng, bởi vì thứ tự các tác giả là quan trọng. Sau đó đặt nó trong một đối tượng *newspaper* như sau:

```js
var newspaper= {
  sports: 'ARod Hits Home Run',
  sportsWriters: ['Miramon Nuevo', 'Rick Reilly', 'Woddy Paige'],

  business: 'GE Stock Dips Again',
  businessWriters: ['Adam Smith', 'Albert Humphrey', 'Charles Handy'],

  movies: 'Superman Is A Flop',
  moviesWriters: ['Rogert Ebert', 'Andrew Sarris', 'Wesley Morris']
}
```

Mảng sẽ rất phù hợp để lưu các tác giả. Chúng ta sẽ biết rằng tác giả đứng trước sẽ có thứ hạng cao hơn.

Một cách khác, bạn sẽ nhóm tên tiêu đề và các tác giả làm một đối tượng. Ví dụ, đối tượng *sports* sẽ chứa thông tin về tiêu đề và danh sách tác giả. Tôi sẽ để bạn tự thực hiện nhé!

# Vài thách thức cho bạn

1. Giả sử trang web của bạn có phần câu hỏi trắc nghiệm, cho người dùng đưa ra câu trả lời và sau khi hoàn thành sẽ hiển thị kết quả. Với mỗi câu hỏi, bạn muốn lưu câu trả lời của người dùng, sau đó có thể kiểm tra đáp án để biết đúng sai. Liệu bạn sẽ dùng cấu trúc nào để lưu các câu trả lời của người dùng trước khi đem đi kiểm tra? Tại sao?

2. Giả sử bạn cho phép người dùng tạo một trang tiểu sử trên site của mình, với: tên, họ, email và số điện thoại. Bạn muốn lưu thông tin đó trước khi gửi nó tới back end. Vậy cấu trúc nào bạn sẽ sử dụng để lưu những thông tin này? Tại sao?

3. Giả sử bạn đang xây dựng một forum, chức năng cần thực hiện là xếp hạng bình luận dựa vào lượt vote. Cấu trúc nào giúp bạn theo dõi nội dung bình luận VÀ số lượt vote? Gợi ý: có thể kết hợp mảng và đối tượng.

Bài viết được dịch từ nguồn: [medium.freecodecamp.com/javascript-arrays-and-objects-are-just-like-books-and-newspapers](https://medium.freecodecamp.org/javascript-arrays-and-objects-are-just-like-books-and-newspapers-6e1cbd8a1746)