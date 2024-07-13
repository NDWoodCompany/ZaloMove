Giúp bạn thay đổi vị trí lưu Zalo.

Giảm béo cho ổ C khi Zalo lưu quá nhiều videos, hình ảnh,...

Thao tác đơn giản với click chuột.

![image](https://github.com/NDWoodCompany/ZaloMove/assets/102244520/db3446be-93d5-405a-9ac8-478347707755)


**Hướng dẫn sử dụng tool:**

Bước 1: Mở tool với quyền administrator

Bước 2: Click [![image](https://github.com/NDWoodCompany/ZaloMove/assets/102244520/6f791042-acde-4ac2-90a8-b81cc5c532f2)] Chọn nơi muốn lưu Zalo. (Mặc định mình chọn là ổ D).

Bước 3: Chọn thư mục muốn di chuyển. (Mặc định là di chuyển cả 4 thư mục)

Bước 4: Chọn nơi muốn tạo lối tắt.

Bước 5: Chọn chế độ:

5.1: [Di chuyển] là sẽ cut thư mục qua vị trí mới luôn

5.1: [Sao chép] là sẽ copy thư mục qua vị trí mới và đổi tên thư mục ở vị trí gốc để dự phòng lỗi.

Bước 6: Click [BẮT ĐẦU DI CHUYỂN]. Chờ đợi cho đến khi hoàn thành việc di chuyển.

_**Lưu ý: Trong quá trình tool làm việc không nên mở Zalo để tránh lỗi.**_




**Hướng dẫn làm thủ công:**

Ở hướng dẫn này tôi move qua D:

_Bước 1. Tạo các thư mục sau:_

D:\Zalo\

Zalo

ZaloPC: Lưu

ZaloData: Ứng dụng zalo để chạy

ZaloReceivedFiles: download file từ Zalo


mkdir D:\Zalo\Zalo

mkdir D:\Zalo\ZaloPC

mkdir D:\Zalo\ZaloData

mkdir D:\Zalo\ZaloReceivedFiles




_Bước 2. Chuyển dữ liệu_ (cần quyền administrator mới chuyển được). Làm thủ công hoặc dùng cmd như sau:

Mở cmd với quyền administrator. Copy/paste các lệnh:

xcopy "%LocalAppData%\ZaloPC" "D:\Zalo\ZaloPC" /h /i /c /k /e /r /y

xcopy "%appdata%\ZaloData" "D:\Zalo\ZaloData" /h /i /c /k /e /r /y

xcopy "%LocalAppData%\Programs\Zalo" "D:\Zalo\Zalo" /h /i /c /k /e /r /y

xcopy "%USERPROFILE%\Documents\Zalo Received Files" "D:\Zalo\ZaloReceivedFiles" /h /i /c /k /e /r /y

Ren "%LocalAppData%\ZaloPC" "ZaloPC-Old"

Ren "%appdata%\ZaloData" "ZaloData-Old"

Ren "%LocalAppData%\Programs\Zalo" "Zalo-Old"

Ren "%USERPROFILE%\Documents\Zalo Received Files" "Zalo Received Files-Old"


Or

move /-y "%LocalAppData%\ZaloPC" "D:\Zalo"

move /-y "%appdata%\ZaloData" "D:\Zalo"

move /-y "%LocalAppData%\Programs\Zalo" "D:\Zalo"

move /-y "%USERPROFILE%\Documents\Zalo Received Files" "D:\Zalo"




_Bước 3: Tạo liên kết thư mục_

mklink /d "%LocalAppData%\ZaloPC" "D:\Zalo\ZaloPC"

mklink /d "%appdata%\ZaloData" "D:\Zalo\ZaloData"

mklink /d "%LocalAppData%\Programs\Zalo" "D:\Zalo\Zalo"

mklink /d "%USERPROFILE%\Documents\Zalo Received Files" "D:\Zalo\ZaloReceivedFiles"



Lưu ý: Trước khi liên kết thư mục phải kiểm tra các thư mục sau đã có hay chưa? Chưa có thì sao chép hoặc di chuyển qua.

"D:\Zalo\ZaloPC"

"D:\Zalo\ZaloData"

"D:\Zalo\Zalo"

"D:\Zalo\ZaloReceivedFiles"

Và các thư mục sau đã xóa hay đổi tên hay chưa? Nếu chưa thì xóa hoặc đổi tên đi.

"%LocalAppData%\ZaloPC"

"%appdata%\ZaloData"

"%LocalAppData%\Programs\Zalo"

"%USERPROFILE%\Documents\Zalo Received Files"



Sau khi hoàn thành các bước trên thì mở Zalo từ "D:\Zalo\Zalo\Zalo.exe" Thay các đường dẫn shortcut nếu muốn đảm bảo không lỗi.
