# Các lệnh cơ bản của vim
## Làm việc với file

| Lệnh | Mô tả |  
| :----- | :---------- | 
|:e|filename Mở file.|
|:w|filename Lưu file.|
|:q|Thoát khỏi Vim. Lệnh sẽ vô hiệu nếu file chưa được lưu|
|:q!|Thoát khỏi Vim kể cả file chưa được lưu|
|:wq|Lưu và thoát|
|:x|Lưu và thoát. Tương tự :wq|

## Chế độ ghi chèn và đè 

| Lệnh | Mô tả |  
| :----- | :---------- | 
|C|	Xóa từ vị trí con trỏ đến cuối dòng hiện tại để chèn.|
|r|Thay thế / ghi đè 1 kí tự.|
|R|Thay thế / ghi đè nhiều kí tự. Ấn ESC để kết thúc.|

## Xóa văn bản

| Lệnh | Mô tả |  
| :----- | :---------- | 
|x|Xóa kí tự hiện tại ở vị trí con trỏ.|
|X|Xóa kí tự phái trước con trỏ.|
|dd or d:|Xóa dòng hiện tại.|

## Chế độ visual 

| Lệnh | Mô tả |  
| :----- | :---------- | 
|v|Bắt đầu bôi đen kí tự. Sử dùng các lệnh di chuyển để chọn văn bản 1 cách thích hợp.|
|V|Bắt đầu bôi đen dòng|
|The ESC key|Thoát khỏi chế độ Visual trở về chế độ lệnh|

## Chỉnh sửa văn bản

- Chú ý: Đánh dấu (V) là làm việc trong chế độ Visual, khi bạn đánh dấu văn bản. Các lệnh khác làm việc ở chế độ lệnh, khi không có đoạn văn bản nào được chọn.

| Lệnh | Mô tả |  
| :----- | :---------- | 
|~|Chuyển đổi từ kí tự thường sang hoa hoặc ngược lại. Làm việc ở cả chế độ Visual và chế độ lệnh.|
|>(V)|Thụt lề sang phải.|
|<(V)|Thụt lề sang trái.|
|c (V)|Xóa đoạn văn bản được đánh dấu để chèn.|
|y (V)|Sao chép đoạn văn bản được đánh dấu vào bộ nhớ đệm.|
|d (V)|	Cắt đoạn văn bản trong bộ nhớ đệm vào vị trí con trỏ.|
|yy or :y or Y|	Sao chép 1 dòng.|
|dd or :d|Xóa 1 dòng.|
|p|Dán đoạn văn bản trong bộ nhớ đệm vào sau vị trí con trỏ. Nếu cả dòng thì dán vào vị trí dòng bên dưới.|
|P|Dán đoạn văn bản trong bộ nhớ đệm vào trước vị trí con trỏ. Nếu cả dòng thì dán vào vị trí dòng bên trên.|

## Undo & redo

| Lệnh | Mô tả |  
| :----- | :---------- | 
|u|Undo.|
|U|Undo tất cả các thao tác thực hiện với dòng hiện tại.|
|Ctrl + r|Redo.|

## Tìm kiếm 

| Lệnh | Mô tả |  
| :----- | :---------- | 
|/|chuỗi Tìm kiếm chuỗi|
|n|Sử dụng sau lệnh /, tìm chuỗi phù hợp tiếp theo (tìm về cuối)|
|N|Sử dụng sau lệnh /, tìm chuỗi phù hợp phía trước (tìm về đầu)|

## Thay thế

| Lệnh | Mô tả |  
| :----- | :---------- | 
|:rs/foo/bar/g|Substitute foo with bar. r determines the range and g determines the arguments.|

Thay thế foo bởi bar,
:s có nghĩa là tìm kiếm và thay thế
r và g có thể thay đổi.

- r có thể là:

| Lệnh | Mô tả |  
| :----- | :---------- | 
|Không gì cả|Làm việc với dòng hiện tại.|
|number|Làm việc trên dòng number được chỉ định|
|%|Toàn bộ văn bản|

- g có thể là:

| Lệnh | Mô tả |  
| :----- | :---------- | 
|g|Thay thế toàn bộ, nếu không có tham số này. Vim chỉ thay thế mẫu đầu tiên tìm được trên mỗi dòng.|
|i|Không phân biệt chữ hoa chữ thường|
|l|Phân biệt cả hoa – thường (mặc định)|
|c|Có lựa chọn trước khi thay thế. Khi lựa chọn xuâts hiện, ấn y để đồng ý, n để bỏ qua, a để đồng ý toàn bộ,q để thoát|

# Thiết lập môi trường trong vim

