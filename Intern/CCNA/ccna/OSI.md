<h1 style="color: yellow">Mô hình OSI</h1>

- Kết nối giữa các máy tính khác nhau, giao tiếp với nhau.
- Mô hình liên kết hệ thống mở, có khả năng kết nối với các hệ thống khác. 
- Giao thức: Hướng liên kết, hướng không liên kết.

<h1 style="color: yellow">Máy truyền</h1> 

1. Tầng ứng dụng: Truyền dữ liệu, hình ảnh, video,...
2. Tầng trình diễn: Biến đổi dữ liệu thành dạng chung để mã hóa và nén dữ liệu.
3. Tầng phiên: Bổ sung thông tin cho phiên chuyển.
4. Tầng vận chuyển: Chia dữ lịu làm nhièu segment, thêm phương thức vận chuyển.
5. Tầng mạng: Cắt segment thành các packet để định tuyến.
6. Tầng liên kết: Chia packet thành nhiều frame và bổ sung thông tin kiểm tra gói dữ liệu cho máy nhận.
7. Tầng vật lý: Chuyển frame thành các bit hệ nhị phân: 0, 1 để truyền dữ liệu qua dây cáp quang.

<h1 style="color: yellow">Máy nhận</h1>

- Tầng 1: Nhận chuỗi bit và báo với tầng 2 đã nhận được dữ liệu.
- Tầng 2: Kiểm tra FCS xem lỗi không để hủy, kiểm tra MAC sau đó gửi lên lớp 3 (bóc header).
- Tầng 3: Kiểm tra IP.
- Tầng 4: Phục hồi lỗi, xử lý lỗi bằng cách gửi gói tin ACK, NAK, sắp xếp segment.
- Tầng 5: Kiểm tra tính toàn vẹn.
- Tầng 6: Chuyển đổi dạng dữ liệu phù hợp.
- Tầng 7: Bóc header, hiển thị.

