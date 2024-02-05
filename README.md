# Bài tập tết - Kiến trúc phần mềm

>
> Họ tên: **Trần Phúc Khang**
>
> Mã sinh viên: **21020341**

### Mục lục
***[I. Lý thuyết](#I)***

[1. Docker, docker-composer là gì? ](#Question1)

[2. Linux vs Unix vs BSD hay *nix? macOS thuộc loại nào?](#Question2)

[3. Alpine vs Ubuntu?](#Question3)

[4. VNC](#Question4)

***[II. Thực hành](#II)***

<a name = "I"></a>
## I. Lý thuyết

<a name="Question1"></a>
### 1. Docker, docker-composer là gì?
- Docker là nền tảng phần mềm cho phép bạn dựng, kiểm thử và triển khai ứng dụng một cách nhanh chóng. Docker còn là một nền tảng ảo hóa mã nguồn mở giúp đóng gói phần mềm vào các đơn vị tiêu chuẩn hóa được gọi là **'container'** . Mỗi **container** chứa mọi thứ cần thiết để chạy một ứng dụng, bao gồm *mã nguồn, thư viện, môi trường thực thi và công cụ hệ thống*
- Docker giúp đơn giản hóa quá trình triển khai và quản lý ứng dụng, giúp đảm bảo ứng dụng sẽ hoạt động giống nhau trên mọi môi trường chạy Docker.

<a name="Question3"></a>
### 3. Alpine VS Ubuntu ?
- Alpine Linux và Ubuntu là hai hệ điều hành dựa trên Linux, nhưng chúng có những đặc điểm khác nhau.
#### Kích thước của hệ điều hành:
- **Alpine:**
  * Alpine được thiết kế nhẹ và nhỏ gọn
  * Kích thước của image Alpine thường rất nhỏ, điều này làm cho nó trở thành một lựa chọn phổ biến cho việc triển khai container.
- **Ubuntu:**
  * Ubuntu có kích thước lớn hơn so với Alpine do nó cung cấp nhiều gói và thư viện mặc định hơn
    
#### Package Manager:
- **Alpine:**
  * Alpine sử dụng 'apk' làm package manager.
  * 'apk' có thể cài đặt các gói một cách nhanh chóng và hỗ trợ quản lí dependencies hiệu quả.
- **Ubuntu:**
  * Ubuntu sử dụng 'apt' làm package manager.
  * 'apt' có nhiều tính năng và hỗ trợ nhiều gói mở rộng.
    
#### Thư viện và Dependencies
- **Alpine:**
  * Alpine thường sử dụng thư viện musl thay vì glibc, giúp giảm kích thước và tiêu tốn ít tài nguyên hệ thống hơn.
- **Ubuntu:**
  * Ubuntu thường sử dụng glibc và có sẵn nhiều dependencies hơn so với Alpine.
    
#### Image Base và Container
- **Alpine:**
  * Alpine thích hợp cho việc xây dựng các container nhỏ gọn và nhẹ.
  * Thường được sử dụng trong môi trường containerized, đặc biệt là Docker.
- **Ubuntu:**
  * Ubuntu thích hợp cho các ứng dụng cần sự đa dạng và tính đầy đủ của một hệ điều hành.
  * Thường được sử dụng trong các ứng dụng không yêu cầu sự nhẹ nhàng tuyệt đối.
#### Bảo mật 
- **Alpine:**
  * Alpine thường được biết đến với việc chú trọng đến bảo mật và giảm thiểu các thành phần không cần thiết.
- **Ubuntu:**
  * Ubuntu cũng chú trọng đến bảo mật, nhưng do cung cấp nhiều gói và tính năng, có thể tăng nguy cơ bị tấn công về bảo mật.
  
<a name="Question4"></a>
### 4. VNC
#### Định nghĩa
* VNC, viết tắt của "Virtual Network Computing", là một hệ thống được sử dụng để chia sẻ màn hình giữa các thiết bị khác nhau với mục đích điều khiển từ xa.
* VNC hoạt động dựa trên mô hình client/server. Máy tính cần được cài đặt thành một máy chủ VNC, trong khi máy tính khác muốn điều khiển từ xa cần cài đặt một trình xem VNC, hoặc còn gọi là client. Khi hai thành phần này được kết nối, máy chủ VNC sẽ chuyển gửi hình ảnh màn hình từ xa đến trình xem VNC.

#### Cách VNC hoạt động:
* **Client-Server Model**: VNC hoạt động theo mô hình client-server. Máy chủ chia sẻ màn hình và chờ đợi các kết nối từ các máy khách. Máy khách kết nối đến máy chủ để xem và điều khiển màn hình.
* **VNC Server và VNC Viewer**: Máy chủ sử dụng phần mềm VNC Server để chia sẻ màn hình. Máy khách sử dụng phần mềm VNC Viewer để kết nối và điều khiển máy chủ.

#### Bảo mật trong VNC:
* **Mã hóa dữ liệu**: Giao thức VNC không mặc định không mã hóa dữ liệu. Có các phiên bản VNC sử dụng mã hóa để bảo vệ thông tin gửi đi và đảm bảo an toàn.
* **Kết nối an toàn**: Nhiều người sử dụng kết hợp VNC với các phương thức bảo mật như kết nối thông qua SSH hoặc sử dụng VNC qua HTTPS.
  
#### Tính năng và lợi ích nổi bật của VNC
* **Giao thức đơn giản**: VNC sử dụng giao thức RFB (remote framebuffer) đơn giản và mạnh mẽ. Giao thức này truyền tải hình ảnh và các đầu vào từ các thiết bị ngoại vi giữa máy chủ (máy tính được truy cập từ xa) và máy khách (thiết bị sử dụng để kết nối đến máy tính từ xa). Vì VNC không sử dụng nhiều tài nguyên như CPU và bộ nhớ, nên nó có thể chạy trên phần cứng có công suất thấp.
* **Hoạt động độc lập**: Giao thức RFB không cần biết rõ về hệ điều hành mà nó đang chạy mà chỉ cần gửi dữ liệu chuột và bàn phím từ máy người dùng đến máy từ xa và gửi dữ liệu hình ảnh từ máy từ xa đến máy người dùng.
* **Chia sẻ màn hình giữa người dùng**: Bạn có thể thiết lập cấu hình VNC để cho phép người dùng địa phương vẫn duy trì đăng nhập khi người dùng từ xa kết nối đến máy tính của họ. Như vậy, việc điều khiển máy tính có thể được chia sẻ giữa cả hai người dùng. Ngoài ra, VNC cũng có thể được sử dụng như một công cụ hỗ trợ khách hàng, cho phép khách hàng nhìn thấy chính xác những gì kỹ thuật viên từ xa đang làm trên máy tính của họ.
* **Chia sẻ các phần khác nhau của màn hình với nhiều người dùng**: Có thể sử dụng VNC để thiết lập nhiều cổng và chia sẻ các phần khác nhau của màn hình cho từng cổng cụ thể.
* **Sử dụng trên nhiều nền tảng**
* **Bảo mật và quản lý dễ dàng**: VNC cung cấp các tính năng bảo mật và quản lý cho người dùng. Bạn có thể thiết lập mật khẩu và các cơ chế xác thực để bảo vệ kết nối VNC. Ngoài ra, VNC cũng hỗ trợ ghi lại hoạt động, cho phép người dùng kiểm tra lại những gì đã xảy ra trong phiên làm việc từ xa.
