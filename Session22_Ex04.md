# Báo cáo: Phân tích sự đánh đổi (Trade-off) giữa các chỉ số uy tín trên diễn đàn kỹ thuật

## 1. Bối cảnh vấn đề
Khi xử lý lỗi `"Git Permission Denied"`, kết quả tìm kiếm trên StackOverflow trả về 2 phương án điển hình:
- **Giải pháp 1:** Có dấu tích xanh (`Accepted Answer ✓`), đăng năm **2014**, đạt **500 upvotes**.
- **Giải pháp 2:** Không có tích xanh, đăng năm **2023**, đạt **50 upvotes**, kèm bình luận xác nhận: *"This works for Windows 11"*.

---

## 2. Bảng so sánh Ưu / Nhược điểm (Trade-off Matrix)

| Tiêu chí | Giải pháp 1 (2014 • ✓ Tích xanh • 500 Upvotes) | Giải pháp 2 (2023 • Không tích xanh • 50 Upvotes) |
| :--- | :--- | :--- |
| **Độ tin cậy lịch sử** | **Ưu:** Được cộng đồng kiểm chứng rộng rãi trong thời gian dài.<br>**Nhược:** Điểm số cao do tích lũy theo thời gian (Legacy Votes), không phản ánh hiệu quả hiện tại. | **Ưu:** Lượng vote tăng nhanh trong thời gian ngắn, phản ánh đúng giải pháp đang hoạt động.<br>**Nhược:** Tổng lượng tương tác ít hơn do mới đăng tải. |
| **Tính cập nhật với HĐH mới** | **Ưu:** Giải thích tốt lý thuyết nền tảng.<br>**Nhược:** Lỗi thời. Dựa trên chuẩn cũ (Windows 7/8, khóa `ssh-rsa` cũ, xác thực mật khẩu đã bị GitHub ngừng hỗ trợ). | **Ưu:** Tương thích trực tiếp với **Windows 11**, hỗ trợ chuẩn khóa mới (`ed25519`) và Git Credential Manager hiện đại.<br>**Nhược:** Có thể không áp dụng được cho các hệ điều hành quá cũ. |
| **Rủi ro gây hỏng thiết lập hiện tại** | **Ưu:** Không chứa mã độc.<br>**Nhược:** **Rủi ro cao.** Dễ gây xung đột giữa dịch vụ OpenSSH mặc định của Windows 11 và SSH