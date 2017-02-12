# SQL Injection Lab Level 1

Thực hiện : Hà Ngọc Khuê

## 1 Lỗi 

Ta thêm ' vào sau URL ta thấy xuất hiện lỗi SQLI

Sau khi thử một số cách ta nhận biết được đó là lỗi Không kiểm tra ký tự thoát truy vấn 

Đây là dạng lỗi SQL injection xảy ra khi thiếu đoạn mã kiểm tra dữ liệu đầu vào trong câu truy vấn SQL. 

Kết quả là người dùng cuối có thể thực hiện một số truy vấn không mong muốn đối với cơ sở dữ liệu của ứng dụng. Dòng mã sau sẽ minh họa lỗi này:

``statement = "SELECT * FROM users WHERE name = '" + userName + "';"``

Câu lệnh này được thiết kế để trả về các bản ghi tên người dùng cụ thể từ bảng những người dùng. Tuy nhiên, nếu biến "userName" được nhập chính xác 
theo một cách nào đó bởi người dùng ác ý, nó có thể trở thành một câu truy vấn SQL với mục đích khác hẳn so với mong muốn của tác giả đoạn mã trên. 
Ví dụ, ta nhập vào giá trị của biến root như sau:

``a' or 't'='t``

Khiến câu truy vấn có thể được hiểu như sau:

``SELECT * FROM users WHERE name = 'a' or 't'='t';``

Lúc đó nó sẽ in ra toàn bộ dữ liệu không mong muốn trong database

<img src="http://sv1.upsieutoc.com/2017/02/12/Untitled4bfaf.png" alt="Untitled4bfaf.png" border="0" />

## 2 Khắc phục 

Để khắc phục lỗi trên, ta cần xử lý các biến trong mã PHP bằng cách sử dụng hàm addslashes(): nó sẽ thêm dấu gạch chéo `\` vào trước các ký tự nháy đơn, nháy kép, null, gạch chéo.

Trước khi khác phục 

<img src="http://sv1.upsieutoc.com/2017/02/12/Untitled1.png" alt="Untitled1.png" border="0" />

Sau khi khác phục 

<img src="http://sv1.upsieutoc.com/2017/02/12/Untitled2.png" alt="Untitled2.png" border="0" />

Đây là 2 host 

[Lỗi](http://trainphp.pe.hu/)

[Đã Fix](http://trainphp.pe.hu/dafix.php)
