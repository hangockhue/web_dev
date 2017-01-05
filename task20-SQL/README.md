SQL viết tắt là Structured Query Language - là ngôn ngữ truy vấn mang tính cấu trúc được sử dụng để thực hiện các hoạt động trên các bản ghi, tạo va sửa đổi các cân bằng ...
- được thiết kế để quản lý dữ liệu trong một hệ thống quản lý cơ sở dữ liệu quan hệ RDBMS
- là ngôn ngữ cơ sở dữ liệu được sử dụng để tạo xóa cơ sở dữ liệu , lấy các hàng và sữa đổi các hàng

Chức năng của SQL
- Truy vấn Database theo nhiều cách khác nhau bởi sử dụng các lệnh
- Truy cập dữ liệu từ RDBMS
- Cho phép người dùng miêu tả dữ liệu
- Định nghĩa dữ liệu trong một Database và thao tác nó khi cần thiết 
- Cho phép người dùng tạo, xóa Database và bảng 
- Cho phép người dùng tạo view , procedure , hàm trong một Database 
- Cho phép người dùng thiết lập quyền truy cập vào bảng , thủ tục và view


Lệnh trong SQL chuẩn để tương tác với Relational Database là CREATE , SELECT , INSERT, UPDATE , DELETE và DROP . Các lệnh này có thể được phân loại thành các nhóm dựa trên bản chất của chúng

DDL ( Data Definition Language) - Ngôn ngữ định nghĩa dữ liệu 

CREATE : Tạo một bảng , một view của bảng hoặc đối tượng khác trong Database 

ALTER : Sữa đổi một đối tượng Database tồn tại ví dụ như một bảng

TRUNCATE : Xóa toàn bộ một bảng , môt view của bảng hoặc đối tượng khác trong một Database

DML ( Data Manipulation Language) - Ngôn ngữ thao tác dữ liệu

SELECT : Lấy các bảng ghi cụ thể từ một hoặc nhiều bảng 

INSERT : Tạo một bản ghi

UPDATE : Sửa đổi bản ghi

DELETE : Xóa các bản ghi

DCL ( Data Control Language) - Ngôn ngữ điều khiển dữ liệu

GRANT : Trao một quyền tới người dùng

REVOKE : Thu hồi quyền đã trao cho người dùng 

-----------------------------------

Cú pháp SQL cơ bản 

-Lấy cột từ một bảng trong Database
```
- SELECT ten_cot FROM ten_bang ;
```
- Tạo một bảng trong Database
````
- CREATE TABLE ten_bang (ten_cot kieu_du_lieu, ....)
```
- Thêm giá trị cho các cột trong bảng 
```
INSERT INTO ( cot1 , cot 2 ... cotn)
VALUES (giatri1 , giatri2 ,... giatrin);
```
- Chỉnh sửa giá trị của từng cột với SET là tên cột sửa còn WHERE là vị trí
```
UPDATE ten_bang
SET ten_cot = giatri 
WHERE dieu_kien;
```
- Thêm một cột mới vào bảng 
```
ALTER TABLE ten_bang ADD COLUMN ten_cot kieu_du_lieu;
```
- Xóa các dữ liệu trong bảng
```
DELETE FROM ten_bang WHERE ten_cot IS dieu_kien ;
```
- Loại bỏ những giá trị trùng lặp trong một cột của một bạng
```
SELECT DISTINCT ten_cot FROM ten_bang;
```
- Để lọc dữ liệu trong bảng ta có cú pháp 
```
SELECT ten_cot FROM ten_bang WHERE dieu_kien;
```
- Để tìm một dữ liệu nào đó trong một bảng ta có thể dùng câu lệnh
```
SELECT ten_cot FROM ten_bang

WHERE ten_cot LIKE dieu_kien;
```
Hoặc 
```
SELECT ten_cot FROM ten_bang

WHERE ten_cot BETWEEN diem_dau AND diemcuoi ;
```
Hoặc dùng OR khi lựa chọn cái này hoặc cái kia :
```
SELECT ten_cot FROM ten_bang

WHERE dieu_kien1 

OR dieu_kien2
```
- Để sắp xếp dữ liệu theo chiều thứ tự tăng dần hay giảm dần ta có câu lệnh 
```
SELECT ten_cot FROM ten_bang 
ORDER BY ten_cot ASC|DESC ;
```
Với DESC là giảm dần từ trên xuống còn ASC là tăng dần từ trên xuống

-Trong SQL có lệnh LITMIT để giới hạn dữ liệu xuất ra ta dùng lệnh nằm ngay sau câu lệnh xuất dữ liệu `LITMIT dieu_kien;`

-Để đếm có bao nhiêu dữ liệu trong cơ sỡ dữ liệu ta dùng lệnh `COUNT` 
```
SELECT COUNT (ten_cot) FROM ten_bang;
```
- Ta có thể kết hợp câu lệnh COUNT và WHERE để đếm dữ liệu với một điều kiện nào đó
```
SELECT COUNT (ten_cot) FROM ten_bang

WHERE dieu_kien
```
- Để sắp xếp dữ liệu đồng nhật vào trong các nhóm ta có lệnh GROUP BY  nó thường theo sau mệnh đề WHERE trong một lệnh SELECT
```
SELECT ten_cot FROM ten_bang

WHERE dieu_kien

GROUP BY ten_cot ;
```
- Để xuất tổng của một cột nào đó ta dùng lệnh SUM 
```
SELECT SUM(ten_cot) FROM ten_bang;
```
- Để xuất ra max của một cột nào đó với kiểu dữ liệu là int thì ta dùng lệnh MAX 
```
SELECT MAX(ten_cot) FROM ten_bang;
```
- Để tính trung bình cho mỗi hàng trong một cột có kiểu dữ liệu int thì ta dùng lệnh AVG ngoài ra để thu gọn kết quả thì ta dùng lệnh ROUND bao quanh AVG để làm tròn số ROUND(AVG(),so_lam_tron)
```
SELECT AVG(downloads) FROM fake_apps;
```
Truy vấn dữ liệu kết hợp giữa các bảng có liên kết với nhau ta có câu lệnh sau
```
SELECT ten_bang.ten_cot , ten_bang.ten_cot ... FROM ten_bang , ten_bang .... ;
```
Để kết nối dữ liệu từ nhiều bảng lại với nhau ta dùng lệnh JOIN
```
JOIN ten_bang1 ON ten_bang1.ten_cot = ten_bang1.ten_cot 
```
Với ten_bang1 là dữ liệu chính mà bạn cân liên kết

Nếu ta thêm trước JOIN lệnh LEFT thì nghĩa là nó sẽ trả về tất cả giá trị từ bảng chính cộng với giá trị được so sánh khớp từ bàng bên phải hoặc NULL trong trường hợp không có số khớp nào 

-Để thay thôi tên hiển thị khi xuất một bảng ta có lên AS ngay phía sau lệnh SELECT 
```
SELECT ten_bang.ten_cot AS "ten_goi" FROM ten_bang ;
```
 


