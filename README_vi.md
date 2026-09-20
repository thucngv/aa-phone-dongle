# AA Phone Dongle

[English](README.md)

Biến điện thoại Android dự phòng thành dongle Android Auto không dây cho màn hình ô tô hỗ trợ Android Auto có dây.

Ứng dụng đang trong giai đoạn thử nghiệm; khả năng tương thích và tự kết nối lại phụ thuộc vào điện thoại và headunit.

## Ứng dụng hoạt động như thế nào?

```text
Điện thoại Android chính       Điện thoại Android dự phòng       Headunit ô tô
Android Auto            <-->   AA Phone Dongle            <-->   Android Auto có dây
                      Bluetooth + Wi-Fi                    USB
```

Điện thoại dự phòng được cắm vào cổng USB dữ liệu của ô tô. Điện thoại chính kết nối không dây với máy dự phòng và chạy Android Auto, bao gồm bản đồ, nhạc và các ứng dụng được hỗ trợ.

Bluetooth thiết lập kết nối không dây và trao đổi thông tin hotspot. Wi-Fi truyền dữ liệu Android Auto; máy dongle chuyển tiếp dữ liệu qua USB tới headunit.

Chỉ cài AA Phone Dongle trên **điện thoại dự phòng**. Ứng dụng không bổ sung Android Auto cho headunit vốn không hỗ trợ và không hỗ trợ Apple CarPlay.

## Tính năng

- Dùng điện thoại Android dự phòng làm cầu nối Android Auto không dây.
- Ghép đôi Bluetooth và tự động trao đổi thông tin kết nối Wi-Fi.
- Hiển thị tên điện thoại đang kết nối khi lấy được thông tin và trạng thái truyền dữ liệu gần nhất.
- Hiển thị SSID hotspot hiện tại, không hiện mật khẩu hoặc mã QR.
- Tùy chọn tự khởi động khi cắm USB.
- Nút **Dừng dongle** để kết thúc phiên.
- Giao diện tiếng Anh và tiếng Việt, hiển thị phiên bản ứng dụng cạnh tiêu đề chính.

## Cần chuẩn bị

| Thành phần | Yêu cầu |
| --- | --- |
| Máy dongle | Android 11 trở lên, có Bluetooth, hỗ trợ hotspot Wi-Fi nội bộ và USB accessory |
| Điện thoại chính | Hỗ trợ Android Auto không dây, đã hoàn thành thiết lập Android Auto |
| Headunit ô tô | Android Auto có dây hoạt động và có cổng USB dữ liệu tương ứng |
| Cáp USB | Cáp hỗ trợ truyền dữ liệu |

Android 11 là phiên bản tối thiểu để cài ứng dụng, không phải cam kết tương thích. Việc thử nghiệm hiện có bao gồm máy dongle Xiaomi sapphire và điện thoại chính Pixel 8a; chưa được kiểm chứng rộng trên nhiều bộ thiết bị.

## Thiết lập lần đầu

### 1. Chuẩn bị hai điện thoại

1. Cài APK AA Phone Dongle lên **điện thoại dự phòng**.
2. Trên **điện thoại chính**, hoàn thành thiết lập Android Auto và bật Android Auto không dây nếu máy có tùy chọn này.
3. Bật Bluetooth và Wi-Fi trên cả hai máy.
4. Giữ dữ liệu di động trên điện thoại chính để dùng bản đồ và nhạc trực tuyến. Dongle tạo hotspot nội bộ, không cung cấp kết nối internet.

**Nên tắt/vô hiệu hóa Android Auto (Gearhead) trên máy làm dongle nếu hệ thống cho phép**, để tránh xung đột. Vào Cài đặt Android → Ứng dụng → Android Auto → **Tắt/Vô hiệu hóa**. Tên mục và khả năng tắt tùy thiết bị. Chỉ đóng màn hình ứng dụng không đồng nghĩa với vô hiệu hóa.

**Giữ Android Auto hoạt động trên điện thoại chính.** Đây là máy chạy phiên Android Auto.

### 2. Cấp quyền

1. Mở AA Phone Dongle và **Hướng dẫn thiết lập**.
2. Nhấn **Cấp quyền**, sau đó cho phép các quyền được yêu cầu. Tùy phiên bản Android, ứng dụng cần quyền thiết bị ở gần, Bluetooth, Wi-Fi/vị trí và thông báo.
3. Cho phép ứng dụng chạy nền nếu cài đặt pin trên điện thoại đang hạn chế.

### 3. Kết nối Bluetooth giữa hai điện thoại trước — bắt buộc

**Phải ghép đôi và kết nối Bluetooth giữa điện thoại chính với máy dongle trước khi tiếp tục. Chỉ bật Bluetooth là chưa đủ; ghép đôi điện thoại với ô tô cũng không thay thế bước này.**

1. Bật Bluetooth trên cả hai điện thoại. Trên máy dongle, nhấn **Ghép đôi Bluetooth** ở màn hình chính của ứng dụng và chấp nhận yêu cầu cho phép hiển thị.
2. Trên **điện thoại chính**, mở cài đặt Bluetooth của Android, tìm thiết bị và chọn **tên Bluetooth của máy dongle**.
3. Xác nhận mã ghép đôi trên cả hai máy. Nếu đã ghép đôi từ trước, chọn máy dongle trong danh sách thiết bị Bluetooth đã lưu trên điện thoại chính để kết nối lại.
4. Hoàn tất kết nối Bluetooth giữa hai điện thoại rồi mới chuyển sang bước kết nối với ô tô bên dưới.
5. Quay lại hướng dẫn thiết lập, chọn có bật **Tự động chạy khi cắm USB** hay không, rồi nhấn **Hoàn tất và bật dongle**.

