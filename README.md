## ***Tìm hiểu & Lập trình Linux kernel module***

Đồ án 3 môn Hệ điều hành

> Viết một module dùng để tạo ra số ngẫu nhiên (RNG - Random Number Generator).

> Module này sẽ tạo một character device để cho phép các tiến trình ở user space có thể open và read các số ngẫu nhiên.

## Thông tin sinh viên

 

+ Phạm Tống Bình Minh - 18120210

+ Nguyễn Văn Phước - 18120226

## Thông tin bài làm


Bao gồm: thư mục *Source* chứa mã nguồn và thư mục *Document* chứa báo cáo đồ án.



## Hướng dẫn sử dụng

Đi tới thư mục chứa mã nguồn:

	cd RNG_LKM

Build kernel module theo phương pháp Kbuild bằng lệnh:

	make

Cài đặt module vào kernel.

	sudo insmod randomModule.ko

Gọi hàm ở user space để đọc dữ liệu số ngẫu nhiên được tạo từ character device ở kernel space.

	sudo ./userTest

Tháo module ra khỏi kernel.

	sudo rmmod randomModule

Dọn dẹp file build dư thừa trong folder.

	make clean