# Temperature Application

## 🌟 Mô tả
Dự án này bao gồm hai thành phần chính:

1. **TemperatureServer**: Một dịch vụ web SOAP cung cấp các phương thức chuyển đổi nhiệt độ giữa Fahrenheit và Celsius.
2. **TemperatureClient**: Một ứng dụng Windows Forms cho phép người dùng nhập nhiệt độ và thực hiện chuyển đổi qua giao diện thân thiện.

## 🗂️ Cấu trúc dự án
```
TemperatureWS/
├── TemperatureServer/
│   ├── WebService1.asmx       # Dịch vụ web chính
│   ├── WebService1.asmx.cs    # Code-behind của WebService1
├── TemperatureClient/
│   ├── Form1.cs               # Form chính của ứng dụng WinForm
│   ├── Program.cs             # Điểm bắt đầu của ứng dụng
│   ├── App.config             # Tệp cấu hình ứng dụng
```

## ⚙️ Yêu cầu hệ thống
- .NET Framework >= 4.7
- Visual Studio 2019 hoặc mới hơn

## 🚀 Hướng dẫn cài đặt

### Bước 1: Clone repository
```bash
git clone https://github.com/soa-ueh-thanhlam/Excersie1.git
```

### Bước 2: Chạy TemperatureServer
- Cài đặt URL cho WebService trong `WebService1.asmx` nếu cần.
- Nhấn `F5` để chạy dịch vụ.

### Bước 3: Chạy TemperatureClient
- Trong Visual Studio, chọn dự án `TemperatureClient` làm dự án khởi chạy.
- Nhấn `F5` để chạy ứng dụng.

## 🌐 API Dịch vụ Web
Dịch vụ web cung cấp hai phương thức chính:

### 1. Chuyển đổi từ Fahrenheit sang Celsius
- **Phương thức:** `FahrenheitToCelsius`
- **Tham số:**
  - `fahrenheit` (double): Nhiệt độ đầu vào bằng Fahrenheit
- **Trả về:**
  - Nhiệt độ tương ứng bằng Celsius (double)

### 2. Chuyển đổi từ Celsius sang Fahrenheit
- **Phương thức:** `CelsiusToFahrenheit`
- **Tham số:**
  - `celsius` (double): Nhiệt độ đầu vào bằng Celsius
- **Trả về:**
  - Nhiệt độ tương ứng bằng Fahrenheit (double)

## 💡 Hướng dẫn sử dụng

### Thành phần

#### 1. TemperatureServer
- **WebService1.asmx:** Dịch vụ web chính cung cấp các phương thức chuyển đổi nhiệt độ.
- **Namespace:** `http://tempuri.org/`

#### 2. TemperatureClient
- **Giao diện WinForm:**
  - **Textbox:** Nhập nhiệt độ đầu vào
  - **Label:** Hiển thị kết quả chuyển đổi
  - **Button:** Thực hiện chuyển đổi giữa Fahrenheit và Celsius

### Các bước sử dụng
1. Chạy **TemperatureServer** để khởi động dịch vụ.
2. Mở ứng dụng **TemperatureClient** để nhập nhiệt độ và chọn chuyển đổi.
3. Xem kết quả trong giao diện.

## 🔧 Hướng dẫn kết nối Client với Server

1. Trong Visual Studio, nhấp chuột phải vào dự án `TemperatureClient`.
2. Chọn **Add > Service Reference**.
3. Trong cửa sổ **Add Service Reference**, chọn **Advanced**.
4. Chọn **Add Web Reference**.
5. Nhập URL của `WebService1.asmx` (ví dụ: `http://localhost:port/WebService1.asmx`).
6. Nhấn **Go** để tải thông tin dịch vụ.
7. Chọn dịch vụ và nhấn **Add Reference**.

## 📋 Kiểm thử
1. Sử dụng các bài kiểm thử có sẵn trong Visual Studio để kiểm tra từng phương thức API.
2. Đảm bảo kết quả trả về đúng với các trường hợp thử nghiệm (ví dụ: 32°F = 0°C).

## 🛠️ Xử lý lỗi
- Ứng dụng kiểm tra đầu vào bằng cách sử dụng `double.TryParse` để đảm bảo định dạng chính xác.
- Thông báo lỗi được hiển thị trong trường hợp nhập sai hoặc có sự cố kết nối với dịch vụ web.

## 📷 Giao diện minh họa
### Giao diện chính của ứng dụng
![image](https://github.com/user-attachments/assets/4624c319-4e03-45fe-91be-bb90e18f1846)

## 📜 License
Dự án này được phát hành dưới giấy phép [MIT License](LICENSE).

## 📧 Thông tin liên hệ
- **Tác giả:** [soa-ueh-thanhlam](https://github.com/soa-ueh-thanhlam)
- **Email:** lamdoan1122334455@example.com
