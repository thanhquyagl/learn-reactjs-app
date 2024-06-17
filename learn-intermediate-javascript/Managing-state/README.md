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
