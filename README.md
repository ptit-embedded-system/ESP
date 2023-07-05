# ESP
## How to run

Tham khảo video hướng dẫn nối mạch (Quan trọng): [Hướng dẫn sử dụng ESP32-CAM](https://www.youtube.com/watch?v=MjFM2rmp1zY)

Trong vid sử dụng code mẫu, nhưng để sử dụng cho đồ án thì chỉ cần lấy code đã upload lên là được.
- B1: kết nối mạch với máy tính
- B2: Tải arduino bản 1.x (******Tuyệt đối không tải bản 2.x******).
- B3: vào arduino → file → references. Và paste đoạn sau vào Additional Boards Manager URLs:
https://dl.espressif.com/dl/package_esp32_index.json
Ấn OK, và chờ, nếu IDE có đang tải về máy thư viện hoặc load thư viện thì chờ cho nó load xong.
- B4: Vào tools → boards → board managers. Tìm esp32, và install. Kiểm tra trong tools → boards có ESP32 Arduino không, nếu có thì thành công.
- B5: Vào tools → boards → ESP32 Arduino → Ai Thinker ESP32-CAM
- B6: Vào tools → CPU Frequency → Chọn 240MHz (Chỉ áp dụng với Wifi 2.4G, Wifi 5G sẽ không bắt được). Lúc chạy thì phải đảm bảo rằng kết nối đến Wifi 2.4G.

> Từ bước B2 đến B6 là bước setup, sau khi đã setup thành công thì các lần sau vào chỉ cần bỏ qua các bước B2 đến B6.
> 
- B7: Mở code. Chỉnh sửa các thông số như:
    - ssid và password là tên wifi và mật khẩu wifi 2.4G đang sử dụng.
    - serverName là địa chỉ ip của server cần để upload hình ảnh.
    - serverPort là công của server.
    - timerInterval là khoảng cách giữa các lần gửi hình ảnh.
- B8: Vào tools → port, chọn đúng port mà mình kết nối mạch
- B9: Chọn port Nạp code (lúc nạp, nhớ đảm bảo rằng GPIO0 và GND được kết nối với nhau)
- B10: Sau khi nạp thành công thì ấn nút reset (chỉ cần nhấn, không giữ)
- B11 Mở serial monitor (nhấp vào ký hiệu kính lúp ở góc trên bên phải của Arudino IDE). Một màn hình pop-up sẽ hiện ra.
- B12: Kiểm tra xem Serial Monitor có đang là 115200baud không, nếu không thì chỉnh lại 115200 baud (kiểm tra ở góc dưới bên phải của màn hình pop-up serial monitor, nút thứ 2 từ bên phải sang).
- B13: Nhấn nút Reset. Rút kết nối GPIO0 và GND ra. Sau đó ấn reset lại lần nữa. (Các lần sau nếu muốn chạy lại thì kết nối GPIO0 và GND lại).
