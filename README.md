# Câu hỏi phong vấn về ReactJs

## JavaScript

1 . This là gì?

'this' trong javascript là 1 phương thức đặc biệt tham chiếu đến đối tương mà một phương thức được gọi trên đó.

2 . Có những loại biến nào, sự khác nhau của chúng?

- Có 3 loại biến trong JS, 'var', 'let' và 'const'. 
- 'Var' và 'let' có thể thay đổi, 'const' thì không?
- 'var' có thể khai báo lại và update, 'let' thì có thể update nhưng không thể khai báo lại.
- 'var' có phạm vi function-scoped, 'let' và 'const' có phạm vi block-scoped.


## ReactJs

1 . ReactJs là gì? Tại sao lại dùng ReactJS?
 ReactJs là 1 thư viện JavaScript được dùng để xây dựng giao diện người dùng tương tác.

2 . trình bày life cycle của Reactjs?
LifeCycle của một component React bao gồm: mounting, updating, unmounting.

3 . useEffect có thể dùng trong các giai đoạn nào của life cycle?
useEffect có thể sử dụng trong tất cả các giai đoạn của lifecycle: componentDidMount, componentDidUpdate, và componentWillUnMount.

4 . Virtual DOM 
viết tắt Document Object MOdel.
Virtual DOm là một bản sao của DOM được React tạo ra và duy trì trong bộ nhớ để tối ưu hoá hiệu suât khi cập nhật giao diện.

Giao diện người dùng là 1 component, khi component thay đổi, React sẽ cập nhất DOM ảo, sau đó sau sánh DOM ảo hiện tại và DOM ảo trc đó "gọi là diffing". Khi React biết DOM ảo thay đổi, thì cập nhật mỗi thay đổi cho DOM thật để tối ưu hiệu suất.

5 . Thành phần Components?
Chia giao diện người dùng thành các phần độc lập, có thể tái sử dụng và có thể được xữ lý riêng.

6. JSX
 jsx là javascript + XML, giúp có thể code các cấu trúc HTML trong cùng 1 tệp chứa code JavaScript.

7 . Key là gì?

Key là 1 phần tử đăc biệt trong React yêu cầu để xác định các phần tử trong danh sách và giúp REact nhận biết các phẩn tử đã thay đổi, được thêm hoặc bị xoá qua đó quyết định thành phần nào cần re-render.

Được dùng khi sử dụng hàm MAP để render danh sách.

8 . tối ưu performance
để tối ưu performance cần tránh re-render nhiều lần, bằng cách:
  - khi sử dụng eventListenner cần phải có clean up.
  - Sử dụng useMemo và useCallback để hạn chế khởi tạo những tác vụ phức tạp.
  - Sử dụng useMeno để tránh useCallback không cần thiết. 
  - sử dụng key khi render danh sách.
  - sử dụng useRef để lưu value trong value trong trường hợp không cần re-render.

9 . có thể gán trực tiếp state mà không thông qua hàm setState được không?
 Có thể gán trực tiếp state bằng giá trị mới, nhưng component chỉ re-render khi thay đổi state thông qua hàm setState
 có thể nhưng không khuyến khích vì nó có thể gây ra các vấn đề liên quan đến hiệu xuât và tính chất nhất quán.


10 . Phân biết state và props.

state là dữ liệu mà component React có thể theo dõi và cập nhật, trong khi props là dữ liệu được truyền từ component cha sang component comn

state: quản lý các trạng thái của component, 

props: được dùng để chia sẽ các trạng thái component này cho các components khác.

11 . cách thức hoạch động useEffect?

useEffect là 1 hook trong React được dùng để thực thi các side effect trong functioal component.

'
  hook là 1 tính năng của React (16.8) cho phép bạn có thể sử dụng state và các chức năng khác của React mà không cần khởi tạo Class, có thể sử dụng state trong functional component.

  useState cho phép sử dụng state trong functional component.
  useEffect cho phép sử lý logic trong lifecycle methods, hàm được gọi mỗi khi có gì đó ảnh hương đến component.
'

12 . custom hook là gì?
là việc có thể tạo 1 hooks mới với chưc năng riêng biệt, tách phần code logic ra khỏi UI, giúp code tường minh, tránh lặp lại code và tái sử dụng.


https://viblo.asia/p/bo-cau-hoi-phong-van-reactjs-tu-co-ban-den-nang-cao-EoW4oxpAJml