### 4. Kết nối với ô tô

1. Dùng cáp dữ liệu nối máy dongle vào **cổng USB Android Auto có dây** của headunit.
2. Nếu Android hỏi ứng dụng cần mở hoặc quyền truy cập USB accessory, chọn AA Phone Dongle và cho phép truy cập.
3. Nếu dongle đang dừng, nhấn **Bật dongle**.
4. Chấp nhận các yêu cầu thiết lập Android Auto trên điện thoại chính hoặc headunit nếu có.
5. Chờ Android Auto xuất hiện trên headunit. Ứng dụng hiển thị **Đang kết nối đến [tên điện thoại]** khi có tên thiết bị và **Đang truyền dữ liệu** khi có dữ liệu đi qua.

Thông thường không cần tự chọn mạng hotspot: thông tin kết nối được trao đổi qua Bluetooth. Android quyết định SSID, mật khẩu và băng tần; SSID có thể thay đổi giữa các phiên.

## Sử dụng hằng ngày

- Khi bật tự khởi động theo USB, cắm máy dongle vào ô tô và giữ Bluetooth/Wi-Fi trên điện thoại chính hoạt động. Các quyền và khả năng chạy nền vẫn phải được duy trì.
- Nhấn **Dừng dongle** để kết thúc phiên, sau đó **Bật dongle** để chạy lại.
- Nếu headunit không kết nối lại hoặc ứng dụng yêu cầu kết nối lại USB, hãy rút rồi cắm lại cáp. Ứng dụng không thể ép đặt lại USB ở mức phần cứng.
- **Đang truyền dữ liệu** phản ánh dữ liệu vừa được chuyển tiếp; riêng trạng thái này chưa xác nhận headunit đang hiển thị phiên chiếu bình thường.

## Hạn chế hiện tại

- **Kết nối lại USB có thể chập chờn**, nhất là sau Dừng/Bật, rút/cắm cáp hoặc khi bắt tay ban đầu kéo dài. Một số headunit có thể khởi động lại USB trong lúc hai điện thoại vẫn đang kết nối.
- **Khả năng phục hồi USB còn hạn chế:** ứng dụng có thể thử mở lại phiên giao thức, nhưng không thể buộc headunit nhận một kết nối USB vật lý mới. Có thể cần rút/cắm cáp thủ công.
- **Hotspot do Android quản lý.** Không đảm bảo SSID cố định hoặc một băng tần Wi-Fi cụ thể. Một số ROM hạn chế đọc thông tin mạng hotspot, có thể khiến kết nối thất bại.
- **Ngắt kết nối đột ngột có thể khiến âm thanh bị kẹt hoặc phát tiếng è trên một số headunit.** Xử lý shutdown đã cải thiện các trường hợp quan sát được, nhưng chưa được xác nhận trên mọi headunit hoặc tình huống force stop Android Auto.
- Chỉ hỗ trợ một phiên chiếu đang hoạt động; chưa hỗ trợ chuyển đổi liền mạch giữa nhiều điện thoại.
- Hạn chế chạy nền, nguồn điện, nhiệt độ và điều kiện sóng có thể ảnh hưởng độ ổn định. Phiên sử dụng dài và khả năng tương thích rộng vẫn cần được kiểm thử.

## Xử lý sự cố

| Hiện tượng | Cách thử |
| --- | --- |
| Headunit không nhận dongle | Kiểm tra Android Auto có dây hoạt động trên đúng cổng USB, thử cáp dữ liệu khác và cấp quyền USB accessory. |
| Bluetooth đã ghép đôi nhưng không lên hình | Kiểm tra Android Auto trên điện thoại chính, giữ Bluetooth/Wi-Fi bật và cấp đủ quyền cho dongle. Nếu vẫn lỗi, vào cài đặt Bluetooth trên cả hai điện thoại, chọn Quên thiết bị/Hủy ghép đôi với máy còn lại, sau đó ghép đôi và kết nối lại hai máy trước khi thử lại. |
| Hai điện thoại đã kết nối nhưng headunit vẫn không lên hình | Dừng dongle, rút/cắm lại USB rồi bật lại. Báo lỗi nếu tình trạng lặp lại. |
| Headunit liên tục kết nối lại lúc khởi động | Ghi lại trình tự thao tác và trạng thái kết nối. Tương thích lúc khởi động/kết nối lại vẫn là hạn chế hiện tại. |
| Âm thanh bị kẹt hoặc có tiếng è sau khi ngắt kết nối | Nhấn **Dừng dongle**. Nếu headunit vẫn bị kẹt, rút USB trước khi bắt đầu phiên mới. |
| Không tự khởi động | Mở ứng dụng, kiểm tra tùy chọn tự chạy khi cắm USB, quyền và hạn chế chạy nền, sau đó kết nối lại USB. |

Khi báo lỗi, cung cấp model và phiên bản Android của cả hai điện thoại, model headunit, phiên bản/loại bản dựng ứng dụng và các bước gây lỗi. Ghi rõ có force stop Android Auto hoặc rút USB hay không. Xóa thông tin cá nhân và thông tin đăng nhập Wi-Fi khỏi log trước khi chia sẻ.

---

Made by @thucngv in Hanoi
