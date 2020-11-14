# flutter_lab0
Cài đặt môi trường phát triển

Trước khi bắt đầu với Flutter chúng ta cần cài đặt các thành phần cần thiết bao gồm :
1. [**Flutter SDK**](https://flutter.dev): Giải nén tệp tin tải về và đặt nó vào một thư mục (trong ví dụ này chúng ta chọn thư
mục **c:\src**), lúc này chúng ta sẽ có **c:\src\flutter**.
2. **Android SDK** (Được tích hợp khi cài Android Studio)
3. **Công cụ viết mã** (Có thể sử dụng sẵn **Android Studio + plugins flutter** hoặc sử dụng một IDE khác như **Visual Studio Code**)
## Yêu cầu hệ thống
Để cài đặt và thực thi Flutter, môi trường phát triển của chúng ta cần tối thiểu:
* Hệ điều hành: Windows 7 SP1 hoặc mới hơn (64-bit)
* Ổ đĩa còn trống: 1.32 GB (không kể không gian cho các IDE và Tools)
* Công cụ (tùy chọn): Các công cụ sau đây cần có nếu chúng ta muốn tải về và cài đặt bằng cách thực thi hoàn toàn bằng dòng lệnh, chúng có thể đã có sẵn trong môi trường hiện tại hoặc nếu chưa có sẵn thì chúng ta có thể cài bổ sung.
* Windows PowerShell 5.0 hoặc mới hơn (công cụ này này đã được cài sẵn với Windows 10).
* Git for Windows 2.x (công cụ này dùng để làm việc với các lệnh Git từ công cụ Windows Command Prompt ....)
### Thực hành
**Cập nhật đường dẫn**

  Việc cập nhật thêm đường dẫn của flutter vào biến môi trường PATH sẵn có của Windows
giúp chúng ta có thể thực thi các lệnh của flutter trên Windows console ở bất kỳ vị trí nào mà
không cần đi đến thư mục **c:\src\flutter\bin**. Để thêm đường dẫn vào biến môi trường của
Windows, từ thanh tìm kiếm ở góc trái dưới màn hình Windows, click chuột vào ô tìm kiếm
và nhập **env** và chọn **Edit environment variables**. Click chọn **Environment variables...** để
cập nhật biến môi trường cho tài khoản của người dùng.
  Nếu biến **Path** tồn tại ở cột Variable của phần User thì chúng ta bổ sung thêm đường dẫn tới
thư mục của Flutter SDK vào giá trị của biến Path bằng cách chọn Edit và thêm mới dòng
**c:\src\flutter\bin**. Lúc này biến Path của chúng ta đã có thêm đường dẫn của Flutter SDK,
điều này có nghĩa là chúng ta có thể thực thi các lệnh của Flutter ở bất kỳ vị trí nào trong công
cụ Windows Command Prompt mà không cần phải di chuyển đến vị trí **c:\src\flutter\bin**.
Nếu biến Path chưa tồn tại ở cột Variable của phần User thì chúng ta thêm mới biến Path và
nhập giá trị bằng cách thêm mới dòng **c:\src\flutter\bin**.

**Thực thi lệnh flutter doctor**

  Từ cửa sổ lệnh của công cụ Windows Command Prompt đã có đường dẫn tới Flutter SDK
(do đã thiết lập ở trên), chúng ta thực thi lệnh và xem kết quả để cài đặt thêm các phụ thuộc
cần thiết.

> Microsoft Windows [Version 10.0.18363.657]  
 (c) 2019 Microsoft Corporation. All rights reserved.  
 c:\Users\admin>**flutter doctor**  
 
 Câu lệnh trên kiểm tra môi trường hiện tại và hiển thị báo cáo tình trạng cài đặt môi trường
phát triển. Xem kết quả một cách cẩn thận để cài thêm những công cụ cần thiết còn thiếu.
Ví dụ một trường hợp như sau:

> Microsoft Windows [Version 10.0.18363.657]  
 (c) 2019 Microsoft Corporation. All rights reserved.  
 C:\Users>flutter doctor  
   Doctor summary (to see all details, run flutter doctor -v):  
 [v] Flutter (Channel stable, 1.20.2, on Microsoft Windows [  
  Version 10.0.18363.900], locale en-US)  
 [v] Android toolchain - develop for Android devices (
  Android SDK version 29.0.3)  
 [!] Android Studio (not installed)  
 [v] VS Code (version 1.48.1)  
 [!] Connected device  
   ! No devices available
 ! Doctor found issues in 2 categories.
 
 Ký hiệu [v] màu xanh là thành công, ký hiệu [!] màu cam là cảnh báo. Trong trường hợp
