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
## Thực hành
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
