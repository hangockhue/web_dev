Thực hiện : Khuê

# Tìm hiểu về HTML

[1.HTML là gì](#htmllagi)
  
[2.Các thẻ định dạng văn bản](#tagvanban)
<dl>  
<dd>[a.Thẻ tiêu đề](#tieude)</dd>
  
<dd>[b.Văn bản](#vanban)</dd>
  
<dd>[c.Danh sách](#danhsach)</dd>
  
<dd>[d.Các thẻ khác](#thekhac)</dd>
</dl>
[3.Thuộc tính của các thẻ](#thuoctinh)

[4.Thẻ thông tin webside](#thongtin)
### 1.HTML là gì :

HTML viết tắt của Hyper Text Markup Language là ngôn ngữ đánh dấu siêu văn bản dùng để tạo một trang web trên một website mỗi trang được gọi là một tài liệu website 

Một tài liệu HTML được tạo bởi cái phần tử HTML được gọi là các cặp thẻ trong HTML . Thường thì các thẻ sẽ đi theo từng cặp nhưng có một số thẻ không có thẻ đóng . 

Mỗi tập tin HTML sẽ được lưu lại với đuôi mở rộng `.html` hoặc `.htm`

HTML là bộ xương của website đống vai trò khai báo siêu văn bản cho website còn chỉnh sửa giao diện thuộc về CSS,JavaScrip.....

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

### 3.Thuộc tính của các thẻ :

Thuộc tính của các thẻ là phần mở rộng của các thẻ để chỉnh sửa phần văn bản hay siêu văn bản nằm trong các thẻ đó 

Thuộc tính của thẻ có dạng như sau `<thẻ thuộctính="giátrị"> nội dung </thẻ>` trong một thẻ thì có thể có nhiều thuộc tính ngăn cách nhau bởi một ký tự trống.

Ta có các thuộc tính thường sử dụng như : 

`align="giátrị"` dịch chuyển văn bản theo chiều ngang với giá trị là left , right , center

`valign` dịch chuyển văn bản theo chiều dọc với các giá trị là top, middle, bottom 

`width` Xác định độ rộng của bảng, hình ảnh, video, hoặc ô trong bảng... với giá trị là số px

`height` Xác định độ cao của bảng, hình ảnh, video, hoặc ô trong bảng... với giá trị là số px 

`title` "Pop-up" tiêu đề của phần tử với giá trị là người dùng tự định nghĩa 


