### 1 .SQLI hay còn gọi là SQL injection 
là một kỷ thuật cho phép lợi dụng lỗ hổng của việc kiểm tra dữ liệu đầu vào trong các ứng dụng web và các thông báo lỗ của hệ quản trị cơ sở dữ liệu trả về để inject(tiêm vào) và thi hành các câu lệnh SQL bất hợp pháp . SQL injection có thể cho phép những kẻ tấn công thực hiện các thao tác : DELETE , INSERT , UPDATE ... trên cở sở dữ liệu của ứng dụng thậm chí là server mà ứng dụng đó đang chạy . SQLI thường được biết đến như một vật trung gian tấn công trên các ứng dụng web có dữ liệu được quản lý bằng các hệ quản trị cơ sở dữ liệu như SQL Server , MySQL , Oracle , DB2 , Sysbase ...

SQLI xãy ra khi có lỗ hổng bảo mật SQLI , một trong những lỗ hổng bảo mật và quy hiểm nhất 

Tác hại của SQLI 

- Có thể gây ra thiệt hại khổng lồ , với SQLI hacker có thể truy cập một phần hoặc toàn bộ dữ liệu trong hệ thống 

- Khi bị truy cập dữ liệu thì hacker có thể xem , chỉnh sửa hay xóa toàn một phần hoặc toàn bộ dữ liệu .

- Khai thác Sql Injection, ngoài việc đoạt được quyền kiểm soát về mặt dữ liệu như đã nói ở trên, hacker còn có thể cài đặt backdoor trên server mà ứng dụng đang chạy, qua đó kiểm soát toàn bộ hệ thống…

### 2.IMFORMATION_SCHEMA trong MySQL 
là cơ sở dữ liệu thông tin , tại đây lưu trữ các thông tin của các cơ sở dữ liệu khác của MySQL . Trong cơ sỡ dữ lieeuuj INFORMATION_SCHEMA chứa một vài bẳng có thuộc tính chỉ đọc . Chúc thực ra chỉ là cái view , không phải là bảng dữ liệu , vì vậy mà không có các file lưu trữ riêng( các bảng đều có các file chứa dữ liệu của bảng nằm trên ổ đĩa) . Cũng chính vì các view mà người dùng không thể thiết lập các Trigger ( các câu lệnh ) lên chúng và đồng thời không có thư mục dữ liệu riêng 

Trong INFORMATION_SCHEMA có nhiều bảng và view tuy nhiên có lẽ hay sử dụng nhiều nhất là các bảng TABLES , COLUMNS và USER_PRIVILEGES .

Bảng TABLES chứa tất cả các thông tin về các bảng của các cơ sở dữ liệu 

Bảng COLUMNS chứa tất cả các thông tin về các cột của các bảng trong tất cả các cơ sở dữ liệu 

Bảng USER-PRIVILEGES chứa tất cả cá thông tin về quyền truy cập của các người dùng đối với mỗi cơ sở dữ liệu . 

### 3.Demo Lab

Đầu tiên ta sẽ đi tìm những site có địa chỉ là product_detail id=

Nhận thấy http://192.168.1.7/cat.php?id=1 là một địa chỉ phù hợp

<img src="https://uphinhnhanh.com/images/2017/01/06/pen10490b.png" alt="pen10490b.png" border="0" />

Sau đó ta thêm dấu `'` ở phía sau đường link nếu site thay đổi nghĩa là site đó có lỗi

<img src="https://uphinhnhanh.com/images/2017/01/06/pen2933d8.png" alt="pen2933d8.png" border="0" />

Rồi ta sử dụng lệnh `ORDER BY` để tìm số cột của cái bảng trong site

Sau khi thử các trường hợp thì ta thấy site trên có 4 cột 

<img src="https://uphinhnhanh.com/images/2017/01/06/pen3ae5b9.png" alt="pen3ae5b9.png" border="0" />

Sau đó tìm xem trong cột nào chứa giá trị lỗi ta dùng lệnh UNION SELECT câu lệnh này để nổi kết quả của các câu truy vấn . Nếu có lỗi thì truy vấn sẽ lỗi

<a href="https://uphinhnhanh.com/image/Pr1"><img src="https://uphinhnhanh.com/images/2017/01/06/pen4d9a0f.png" alt="pen4d9a0f.png" border="0" /></a>

Vậy cột 2 sẽ chứa giá trị lỗi

Bây giờ ta sẽ truy vấn vào giá trị của cột 2

Ta thay đổi các từ khóa để truy vấn ứng với nội dung truy vấn vào số  2 

<img src="https://uphinhnhanh.com/images/2017/01/06/pen55624e.png" alt="pen55624e.png" border="0" />

Bây giờ ta tiến hành truy vấn vào database thông qua information_schema

Đầu tiên ta xem các bảng có trong database 

Ta tìm được tên các bảng trong data base đó 

<img src="https://uphinhnhanh.com/images/2017/01/06/pen69b677.png" alt="pen69b677.png" border="0" />

Nhận thấy có 1 bảng có tên là users . Nên đây có thể là bảng chứa các thông tin về người sử dụng

Ta truy vấn vào bảo đó để lấy ra các tên cột 

<a href="https://uphinhnhanh.com/image/PA8"><img src="https://uphinhnhanh.com/images/2017/01/06/pen782f88.png" alt="pen782f88.png" border="0" /></a>

Sau khi truy vấn ta nhận được dữ liệu 

<img src="https://uphinhnhanh.com/images/2017/01/06/pen8cebaf.png" alt="pen8cebaf.png" border="0" />

Ta thấy mật khẩu có dạng mã hóa MD5 sau khi giải mã ta có mật khẩu là  P4ssw0rd





