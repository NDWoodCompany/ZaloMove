Giúp bạn thay đổi vị trí lưu Zalo.

Giảm béo cho ổ C khi Zalo lưu quá nhiều videos, hình ảnh,...

Thao tác đơn giản với click chuột.

![image](https://github.com/user-attachments/assets/779bc749-e79e-43df-ab97-27f5a181cf52)




**Hướng dẫn sử dụng tool:**

Bước 1: Mở tool với quyền administrator

Bước 2: Click [![image](https://github.com/NDWoodCompany/ZaloMove/assets/102244520/6f791042-acde-4ac2-90a8-b81cc5c532f2)] Chọn nơi muốn lưu Zalo. (Mặc định mình chọn là ổ D).

Bước 3: Chọn thư mục muốn di chuyển. (Mặc định là di chuyển cả 5 thư mục)

Bước 4: Chọn chế độ: (Bước này mình đã ẩn nên các bạn bỏ qua)

4.1: [Sao chép] là sẽ copy thư mục qua vị trí mới và đổi tên thư mục ở vị trí gốc để dự phòng lỗi. (**Mặc định**)

4.2: [Di chuyển] là sẽ copy thư mục qua vị trí mới và xoá thư mục gốc đi.

Ưu tiên sao chép khi di chuyển Zalo. Sau khi sao chép và sử dụng Zalo ổn định thì bạn tiến hành xoá thư mục *-Old

Bước 5: Click [TỰ ĐỘNG]. Chờ đợi cho đến khi hoàn thành việc di chuyển.

Sau khi di chuyển xong sẽ có chữ X màu đỏ xuất hiện. Đây là thư mục gốc mình đổi tên dự phòng. Các bạn mở Zalo lên dùng nếu thấy ổn thì có nhấn để xoá đi.

Còn nếu Zalo bị lỗi. Các bạn bỏ tích ở bảng chọn bên phải để xoá liên kết. Sau đó mở thư mục bằng nút ở bảng bên trái. Đổi tên lại như cũ (xoá chữ "-Old" đi) và tiến hàng di chuyển lại.

**Chế độ thủ công thì các bạn cứ chọn từng cái các bạn muốn di chuyển, sao chép sau đó click chọn ở bảng bên trái để tạo liên kết. Bảng bên trái hiện lên tích thì đã liên kết thành công.**


_**Lưu ý 1: Trong quá trình tool làm việc không nên mở Zalo để tránh lỗi.**_

**Lưu ý 2: Nếu các bạn cài lại win thì dùng tool này tạo lại liên kết để dùng tiếp Zalo không bị mất dữ liệu**
Cách thực hiện sau khi cài lại win.
Sau Bước 1, Bước 2 ở trên thì các lựa chọn sẽ sáng lên nếu có thư mục dữ liệu. Các bạn tích chọn để tạo liên kết và sử dụng.



**Hướng dẫn làm thủ công:**

Ở hướng dẫn này tôi move qua D:

_Bước 1. Tạo các thư mục sau:_

D:\Zalo\

Zalo

ZaloPC: Lưu

ZaloData: Ứng dụng zalo để chạy

ZaloReceivedFiles: download file từ Zalo


Lệnh cmd:

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
