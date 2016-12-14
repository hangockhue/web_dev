## Ở phiên bản HTML5 có thêm một số thẻ mới ví dụ như:

Các thẻ `<hearder`, `<nav>` , `<article>` , `<asite>`, `<footer>` dùng để phân bố vị trí nội dung trong 1 trang web, `<section>` dùng để định nghĩa một vùng 

Vị trí các thẻ như sau :

<img src="http://sv1.upsieutoc.com/2016/12/14/html6.png">

Cung cấp các thẻ như `<mark>` để làm nổi bật nội dung , thẻ `<summary>` xác định một tiêu đề cho các thành phần details, được sử dụng để mô tả chi tiết về tài liệu, hoặc các bộ phận của tài liệu và thẻ `<details>` xác định thêm chi tiết hoặc điều khiển có thể được ẩn hoặc hiển thị theo yêu cầu. Thẻ `<meter>` định nghĩa cho một phép đo , cho giá trị tối thiểu hoặc tối đa 

<img src="http://sv1.upsieutoc.com/2016/12/14/html7.png">

Thẻ `<embed>` thường dùng để nhúng một nội dung chứa plugin hoặc để chèn flash , thẻ `<figuare>` dùng để khoanh vùng những nội dung liền mạch liên quan với nhau , thẻ `<output>` thường được dùng để xuất giá trị như là kết quả phép tính và dùng gắn liền với thẻ `<input>` để nhập giá trị 

Ví dụ bạn có thể tạo ra một form tính phép cộng với thẻ input và output như sau :
```
<form action="">
<input name="num01" type="number" /> + <input name="num02" type="number" /> = <output name="result" onforminput="value=num01.valueAsNumber + num02.valueAsNumber">
</output>
</form>
```

Nếu bạn muốn thể hiện một quá trình đang load dữ liệu hay hoạt động thì html5 có hổ trợ thẻ `<progress>` để thể thiện quá trình đó nhập đoạn code này và thấy kết quả `<p>Quá trình download được: <progress>90%</progress></p>`

HTML5 cung cấp các thẻ `<audio>` hay `<video>` để định nghĩa các siêu văn bản nằm trong thẻ đó .

Các thẻ hổ trợ việc nhập dữ liệu như `<keygen>` xác định một cặp trường khóa chính sử dụng cho `<form>`.
Khi `<form>` được submit các khoá riêng (private key) được lưu trữ tại địa phương, và các khóa chung được gửi (public key) đến máy chủ

Và `<datalist>` định nghĩa một danh sách tùy chọn.
Tag `<datalist>` được sử dụng cùng với các thành phần `<input />` nhằm xác định giá trị các thành phần `<input />` có thể có (tương tự như `<select> - <option>`).
Sử dụng thuộc tính list trong `<input />` để cho biết thành phần `<input />` nào liên quan đến `<datalist>`.

Ta có một số ví dụ như : 

<img src ="http://sv1.upsieutoc.com/2016/12/14/html8.png">
