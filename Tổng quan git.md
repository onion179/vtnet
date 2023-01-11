<h1 style="color: yellow">Lịch sử ra đời</h1>
Tháng 4 năm 2005, Linus Torvalds đã sử dụng BitKeeper để kiểm soát phiên bản phát triển Linux Kernel. Anh ấy có một số lượng lớn các nhà phát triển tình nguyện làm việc trên Linux Kernel. BitKeeper là một công cụ tuyệt vời để quản lý sự đóng góp to lớn của các nhà phát triển. Các nhà phát triển Linux đã sử dụng công cụ này miễn phí sau khi có thỏa thuận giữa hai bên vì BitKeeper là một hệ thống quản lý kiểm soát nguồn độc quyền, nghĩa là bạn phải trả tiền cho việc sử dụng công cụ này. Nó Đã xảy ra xung đột lợi ích sau khi Andrew Tridgell tạo một ứng dụng người dùng nguồn mở để truy cập hệ thống kiểm soát phiên bản Bitkeeper bằng kỹ thuật đảo ngược các giao thức BitKeeper. Điều này khiến người giữ bản quyền rút lại chính sách sử dụng miễn phí mà họ đã đồng ý trước đó. Nhiều nhà phát triểnLý do tồn tại nhân Linux đã từ bỏ quyền truy cập vào BitKeeper.

Linux biết rằng anh ấy phải hành động nhanh chóng để thay thế hệ thống kiểm soát phiên bản mà anh ấy biết và yêu thích, vì vậy anh ấy đã có một kỳ nghỉ làm việc để quyết định xem phải làm gì vì hệ thống kiểm soát phiên bản miễn phí sử dụng hiện tại không thể giải quyết vấn đề của anh ấy vào thời điểm đó. Kết quả của kỳ nghỉ của anh ấy là sự ra đời của một hệ thống kiểm soát phiên bản mới có tên Git.

<h1 style="color: yellow">Lý do tồn tại</h1>

* Git dễ sử dụng, an toàn và nhanh chóng.
* Có thể giúp quy trình làm việc code theo nhóm đơn giản hơn rất nhiều bằng việc kết hợp các phân nhánh (branch).
* Có thể làm việc ở bất cứ đâu vì chỉ cần clone mã nguồn từ kho chứa hoặc clone một phiên bản thay đổi nào đó từ kho chứa, hoặc một nhánh nào đó từ kho chứa.
* Dễ dàng trong việc deployment sản phẩm.


<h1 style="color: yellow">Sự phát triển hiện tại</h1>

Ngày nay, git và GitHub đang chiếm lĩnh thế giới vì nhiều nhà phát triển đang áp dụng git và GitHub để kiểm soát phiên bản. Có khoảng 56 triệu nhà phát triển theo thống kê.

<h1 style="color: yellow">Ứng dụng thực tế</h1>

Giả sử có 1 project tạm gọi là project Gốc. Và sau 1 thời gian muốn clone project bằng cách fork, mirror project này ra thành nhiều dự án khác nhau (tạm gọi là project Clone). Mỗi dự án được clone ra sẽ có 1 vài điều chỉnh, chỉnh sửa, thêm hoặc xoá bớt tính năng các thứ. Rồi 1 vài trường hợp sau có thể xuất hiện:

1. Project Gốc tiếp tục được phát triển thêm tính năng mới, fix bug code cũ, refactor các thứ, bla bla bla... Và những thay đổi này, sẽ áp dụng cho tất cả những project được clone ra từ Project Gốc này đều có được những thay đổi ấy.
   
2. Project Clone được phát triển và có những thay đổi, cải tiến, fix bug.
