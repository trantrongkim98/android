# Activity

## Giới thiệu


- Android System không bắt đầu với 1 hàm main, mà được khởi tạo cùng với 1 Activity vì Android System không có điểm bắt đầu và điểm kết thúc, mà nó có thể bắt đầu ở bất cứ Activity nào trong System và mỗi Application trong Android sẽ có 1 Activity chính được cấu hình trong AndroidManifest.xml và sẽ được mở lên khi mở ứng dụng

- Activity có thể tồn tại full screen hoặc 1 phần nhỏ của device hoặc neo trên top của trên eg: khi xem video trong YouTube của Chrome và xuống background thì sẽ có 1 Activity động trên màn hình điện thoại để tiếp tục xem video đang xem
Eg: 
- khi bạn mở ứng dụng Android System sẽ tim Activity có action là LUNCHED trong Android Application để mở
- Khi bản share 1 đoạn text ở 1 ứng dụng bất kỳ Android System sẽ tìm những Activity có action là SEND và tuỳ theo tuỳ chọn của bạn mà mở activity đó lên 
Note:  mỗi Activity là 1 window, nên khi  mở recent của operation system bạn sẽ thấy các Activity đã được mở trước đó, nếu bạn gửi implicit từ Android system nó sẽ mở 1 Activity mới và cũng có thể phủ lên activity hiện tại của bạn **cần làm rõ hơn**

Intent
Intent có 2 loại là: explicit và implicit

- Intent explicit là intent được gửi tới đích đến rõ ràng (eg: Facebook bắn 1 intent đến Messenger)
- Intent implicit là intent được gửi tới Activity có action là action được gởi đi (eg: share Text của system và system tìm tất cả Activity có action là SEND) 

Để bắt đầu ở 1 Activity bất kỳ chúng ta cấu hình `<intent-filter>` trong AndroidManifest.xml

- Tag action cho biết action được gửi tới

- Tag category cho biết danh mục của Activity

- Tag data cho biết loại data mà app được gửi tới eg: mineType:”text/plain”

- **Để lấy dữ liệu từ intent khi Activity được chọn để mở, thì chúng ta sẽ dùng intent.clipData**
