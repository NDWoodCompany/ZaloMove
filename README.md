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


_Nếu có lỗi phát sinh:_

Như trắng màn hình Zalo,...

Bạn đảm bảo các thư mục ZaloData, ZaloPC, Reveiced Files đã sao chép đủ và có liên kết.

Hãy thử mở Zalo với quyền Administrator để nó cập nhật. Ok thì thôi còn không thì bạn Cài đặt lại Zalo (Cài đè luôn không gỡ Zalo cũ).

Sau khi cài xong Nếu thích thì di chuyển thư mục Zalo ("%LocalAppData%\Programs\Zalo") và tạo lại liên kết. Sau đó mới tiến hàng đăng nhập zalo để sử dụng.



**Hướng dẫn làm thủ công:**

Ở hướng dẫn này tôi di chuyển qua ổ D: 5 thư mục (Các bạn di chuyển 3 cái ở giữa thôi cũng được. 3 cái đó nặng nhất)
Zalo
ZaloPC
ZaloData
Zalo Received Files
zalo-updater

Bước 1: Tạo thư mục Zalo trong D
Bạn có thể dùng lệnh cmd dưới để tạo
Mở Command Prompt copy/paste vào

mkdir "D:\Zalo"

mkdir "D:\Zalo\Zalo Received Files"

Bước 2. Di chuyển dữ liệu sang ổ D

Chuyển Zalo Received Files qua D thì vào Cài đặt > Tin nhắn > File được lưu tại thư mục: > Thay đổi nó qua ổ D cũng được. Nếu dùng tính năng của Zalo thì các bước sau các bạn bỏ qua thư mục này.

Tắt hoàn toàn zalo đi. Chuột phải vào biểu tượng zalo dưới taskbar (hoặc vào task manager kiểm tra và tắt cho chắc)


Di chuyển toàn bộ 3 thư mục còn lại qua ổ D. Bạn làm thủ công hoặc dùng lệnh dưới:

Mở Command Prompt copy/paste vào

xcopy "%LocalAppData%\Programs\Zalo" "D:\Zalo\Zalo" /h /i /c /k /e /r /y

xcopy "%LocalAppData%\ZaloPC" "D:\Zalo\ZaloPC" /h /i /c /k /e /r /y

xcopy "%appdata%\ZaloData" "D:\Zalo\ZaloData" /h /i /c /k /e /r /y

xcopy "%USERPROFILE%\Documents\Zalo Received Files" "D:\Zalo\Zalo Received Files" /h /i /c /k /e /r /y

xcopy "%appdata%\zalo-updater" "D:\Zalo\zalo-updater" /h /i /c /k /e /r /y


Ren "%LocalAppData%\Programs\Zalo" "Zalo-Old"

Ren "%LocalAppData%\ZaloPC" "ZaloPC-Old"

Ren "%appdata%\ZaloData" "ZaloData-Old"

Ren "USERPROFILE%\Documents\Zalo Received Files" "Zalo Received Files-Old"

Ren "%appdata%\zalo-updater" "zalo-updater-Old"


Dùng lệnh này thì còn thư mục cũ đề phòng lỗi thì khôi phục lại

Hoặc

move /-y "%LocalAppData%\Programs\Zalo" "D:\Zalo"

move /-y "%LocalAppData%\ZaloPC" "D:\Zalo"

move /-y "%appdata%\ZaloData" "D:\Zalo"

move /-y "%USERPROFILE%\Documents\Zalo Received Files" "D:\Zalo"

move /-y "%appdata%\zalo-updater" "D:\Zalo"

Lệnh này thì move luôn nha.


Bước 3. Tạo liên kết thư mục

Mở Command Prompt copy/paste vào

mklink /d "%LocalAppData%\Programs\Zalo" "D:\Zalo\Zalo"

mklink /d "%LocalAppData%\ZaloPC" "D:\Zalo\ZaloPC"

mklink /d "%appdata%\ZaloData" "D:\Zalo\ZaloData"

mklink /d "%USERPROFILE%\Documents\Zalo Received Files" "D:\Zalo\Zalo Received Files"

mklink /d "%appdata%\zalo-updater" "D:\Zalo\zalo-updater"


Làm xong các bước trên thì vào mở Zalo trong "D:\Zalo\Zalo\Zalo.exe" lên dùng nha.


Mình hướng dẫn xong rồi. Chúc các bạn thành công và vui vẻ.
