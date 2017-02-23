### Level 2

Khi ta truy xuất dữ liệu từ sever có dấu cách thì xuất hiện lỗi , còn bỏ dấu cách không sử dụng thì không xuất hiện lỗi .

<img src="http://sv1.upsieutoc.com/2017/02/23/EX2.png" alt="EX2.png" border="0" />

Vậy người lập trình đã xử lí việc kiểm tra dữ liệu đầu vào khi chúng ta nhập vào sao cho sẽ báo lỗi nếu như trong cú pháp truy xuất dữ 
liệu của chúng ta có dấu cách

Trong PHP có một số hàm dùng để xử lý so khớp với dữ liệu xem dữ liệu truyền vào có hợp lệ hay không 
Trong đó có hàm preg_match() được dùng để kiểm tra, so khớp và lấy kết quả của việc so sánh chuỗi dựa vào biểu thức chính quy Regular Expression, hàm này có ba tham số và có cú pháp như sau:

preg_match ( $pattern , $subject, &$matches)

Trong đó:
<ul>
	<li>$pattern là biểu thức Regular Expression</li>
	<li>$subject là chuỗi cần kiểm tra</li>
	<li>$matches là kết quả trả về, đây là một tham số truyền vào ở dạng tham chiếu.</li>
</ul>
Chúng ta có thể bỏ qua $matches vì nó là một tham số thứ 3 nên không cần truyền vào cũng được 

Ta chỉ cần thêm cậu lệnh vào như thế này 

<img src="http://sv1.upsieutoc.com/2017/02/23/ex2-1.png" alt="ex2-1.png" border="0" />

[Demo lỗi](http://trainphp.pe.hu/testex2.php)
[Fix lỗi](http://trainphp.pe.hu/dafix.php)