| viết tắt | Mô tả |  
| :----- | :---------- | 
|ai|autoindent sẽ thụt lề mỗi dòng cho cùng với dòng phía trên. Mặc đình off.|
|ap|autoprint in dòng hiện hành lên màn hình khi dòng thay đổi. Mặc định là on.|
|eb|errorbells làm cho máy kêu bíp mỗi khi gõ sai lệnh. Mặc định off.|
|nu|number hiển thị số hiệu của dòng. Mặc định off|
|redraw|redraw cập nhật màn hình mỗi khi có thay đổi. Mặc định on|
|report|report lập ra kích cỡ của một thay đổi trong tiến trình hiệu chỉnh, và đưa kết quả ra dòng trạng thái. Ví dụ, report=3 sẽ bắn lời nhắn mỗi khí bạn ra lệnh xóa nhiều hơn 3 dòng, song sẽ im lặng nếu bạn xóa ít hơn 3 dòng. Mặc định report=5|
|sm|showmatch hiển thị một dấu mở ngoặc nếu bạn gõ vào một dấu đóng ngoặc. Rất tiện cho lập trình viên. Mặc định là off.|
|smd|showmode hiển thị các thông báo chế độ như: Insert, Visual, … mặc định là on|
|warn|warn hiển thị thông báo khi bạn thoát khỏi Vim khi vùng đệm bị thay đổi mà chưa được lưu. Mặc định là on.|
|wm=n|wrapmargin xác định lề phải. Mặc định wm=0|
|sw|shiftwidth số khoảng trắng khi tab lùi (Ctrl+D)trong lúc dùng autoindent và sử dụng cho lệnh << và >>. Mặc định sw=8|
|ts|tabstop định số khoảng trắng khi tab. Mặc định ts=8|

Để sử dụng các tùy chọn trên, sử dụng lệnh **:set “tên tùy chọn[=tham số]“**

VD: 
> **:set ai eb sw=4 ts=4**

Nếu muốn xem các thiết lập của Vim, bạn chỉ đánh lệnh :set mà không sử dụng đối số.
Muốn xem danh sách các tùy chọn và cách thiết lập, bạn gõ :set all
Muốn tắt một tùy chọn, bạn thêm “no” vào trước tên tùy chọn đó vào trong lệnh :set.

VD:
> **:set nonumber nowarn**

Để sử dụng các tùy chọn này là mặc định cho các lần sử dụng tiếp theo, chỉnh sửa file: ~/.vimrc
Trong gVim, có thể chỉnh sửa bằng cách chọn: Edit/Startup Settings

Để thay đổi thiết lập màu nền cũng như màu chữ theo các mẫu có sẵn của Vim, bạn dùng lệnh:

> **colorscheme <tên mẫu>**

# Tabs trong vim

Tabs ở đây là các thẻ tab dùng cho soạn thảo nhiều tài liệu khác nhau đồng thời một cách đơn giản hơn thay vì mở nhiều chương trình Vim.

Để mở nhiều file một lúc trên các tab khác nhau, có thể dùng câu lệnh sau vim với tham số -p trong terminal:

> **vim -p file1 file2 file3**

Đang trong quá trình soạn thảo, muốn tạo mới một tab để soạn thảo văn bản khác có thể dùng lệnh:

> **:tabnew [tên file] hoặc :tabe [tên file]**

Mặc định số tab có thể mở nhiều nhất là 10, nhưng cũng có thể thay đổi thành n tab bằng câu lệnh:

> **:set tabpagemax=n**

Để xem thông tin về các tab đang được mở, sử dụng lệnh:

> **tabs**

Để di chuyển giữa các tab có thể dùng lệnh **:tabn*** (tab next) di chuyển đến tab phía sau hoặc **:tabp** (tab previous) di chuyển về tab phía trước. Có thể di chuyển giữa các tab bằng lệnh **gt**. Để chuyển về tab đầu tiên dùng lệnh:

> **:tabfirst hoặc :tabfir**

Lệnh di chuyển đến tab cuối cùng là: **:tablast**. Để hiển thị tab bar hay không có thể dùng lệnh:

> **:set showtabline=n**

trong đó n có giá trị là 2 hoặc 0 tương đương với hiển thị hoặc không hiển thị. Để di chuyển tab hiện tại đến vị trí khác trong tab bar, có thể dùng lệnh:

> **:tabm vị trí**

Chú ý là vị trí tab bắt đầu từ 0. Để thoát khỏi tất cả các tab dùng lệnh: **:qa** hoặc **:qa!** hoặc **:wqa** hoặc **:wa** tùy vào mục đích muốn thoát.

# Marco trong vim

Để lặp lại lệnh đã thực hiện trước đó trong Vim có thể dùng lệnh . nhưng lệnh . chỉ lặp lại các thao tác trong 1 lần nhấn phím **ESC**.

Marco là một tính năng mạnh mẽ hơn lệnh . giúp lặp lại nhiều thay đổi hơn. Để bắt đầu sử dụng Marco nhấn q, tiếp tục nhấn một phím kí tự bất kì từ a đến z đại diện cho tên marco, sau đó thực hiện các thao tác muốn lặp lại, sau đó lại nhấn q để kết thúc marco đó.

Để áp dụng marco thì nhấn @ rồi nhấn tên marco.