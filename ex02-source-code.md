## PHẦN 2: SOURCE CODE (NỘI DUNG FILE .md)

### Hướng Dẫn Cài Đặt Cảm Biến Độ Ẩm Cho Trang Trại Lan


### 1. Mã nguồn điều khiển máy bơm (Python)
Dưới đây là đoạn mã Python mẫu dùng để đọc độ ẩm và điều khiển máy bơm:

```python
 import time
 def control_pump(humidity):
    threshold = 60.0
    if humidity < threshold:
        print("Độ ẩm thấp! Đang bật máy bơm tưới nước...")
    else:
        print("Độ ẩm ổn định. Máy bơm ở trạng thái tắt.")

if __name__ == "__main__":
    current_humidity = 55.5
    control_pump(current_humidity)  

**3. So sánh Cảm biến Cũ và Mới**
| Tiêu chí | Cảm biến Cũ (Analog) | Cảm biến Mới (Digital) |
| :--- | :--- | :--- |
| Độ chính xác | Thấp, dễ bị nhiễu tín hiệu | Cao, truyền dữ liệu số ổn định |
| Độ bền | Dễ bị oxy hóa ngoài trời | Chống ẩm tốt, tuổi thọ cao |
| Cách đọc dữ liệu | Đọc qua cổng ADC | Đọc qua giao tiếp chuẩn |

4. Tiến độ kiểm tra thiết bị (Task List)

- [x] Kết nối dây nguồn và chân tín hiệu GPIO
- [x] Kiểm tra phiên bản thư viện Python hỗ trợ cảm biến
- [ ] Chạy thử nghiệm script điều khiển máy bơm tự động
- [ ] Kiểm tra các ký tự đặc biệt như dấu sao \* hoặc dấu thăng \# trong tài liệu hướng dẫn

## GIẢI ĐÁP BẪY DỮ LIỆU
Cách sử dụng ký tự Escape (\) trong Markdown:
Khi muốn hiển thị các ký tự đặc biệt có chức năng cú pháp trong Markdown (như dấu sao *, dấu thăng #, hoặc gạch dưới _) như là một ký tự văn bản thông thường mà không bị trình biên dịch hiểu nhầm là lệnh định dạng (in đậm, tiêu đề...), ta đặt dấu gạch chéo ngược \ ngay trước ký tự đó (Ví dụ: viết \* hoặc \# để hiện ra ký tự thô).
