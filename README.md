Giúp bạn thay đổi vị trí lưu Zalo.

Giảm béo cho ổ C khi Zalo lưu quá nhiều videos, hình ảnh,...

Thao tác đơn giản với click chuột.

![image](https://github.com/NDWoodCompany/ZaloMove/assets/102244520/c870c8e3-3a82-403b-9eca-f9d661185d27)

Hướng dẫn làm thủ công:

Ở hướng dẫn này tôi move qua D:

Bước 1:

Tạo các thư mục sau:

D:\Zalo\

Zalo

ZaloPC: Lưu

ZaloData: Ứng dụng zalo để chạy

ZaloReceivedFiles: download file từ Zalo


Bước 2: Chuyển dữ liệu bằng cmd

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



Bước 3: Tạo liên kết thư mục

mklink /d "%LocalAppData%\ZaloPC" "D:\Zalo\ZaloPC"

mklink /d "%appdata%\ZaloData" "D:\Zalo\ZaloData"

mklink /d "%LocalAppData%\Programs\Zalo" "D:\Zalo\Zalo"

mklink /d "%USERPROFILE%\Documents\Zalo Received Files" "D:\Zalo\ZaloReceivedFiles"



Sau khi hoàn thành các bước trên thì mở Zalo từ "D:\Zalo\Zalo\Zalo.exe" Thay các đường dẫn shortcut nếu muốn đảm bảo không lỗi.
