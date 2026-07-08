# LUX — Dự báo tuyển sinh HUST 2026 (bản cập nhật v2)

## Cách chạy
1 file duy nhất: mở `index.html` bằng trình duyệt.

## Thay đổi trong bản này

### Tab "Đổi điểm"
- Gộp còn **2 bước** thay vì 4: Bước 1 chọn phương thức, Bước 2 gồm TẤT CẢ trong 1 trang — điểm chạy, ưu tiên khu vực/đối tượng, chứng chỉ ngoại ngữ, và **kết quả điểm cuối cùng hiển thị ngay bên dưới**, cập nhật trực tiếp mỗi khi bạn thay đổi bất kỳ ô nào (không cần bấm "tiếp tục").
- **Đã sửa lỗi nút "Quay lại"** ở bước cuối không hoạt động — đã kiểm thử bằng trình duyệt thật, nút quay lại bước 1 hoạt động đúng.

### Tab "Đặt nguyện vọng"
- Bỏ toàn bộ wizard nhiều bước (không còn nhập điểm/ưu tiên/chứng chỉ riêng ở đây).
- Thay bằng: **1 ô chọn phương thức + 1 ô nhập điểm hiện có duy nhất**.
- Sau khi nhập, hiển thị điểm quy đổi tương đương sang cả thang **THPT** và **TSA**.
- Bảng so sánh đầy đủ **65 ngành**, 4 cột trạng thái: THPT vs 2025 / THPT vs 2026 (dự báo) / TSA vs 2025 / TSA vs 2026 (dự báo).
- 3 hiệu ứng trạng thái theo đúng ngưỡng bạn cho:
  - **TSA**: chênh ≤ -2 → 🚤 "Xa bờ" (thuyền trôi dạt) · chênh ≥ +2 → 😴 "Quá ok" (ngủ, thở đều) · còn lại → 🫁 "Cần cố gắng" (nhịp thở gấp, hiệu ứng máy thở oxy)
  - **THPT**: chênh ≤ -1 → 🚤 "Xa bờ" · chênh ≥ +1,5 → 😴 "Quá ok" · còn lại → 🫁 "Cần cố gắng"
- Có ô tìm kiếm để lọc nhanh theo mã/tên ngành trong bảng 65 dòng.

## Đã kiểm thử bằng Playwright (trình duyệt thật)
- Tab Đổi điểm: nhập điểm + IELTS 6.0 → cộng đúng +3.00, tổng điểm cập nhật sống động, nút quay lại hoạt động.
- Tab Đặt nguyện vọng: quy đổi TSA→THPT chính xác, cả 3 hiệu ứng (xa bờ/quá ok/cần cố gắng) đều kích hoạt đúng ngưỡng ở các ca thử khác nhau.

## Giới hạn cần biết
- Dự báo 2026 vẫn là suy luận định tính, không phải điểm chuẩn chính thức.
- Bảng quy đổi điểm dùng đúng bảng phân vị chính thức 2026 (từ file bạn cung cấp).
- Điểm cộng chứng chỉ ngoại ngữ = 1/2/3/4/5 (thang 100) theo đúng bảng bạn xác nhận.
