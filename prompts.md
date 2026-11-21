# Khai báo dùng AI — Phạm Trần Anh

| # | Công cụ | Câu hỏi tóm tắt | Cách dùng kết quả | Cách kiểm lại |
|---|---|---|---|---|
| 1 | Codex | Clone repo, hướng dẫn CVAT, lập nhóm và nộp bài. | Chuẩn bị repo và làm theo các bước của lab. | Đối chiếu GUIDE, RULES và SUBMISSION. |
| 2 | Codex | Giải nén G01, gom 22 ảnh, tìm và quản lý các ZIP tải về. | Chuẩn bị dữ liệu cục bộ và chọn đúng file. | Kiểm tên, vị trí và số lượng file. |
| 3 | Codex | Viết lệnh kiểm, chạy kiểm và lập báo cáo. | Tạo các báo cáo kiểm tra cuối và kiểm lại hai checkpoint từ v2. | Đối chiếu số ảnh, tag và kết quả hai schema. |
| 4 | Codex | So ZIP của Anh và Minh, điền review. | Ghi 5 dòng nhận xét từ XML và guideline. | Hai dòng còn mơ hồ cần cùng Minh xem lại trên CVAT. |
| 5 | Codex | Sửa một giá trị tay trong ZIP v2. | Đổi `hand.side` ở `D01` trực tiếp trong XML dựa trên hộp tương ứng của Minh. | Đã chạy checker. Cần đối chiếu trên CVAT và xuất lại theo quy trình lớp. |
| 6 | Codex | Điền các file nộp và chuẩn bị nội dung gửi Minh. | Soạn nháp mẫu nộp từ dữ liệu nhãn và đề bài. | Người làm cần xác nhận quan sát ảnh, thông tin nhóm và đáp án cá nhân. |
| 7 | Codex | Kiểm đáp án Exit ticket và đối chiếu bốn khung cho nhật ký IR. | Chạy Python cục bộ để đo độ sáng trong các vùng dựa trên tọa độ XML, rồi cập nhật nhật ký. | Đối chiếu số đo với XML và guideline. Các kết luận về nhãn vẫn cần xem ảnh trong CVAT. |

Codex đọc tài liệu, tên file và nhãn XML. Các ảnh cabin được giải nén và sao chép cục bộ.
