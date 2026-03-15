# Tìm Nghịch Đảo Trong Trường Hữu Hạn GF(2^10)
(Galois Field Inverse Finder)

Dự án này cài đặt thuật toán **Euclidean mở rộng (Extended Euclidean Algorithm)** bằng C++ để tìm nghịch đảo nhân của một phần tử trong trường hữu hạn GF(2^10). 

Chương trình thao tác trực tiếp trên các bit nhị phân để mô phỏng các phép toán cộng, trừ, nhân, chia đa thức trong môi trường GF(2).

## 🧮 Cơ sở toán học
- **Trường hữu hạn:** GF(2^10)
- **Đa thức tối giản:** `m(x) = x^10 + x^3 + 1` (Biểu diễn nhị phân: `10000001001` - Số nguyên: `1033`)
- **Phép toán:** - Cộng/Trừ trong GF(2) được thực hiện bằng phép `XOR` (^).
  - Nhân/Chia đa thức được thực hiện bằng các phép dịch bit (bit shift) và `XOR`.

## 🚀 Chức năng chính
1. **Tìm nghịch đảo nhân:** Tính đa thức nghịch đảo `a^-1` sao cho `(a * a^-1) mod m(x) = 1`.
2. **Theo dõi các bước (Step-by-step):** In ra chi tiết bảng giá trị trung gian của từng bước trong thuật toán Euclid mở rộng, bao gồm:
   - `Quotient (q)`: Thương số
   - `Remainder (r)`: Số dư
   - `s`: Hệ số nghịch đảo trung gian
3. **Hiển thị đa dạng:** Trả về kết quả dưới dạng số nguyên (integer) và dạng chuỗi nhị phân (binary).
4. **Tự động kiểm tra (Verification):** Tự động nhân ngược kết quả với số ban đầu và chia lấy dư cho `m(x)` để xác minh kết quả có chính xác bằng 1 hay không.

## 🛠 Yêu cầu hệ thống
- Trình biên dịch C++ hỗ trợ chuẩn C++17 trở lên (để sử dụng structured binding `auto [q, r]`).
- IDE gợi ý: Visual Studio Code, Code::Blocks, Dev-C++, hoặc chạy trực tiếp trên Terminal/Command Prompt.

## 💻 Cách biên dịch và chạy (Dành cho Terminal/Command Prompt)

1. Mở terminal và di chuyển đến thư mục chứa code.
2. Biên dịch file code (giả sử file tên là `main.cpp`):
   ```bash
   g++ -std=c++17 main.cpp -o main