**Android toolchain - devlop for Android devices** chưa thành công thì cần phải cài đặt
Android Studio hoặc Android SDK, sau đó tiếp tục thực hiện lệnh flutter doctor cho
đến khi mục này thành công.  
  Đối với mục **Android Studio** có thể không cần vì chúng ta chỉ cần một trong số các môi
trường viết mã là **VS Code** hoặc **Android Studio.**
  Mục **Connected device** cho biết thiết bị di động đã kết nối bao gồm cả thiết bị vật lý (devices)
và thiết bị giả lập (emulators).  
  Để sẵn sàng lập trình với flutter trên Windows, chúng ta cần một thiết bị di động vật lý nền
tảng Android hoặc một thiết bị giả lập nền tảng Android.

#### THiết lập android

**Cài đặt Android Studio**
1. Tải và cài đặt Android Studio tại địa chỉ https://developer.android.com/
studio.

2. Khởi động Android Studio và đi đến **Android Studio Setup Wizard**. Việc này sẽ cài
đặt Android SDK mới nhất, các công cụ dòng lệnh của Android SDK và công cụ xây
dựng Android SDK được Flutter yêu cầu khi phát triển ứng dụng cho Android.
**Thiết lập thiết bị Android vật lý**
Để chuẩn bị chạy và kiểm tra ứng dụng Flutter trên thiết bị di động Android, chúng ta cần có
thiết bị Android phiên bản Android 4.1 (API cấp 16) trở lên.
1. Bật tùy chọn **Nhà phát triển** (Developer options) và **trình gỡ lỗi USB** (USB debugging)
trên thiết bị. Hướng dẫn chi tiết có sẵn trong tài liệu Android tại địa chỉ https:
//developer.android.com/studio/debug/dev-options.

2. Chỉ dành cho Windows: Cài đặt **Trình điều khiển USB** (Google USB Driver) của
Google tại địa chỉ https://developer.android.com/studio/run/win-usb.

3. Sử dụng cáp USB (nên sử dụng cáp nguyên bản), cắm điện thoại của bạn vào máy tính.
Nếu được nhắc trên thiết bị của bạn, hãy cho phép máy tính truy cập thiết bị của bạn.

4. Tại cửa sổ lệnh, hãy thực thi lệnh **flutter devices** để xác minh rằng Flutter nhận ra
thiết bị Android đã kết nối của bạn. Theo mặc định, Flutter sử dụng phiên bản Android
SDK nơi công cụ adb của bạn dựa trên. Nếu bạn muốn Flutter sử dụng cài đặt AndroidSDK khác, bạn phải đặt biến môi trường ANDROID_SDK_ROOT vào thư mục cài đặt
đó.
**Thiết lập trình giả lập Android**

  Để chuẩn bị chạy và kiểm tra ứng dụng Flutter trên trình giả lập Android, hãy làm theo các
bước sau:
1. Cho phép tăng tốc phần cứng cho trình giả lập **VM acceleration** trên máy tính của
bạn theo hướng dẫn tại địa chỉ https://developer.android.com/studio/
run/emulator-acceleration.

2. Khởi chạy Android Studio > Tools > Android> AVD Manager và chọn Tạo thiết bị
ảo (Create Virtual Device). (Menu con Android chỉ hiển thị khi bên trong một dự án
Android.).

3. Chọn định nghĩa thiết bị (device definition) và chọn Tiếp theo (Next).

4. Chọn một system image cho các phiên bản Android bạn muốn mô phỏng sau đó chọn
Tiếp theo (Next). Nên sử dụng image **x86** hoặc **x86_64**.

5. Trong phần Hiệu suất được mô phỏng (Emulated Performance), chọn Phần cứng -
GLES 2.0 (Hardware - GLES 2.0) để bật tăng tốc phần cứng.

6. Xác minh cấu hình AVD là đúng và chọn Hoàn tất (Finish). Để biết chi tiết về các bước
trên, hãy xem Quản lý AVD theo đường dẫn https://developer.android.
com/studio/run/managing-avds.

7. Trong Trình quản lý thiết bị ảo Android (Android AVD), nhấp vào Chạy trên thanh
công cụ. Trình giả lập khởi động và hiển thị canvas mặc định cho thiết bị và phiên bản
hệ điều hành đã chọn của bạn

Sinh viên hãy tiếp tục hành thực hành theo tài liệu ở đây  https://flutter.dev/docs/get-started/install/

Sau mỗi lần thực hiện thành công hãy commit và push lên github của cá nhân
