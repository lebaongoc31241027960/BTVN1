# AI Usage Log

## 1. Công cụ AI

- **Tên công cụ:** ChatGPT
- **Nhà phát triển:** OpenAI
- **Mục đích:** Hỗ trợ phân tích giao diện, đề xuất cải tiến HTML/CSS, giải thích mã nguồn và hỗ trợ kiểm tra logic tương tác trong trang thanh toán thương mại điện tử.

## 2. Mục đích sử dụng

ChatGPT được sử dụng trong quá trình phát triển giao diện thanh toán mô phỏng của Watsons Việt Nam nhằm:

- Phân tích những điểm có thể cải thiện trong giao diện thanh toán.
- Đề xuất cách thu gọn khu vực chọn mã giảm giá để giảm chiều dài trang.
- Hỗ trợ bổ sung nút tăng và giảm số lượng sản phẩm.
- Giải thích vai trò của các thành phần HTML, CSS và JavaScript được bổ sung hoặc điều chỉnh.
- Hỗ trợ xây dựng logic tính toán lại thành tiền, tạm tính, phí vận chuyển, giảm giá và tổng thanh toán.
- Hỗ trợ viết tài liệu mô tả các cải tiến và ghi lại quá trình sử dụng AI.

## 3. Prompt đã sử dụng

Các prompt chính được sử dụng trong quá trình thực hiện:

**Prompt 1: Phân tích và cải tiến giao diện**

"Trang thanh toán của tôi đang quá dài. Hãy đề xuất cách thu gọn khu vực chọn voucher thành một hàng có thể nhấn để mở rộng danh sách, đồng thời bổ sung nút tăng/giảm số lượng sản phẩm."

**Prompt 2: Chỉnh sửa mã nguồn HTML**

"Làm lại thành một đoạn HTML hoàn chỉnh. Đánh dấu những phần đã chỉnh sửa so với bản gốc."

**Prompt 3: Giải thích mã nguồn**

"Giải thích được vai trò của các thành phần HTML/CSS đã sửa."

## 4. Kết quả AI đề xuất

ChatGPT đã hỗ trợ các nội dung sau:

- Đề xuất giao diện voucher có thể mở rộng và thu gọn bằng nút bấm.
- Đề xuất sử dụng thuộc tính `hidden` để ẩn danh sách voucher khi trang được tải.
- Bổ sung cấu trúc HTML cho bộ điều chỉnh số lượng sản phẩm với hai nút `+` và `−`.
- Đề xuất các thuộc tính `data-product` và `data-unit-price` để nhận diện sản phẩm và lấy đơn giá phục vụ tính toán.
- Hỗ trợ xây dựng JavaScript để cập nhật số lượng, thành tiền từng sản phẩm và tổng giá trị đơn hàng.
- Giải thích vai trò của các bộ chọn CSS như `.voucher-toggle`, `.quantity-control`, `.quantity-btn` và `.quantity-value`.
- Hỗ trợ soạn thảo tài liệu mô tả chức năng, công nghệ, cách chạy dự án và các cải tiến đã thực hiện.

Các đề xuất của AI là cơ sở tham khảo cho quá trình phát triển. Kết quả cuối cùng phụ thuộc vào việc tích hợp mã nguồn và kiểm tra thực tế trên trình duyệt.

## 5. Kiểm tra và điều chỉnh

Sau khi nhận đề xuất từ AI, người thực hiện cần kiểm tra các nội dung sau:

- Đối chiếu HTML đã sửa với cấu trúc trang thanh toán ban đầu để bảo đảm không làm mất các khu vực chức năng.
- Kiểm tra nút mở/đóng voucher và xác nhận danh sách được ẩn khi tải trang.
- Kiểm tra việc áp dụng và hủy voucher, bao gồm thông báo trạng thái và số tiền giảm giá.
- Kiểm tra nút `+` và `−` của từng sản phẩm, bảo đảm số lượng và thành tiền được cập nhật phù hợp.
- Đối chiếu tạm tính và tổng thanh toán với công thức tính giá.
- Kiểm tra cách bố trí giao diện trên máy tính và điện thoại.
- Kiểm tra đường dẫn đến file CSS và các lỗi JavaScript trong trình duyệt.

## 6. Phần tôi hiểu và có thể giải thích

### 6.1. HTML

- `button`: Tạo nút thao tác để mở voucher hoặc tăng/giảm số lượng.
- `id`: Định danh duy nhất cho phần tử HTML để JavaScript có thể truy cập.
- `class`: Nhóm các phần tử có cùng mục đích định dạng bằng CSS.
- `hidden`: Ẩn phần tử HTML cho đến khi thuộc tính này được gỡ bỏ.
- `data-unit-price`: Lưu đơn giá sản phẩm dưới dạng thuộc tính dữ liệu tùy chỉnh.
- `data-action`: Xác định thao tác mà nút thực hiện, chẳng hạn tăng hoặc giảm số lượng.

### 6.2. CSS

- `.voucher-toggle`: Định dạng nút mở/đóng danh sách voucher.
- `.quantity-control`: Bố trí các nút và số lượng sản phẩm trên cùng một hàng.
- `.quantity-btn`: Định dạng nút tăng và giảm số lượng.
- `.quantity-value`: Định dạng phần hiển thị số lượng hiện tại.
- `@media`: Điều chỉnh giao diện theo kích thước màn hình để hỗ trợ thiết bị di động.

### 6.3. JavaScript

JavaScript xử lý các thao tác tương tác và cập nhật dữ liệu hiển thị:

- Bắt sự kiện nhấn nút voucher để mở hoặc thu gọn danh sách.
- Bắt sự kiện nhấn nút `+` hoặc `−` để thay đổi số lượng sản phẩm.
- Tính thành tiền dựa trên đơn giá và số lượng.
- Cập nhật tạm tính, phí vận chuyển, giảm giá và tổng thanh toán theo logic của phiên bản mô phỏng.

Công thức tính thành tiền:

**Thành tiền = Đơn giá × Số lượng**

Công thức tổng quát:

**Tổng thanh toán = Tạm tính + Phí vận chuyển − Giảm giá**

### 6.4. Những giới hạn tôi nhận thức được

- Giao diện hiện tại là phiên bản mô phỏng phục vụ học tập, chưa kết nối cơ sở dữ liệu hoặc hệ thống thanh toán thực tế.
- Dữ liệu sản phẩm, mã giảm giá và quy tắc vận chuyển được thiết lập trong mã nguồn.
- HTML và CSS không tự xử lý việc tính toán; những chức năng tương tác và cập nhật giá trị cần JavaScript.
- Mã nguồn do AI đề xuất cần được kiểm tra, điều chỉnh và chạy thử trước khi sử dụng.

Qua quá trình thực hiện, em hiểu được cách phối hợp HTML, CSS và JavaScript để cải tiến giao diện thương mại điện tử, đồng thời nhận thức được trách nhiệm kiểm tra và giải thích mã nguồn do AI hỗ trợ tạo ra.
