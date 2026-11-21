# Danh sách lớp v0 — Phạm Trần Anh · G01

## DMS

| # | Lớp / thuộc tính | Giá trị | Chức năng DMS | Quan sát trên IR |
|---|---|---|---|---|
| 1 | `eye_left`, `eye_right` | `open`, `closed`, `unknown` | Theo dõi từng mắt qua nhiều khung để phát hiện nhắm mắt kéo dài. | Có khi thấy rõ khe mắt. |
| 2 | `gaze_zone` | `road`, `mirror_l`, `mirror_r`, `mirror_c`, `cluster`, `center`, `lap`, `other` | Theo dõi thời gian mắt rời đường và phân biệt các vùng nhìn. | Tùy độ rõ của mắt, hướng đầu và ngữ cảnh. |
| 3 | `glasses` | `none`, `clear`, `sun`, `unknown` | Đánh giá độ tin cậy của tín hiệu mắt khi tài xế đeo kính. | Có điều kiện, kính râm có thể trông trong trên NIR. |
| 4 | `face13` | 13 điểm, cờ `occluded` và `outside` | Ước lượng hướng đầu và vị trí các mốc mắt. | Có khi mặt đủ lớn và các điểm không bị che. |
| 5 | `hand.on_wheel` | `yes`, `no`, `unknown` | Xác định tay có tiếp xúc vô lăng khi cần theo dõi việc cầm lái. | Có nếu thấy tay và vùng tiếp xúc. |
| 6 | `phone.state` | `held`, `mounted`, `lap` | Phân biệt cầm máy với đặt trên giá hoặc trên đùi. | Có nếu thấy cạnh, góc hoặc màn hình. |

## OMS

| # | Lớp / thuộc tính | Giá trị | Chức năng OMS | Quan sát trên IR |
|---|---|---|---|---|
| 1 | `person` | Hộp người thấy được | Phát hiện người trong cabin. | Thường thấy theo hình dáng, tùy mức che khuất. |
| 2 | `person.seat` | `driver`, `front_passenger`, `rear_left`, `rear_middle`, `rear_right` | Gắn cảnh báo với vị trí ghế. | Có nếu thấy người và mốc cabin. |
| 3 | `person.seatbelt` | `worn_correct`, `worn_incorrect`, `not_worn`, `unknown` | Nhắc thắt dây hoặc chỉnh đường đi của dây. | Tùy độ tương phản và mức che. |
| 4 | `child_seat.occupied` | `no`, `unknown` theo v1.0 | Phân biệt ghế trẻ em trống nhìn rõ với trường hợp chưa xác định được. | Có nếu thấy lòng ghế. |
| 5 | `infant_seat.facing` | `rear`, `front` | Kiểm tra hướng bố trí ghế em bé. | Có nếu thấy hình dáng và hướng ghế. |
| 6 | `object.type` | `bag`, `box`, `cup`, `other` | Phân loại đồ để trên ghế và tránh nhầm với người hoặc ghế trẻ em. | Có theo hình dạng nếu đủ dấu hiệu. |

## 2 câu hỏi leo thang

1. Nếu chỉ nhìn rõ hướng đầu ở ranh giới vùng bảng giữa và vùng ngoài danh sách, cần dấu hiệu nào để gán `center`? Khung `D02.png` có bất đồng `other/center`. Tạm giữ `other` nếu đối chiếu ảnh vẫn chưa đủ căn cứ.
2. Khi hai hộp ghế nằm sát ranh giới ghế xe, dựa vào tâm hộp hay vị trí chân đế để xác định `seat` nếu hai dấu hiệu cho kết quả khác nhau? Ở `S08_ir.png`, ZIP đang ghi cả hai là `rear_right`. Tạm giữ hai hộp riêng, rà lại vị trí trong CVAT và hỏi coach nếu vẫn không rõ.
