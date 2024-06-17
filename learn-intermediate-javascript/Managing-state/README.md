## Managing State - Quản lý trạng thái.
Dư thừa hoặc trùng lặp state là nguyên nhân phổ biến gây ra lỗi.
phải có cấu trúc state tốt để giữ cho logic cập nhật trạng thái có thể duy trì được và chia sẽ trạng thái cho các compnent ở xa.


### Reacting to input with state - Phản ứng với đầu vào state
Ta không thể thay đổi giao diện người dung. mà chỉ có thể mô tả giao diện người dùng muốn xem cho các State hình ảnh khác nhau của compnent, sau đó kích hoạt các thay đổi trạng thái để phản hồi dữ liệu đầu vào cho người dùng.

### Choosing the state structure - Lựa chọn cấu trúc State
trạng thái cấu trúc tốt tạo ra sự khác biết giữ thành phần dễ sửa đổi và gỡ lỗi và thành phần thường xuyên có lỗi. 
Nguyên tắc quan trọng nhất là state không được chứa thông tin dư thừa hoặc trùng lặp, nếu có state không cần thiết rất dễ quên cập nhật và gây ra lỗi!


### Sharing state between components - chia sẽ state giữ các component
Tạo 1 thành phần cha mẹ giữ state và chỉ định các props cho các thành phần con của nó.


### Preserving and resetting state - Bảo toàn và đặt lại State
React cần quyết định phần nào của cây sẽ giữ lại (và cập nhật) và phần nào cần loại bỏ hoặc lại từ đầu. Theo mặc định React giữ nguyên các phần của cây "khớp" với thành phần  được hiển thị trước đó. Đôi khi sải ra ngoài mong muốn, chúng ta có thể ghi đè hành vi mặc định và buộc 1 thành phần đặt lại State của nó bằng cách chuyển cho no 1 khoá khác. ( như key={item.email}). làm thế cho React biết nếu khác người nhận nó cần làm mới giao diện người dùng như ban đầu.

### Extracting state logic into a reducer - Trích xuất logic State vào Reducer 
Các Component có nhiều cập nhật State trải rộng trên nhiều trình xữ lý sự kiện có thể trở nên quá tải. Đối với nhưng trường hợp này có thể hợp nhất tất cả logic cập nhật State bên ngoài thành phần của mình trong 1 hàm duy nhất, được gọi là "Reducer". Trình xữ lý sẽ ngắn gọn hơn vì chúng chỉ xác định "Hành động" của người dùng. Ở Cuối tệp, Hàm Reducer chỉ định cách State sẽ cập nhật dể phản hồi từng hành động!

### Passing data deeply with context - Tuyền dữ liệu sâu với hàm Context
Thông thường ta dùng props để tuyền thông tin từ component cha sang component con. sẽ trở nên bất tiện nếu ta cần chuyển 1 số props qua nhiều Component hoặc nếu nhiều Component cần cùng 1 thông tin. 
hàm Context cho phép thành phần cha cung cấp một số thông tin cho bất kỳ component nào trong cây bên dưới nó - bất kể nó xâu đến mức nào - mà không chuyển nó 1 cách rõ ràng qua các Props.

### Scaling up with reducer and context - Mở rộng quy mô với hàm Reducer và Hàm Context.

Hàm Reducer cho phép hợp nhất logic cập nhật State của 1 Component. Hàm Context cho phép tuyền xâu xuống các component khác. Ta có thể kết hợp các hàm Reducer và Context với nhau để quản lý State của 1 màn hình phức tạp.

Với cách tiếp cận này, Component gốc có State phức tạp sẽ quản lý no bằng hàm Reducer. Các thành phần khác ở bất kì đâu ở trong cây đều có thể đọc trạng thái của nó thông qua Context. Và có thể gửi hành động để cập nhật State đó.
