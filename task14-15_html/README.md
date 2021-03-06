Thực hiện : Khuê
Update : 12/11
# Tìm hiểu về HTML

[1.HTML là gì](#htmllagi)
  
[2.Các thẻ định dạng văn bản](#tagvanban)
<ul>  
<li>a.Thẻ tiêu đề</li>
<li>b.Văn bản </li>  
<li>c.Danh sách </li>
<li>d.Các thẻ khác </li>
</ul>

[3.Thuộc tính của các thẻ](#thuoctinh)

[4.Thẻ thông tin webside](#thongtin)

[5.Tạo form nhập dữ liệu](#form)
<a name = "htmllagi"></a>
### 1.HTML là gì :

HTML viết tắt của Hyper Text Markup Language là ngôn ngữ đánh dấu siêu văn bản dùng để tạo một trang web trên một website mỗi trang được gọi là một tài liệu website 

Một tài liệu HTML được tạo bởi cái phần tử HTML được gọi là các cặp thẻ trong HTML . Thường thì các thẻ sẽ đi theo từng cặp nhưng có một số thẻ không có thẻ đóng . 

Mỗi tập tin HTML sẽ được lưu lại với đuôi mở rộng `.html` hoặc `.htm`

HTML là bộ xương của website đống vai trò khai báo siêu văn bản cho website còn chỉnh sửa giao diện thuộc về CSS,JavaScrip.....
<a name = "tagvanban"></a>
### 2.Các thẻ định dạng văn bản 

Các thẻ được viết dưới dạng : `<thẻ> nội dung </thẻ>`

TĐối với thẻ ko đi theo cặp : `<thẻ> nội dung />`

#### a.Thẻ tiêu đề :

Trong HTML hổ trợ 6 thẻ tiêu đề : `<h1></h1> , <h2></h2> , <h3></h3> , <h4></h4> , <h5></h5> , <h6></h6>` 

Nếu bạn dùng h7 trở lên nó sẽ thành dạng text bình thường . Ví dụ :
<img src ="http://sv1.upsieutoc.com/2016/12/10/html1.png">

#### b.Văn bản 

Để khai báo một đoạn văn bản ta dùng thẻ : `<p></p>`

Để in đậm một nội dung ta dùng thẻ : `<strong></strong>`

Để in nghiêng một nội dung ta dùng : `<i></i>`

Để gạch chân một nội dung ta dùng : `<u></u>`

Để gạch ngang một nội dung ta dùng : `<strike></strike>`

Gạch gang : `<hr>`

Câu trích dẫn : `<quote></quote>`

Thẻ định dạng sẵn : `<pre></pre>`

Khai báo những đoạn code ngắn : `<code></code>`

Ghi chú trong HTML : `<!-- nội dung -->`


Xem thêm 1 số thẻ ở [đây](http://hocwebchuan.com/reference/tag/)

Ví dụ :
<img src ="http://sv1.upsieutoc.com/2016/12/10/html2.png">
#### c.Danh sách trong HTML 

Để khai báo danh sách ta dùng thẻ : `<ol></ol>`

Trong thẻ `<ol></ol>` ta có thẻ `<li></li>` dùng để khai báo danh mục trong danh sách đó.

Ngoài thẻ `<ol></ol>` ta còn có thẻ `<ul></ul>` không có sắp xếp còn thẻ `<ol></ol>` thì có sắp xếp 

Đối với danh sách có mô tả ta dùng thẻ `<dl></dl>` nhưng trong thẻ này ta không dùng thẻ `<li></li>` mà ta sử dụng thẻ `<dt></dt>` để khai báo danh mục và dùng thẻ `<dd></dd>` để khai báo mô tả cho danh mục 

Ví dụ :
<img src ="http://sv1.upsieutoc.com/2016/12/10/html3.png">

#### d.Các thẻ khác

Chèn thêm ảnh ta có thẻ `<img src =" Đường dẫn của ảnh"/>`

Để chèn video ta có thẻ `<video></video>` trong thẻ đó ta khai báo đường dẫn bằng thẻ `<source src="Đường dẫn />`

Để chèn audio ta có thẻ `<audio></audio>` trong thẻ đó ta khai báo đường dẫn bằng thẻ `<source src="Đường dẫn />`

Để chèn một website ta có thẻ `<iframe src="link"></iframe>`

Đề chèn link vào một nội dung ta có thẻ `<a href="link">nội dung</a>`

Ví dụ :

<img src="http://sv1.upsieutoc.com/2016/12/10/html4.png">

<a name = "thuoctinh"></a>
### 3.Thuộc tính của các thẻ :

Thuộc tính của các thẻ là phần mở rộng của các thẻ để chỉnh sửa phần văn bản hay siêu văn bản nằm trong các thẻ đó 

Thuộc tính của thẻ có dạng như sau `<thẻ thuộctính="giátrị"> nội dung </thẻ>` trong một thẻ thì có thể có nhiều thuộc tính ngăn cách nhau bởi một ký tự trống.

Ta có các thuộc tính thường sử dụng như : 

`align="giátrị"` dịch chuyển văn bản theo chiều ngang với giá trị là left , right , center

`valign` dịch chuyển văn bản theo chiều dọc với các giá trị là top, middle, bottom 

`width` Xác định độ rộng của bảng, hình ảnh, video, hoặc ô trong bảng... với giá trị là số px

`height` Xác định độ cao của bảng, hình ảnh, video, hoặc ô trong bảng... với giá trị là số px 

`title` "Pop-up" tiêu đề của phần tử với giá trị là người dùng tự định nghĩa 

`style` có thẻ thay đổi các thuộc tính của văn bản như màu chữ với giá trị trong bảng [mã](http://www.w3schools.com/cssref/css_colors.asp) với tên khai báo là `color` , thay đổi màu nền của nội dung với giá trị là mã màu tên là `background-color`, tiếp theo là `font-size` dùng để thay đổi kích thước chữ với giá trị là số px và `font-family` để thay đổi font chữ của nội dung 

Ví dụ của thuộc tính `style` : `<p style="color: mãmàu; font-size=nãmàu>nội dung</p>` trong thuộc tính style có nhiều giá trị được chia ra bởi dấu `:` 

`target` thuộc tính cho phép thiết lập cửa sổ liên kết có các giá trị là `_blank` ,`_self` 

`id` đặt tên một phần tử để sử dụng với Cascading Style Sheets có giá trị là người dùng tự đặt dùng để đánh dấu một dòng muốn nhảy để với khai báo ta dùng thẻ `<a hef="giátrị">nội dung</a>`

`charset` dùng để khai báo bảng mã sử dụng với giá trị là bảng mã

`name` là khai báo tên mô tả và `content` là khai báo nội dung mô tả đó 
<a name = "thongtin"></a>
### 4 Thẻ thông tinh website:

Những thẻ này không giúp hiển thị trên một trang web mà chỉ tạo nên thông tin của trang web đó 

Thẻ đầu tiên trong tài liệu HTML là thẻ `<!DOCTYPE html>`

Thẻ tiếp theo là thẻ `<html></html>` trong thẻ này có một thuộc tính là `lang` để chỉ ra mã ngôn ngữ mà website sử dụng và cái thẻ này là bao bọc toàn bộ nội dung của website 

Tiếp theo là thẻ `<head></head>` khai báo thông tin của website ở trong này , trong này có thẻ `<title></title>` dùng để khai báo tên website của bạn 

Thẻ `<meta />` trong thẻ này có thuộc tính dùng để khai báo bảng mã mà chúng ta sử dụng trong trang web như : thuộc tính `charset` dùng để khai báo bảng mã sử dụng với giá trị là bảng mã ; `name` có giá trị là description là mô tả tài liệu và `content` dùng để khai báo mô ta cho nó ;

Thẻ `<body></body>` thẻ này sẽ chứa toàn bộ nội dung của trang web của bạn 


<a name = "form"></a>
### 5.Tạo form nhập dữ liệu 

Tạo một cái form nhập dữ liệu cho html tạo ra một cái form để gửi đi dữ liệu như form đăng nhập , đăng kí ....

Thẻ khai báo form là : `<form></form>` trong thẻ này có những thuộc tính phải có như `action` dùng để khai báo đường dẫn khi người dùng bấm phim submit(gửi dữ liệu đi) ; thuộc tính `method` nghĩa là khai báo dữ liệu gửi đi theo phương thức nào có 2 giá trị là `post` và `get` ; thuộc tính nữa đó là `name` là tên của form với giá trị là người dùng tự đặt .

Trong form phải có các trường nhập dữ liệu , để khai báo trường nhập dữ liệu ta có thẻ `<input />` trong thẻ này có các thuộc tính là `type` là loại dữ liệu nhập vào với các giá trị như `number` , `color`  , `date` ,`email`, `text` ... ;  thuộc tính `name` là khai báo tên của trường dữ liệu  

Và để gửi đi bạn dùng thuộc tính `submit` trong thẻ `<input />` để đặt tên cho gửi đi bạn dùng thuộc tính `value` 

Ví dụ như : 
<img src="http://sv1.upsieutoc.com/2016/12/11/html5.png">






