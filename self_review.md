# Tự đánh giá — Phạm Trần Anh · G01

## 1. Tự rà soát 4 cảnh

Ghi chú dựa trên export và báo cáo kiểm tra. Các mục còn mở cần xem lại ảnh trong CVAT.

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|
| `S02_rgb.png` | `person.seatbelt` | `guess` | ZIP ghi `worn_incorrect`. SVIRO dùng `not_worn` khi thấy rõ không có dây hoặc `unknown` khi không nhìn rõ. | Chờ rà ảnh |
| `S08_ir.png` | `child_seat`, `infant_seat` | `seat_flip` cần kiểm | Hai hộp đều ghi `rear_right`. Cần đối chiếu vị trí mỗi hộp theo hướng xe. | Chờ rà ảnh |
| `D01.png` | `hand.side` | `lr_flip` | Hai hộp đều ghi tay trái. Hộp tương ứng tay chạm vô lăng trong bản Minh là tay phải. | Đã đổi trong ZIP v2, chờ xác nhận trên CVAT |
| `D04.png` | `eye_right`, `face13` | `flag` | Mắt phải ghi `open`, cả bốn điểm mắt phải lại có `outside=1`. | Chờ rà ảnh |

## 2. Lỗi lặp nhiều nhất theo checker gốc

Sáu hộp `child_seat` ở `S03` và `S05` dùng `occupied=yes`. Schema cục bộ cho phép giá trị này. Theo v1.0, lần sau chọn `no` khi thấy ghế trống, `unknown` khi không thấy lòng ghế và kiểm bằng schema lớp đang áp dụng.

## 3. Ghi chú về disagreement_log

Ở `D01.png`, bản Minh có một tay trái và một tay phải, còn bản đầu của mình có hai tay trái. Khi có hai hộp tay, mình cần xác định trái/phải theo người và kiểm lại từng hộp ngay sau khi vẽ.
