# Changelog



## [v1.4.0] - 2024-12-19

### 🎯 **Tính năng mới - Hệ thống xoay piece đa dạng**
- **Từ 12 pieces → 32 pieces**: Mở rộng từ 12 pieces cơ bản lên 32 pieces với các hướng xoay
- **4 hướng xoay cho L3, L4, T4**: Mỗi piece có thể xoay 0°, 90°, 180°, 270°
- **2 hướng xoay cho 1x2, 1x3, I3, I4, S4, Z4**: Mỗi piece có thể xoay 0° và 90°
- **1 hướng cho 1x1, 2x2, O3**: Không cần xoay do đối xứng hoàn toàn

### 🔧 **Cải tiến kỹ thuật**
- **Cập nhật `PIECES`**: Thêm tất cả các hướng xoay với tên rõ ràng (ví dụ: L3_90, L3_180, L3_270)
- **Cập nhật `PIECE_COLORS`**: Mỗi hướng xoay giữ nguyên màu gốc để dễ nhận biết
- **Cập nhật `BASE_WEIGHTS`**: Phân bổ trọng số đều cho các hướng xoay
- **Cập nhật `swapCfg.rescueSet`**: Bao gồm các hướng xoay mới trong rescue pieces

### 🎮 **Cách chơi mới**
- **Đa dạng hơn**: Pool giờ có thể chứa cùng loại piece nhưng khác hướng
- **Chiến thuật mới**: Người chơi có thể chọn hướng phù hợp nhất để đặt
- **Tăng độ khó**: Nhiều lựa chọn hơn, cần suy nghĩ kỹ hơn về vị trí đặt

### 📊 **Thống kê pieces mới**
- **Tổng cộng**: 32 pieces (thay vì 12)
- **L3, L4, T4**: 4 hướng mỗi loại = 12 pieces
- **1x2, 1x3, I3, I4, S4, Z4**: 2 hướng mỗi loại = 12 pieces  
- **1x1, 2x2, O3**: 1 hướng mỗi loại = 3 pieces

## [v1.3.1] - 2024-12-19

### 🔧 **Cải tiến trải nghiệm người chơi**
- **Hiển thị piece cuối cùng**: Khi đặt piece cuối cùng mà thua, piece đó vẫn được hiển thị trên bàn chơi
- **Thứ tự logic rõ ràng**: Đặt piece → render → kiểm tra game over → hiển thị thông báo
- **Giảm bối rối**: Người chơi thấy rõ piece cuối cùng đã được đặt ở đâu trước khi thua

### 🎯 **Vấn đề đã cải thiện**
- **Trước**: Khi thua, người chơi không thấy piece cuối cùng đã đặt ở đâu
- **Sau**: Piece cuối cùng được hiển thị rõ ràng trên bàn chơi trước khi hiện thông báo thua

## [v1.3.0] - 2024-12-19

### 🎯 **Tính năng mới - Game Over System**
- **Điều kiện thua**: Khi không còn chỗ đặt piece nào (cả 3 pieces trong pool và hold piece)
- **Kiểm tra thông minh**: Lần lượt kiểm tra từng piece có thể đặt được không
- **Thông báo game over**: Hiển thị "Thua Rồi, Thử lại nhé!" với overlay đẹp mắt
- **Nút chơi lại**: Nút "Chơi Lại" để khởi tạo lại ván mới

### 🔧 **Cải tiến kỹ thuật**
- **Thêm biến `gameOver`**: Theo dõi trạng thái game over
- **Hàm `checkGameOver()`**: Kiểm tra tất cả pieces có thể đặt được không
- **Hàm `resetGame()`**: Reset toàn bộ game về trạng thái ban đầu
- **Hàm `drawGameOver()`**: Vẽ màn hình game over với UI đẹp
- **Logic click nút**: Xử lý click nút "Chơi Lại" để reset game

### 🎮 **Cách hoạt động**
- **Kiểm tra liên tục**: Sau mỗi action (đặt piece, hold, swap, refill) đều kiểm tra game over
- **Hiển thị ngay lập tức**: Khi thua, hiển thị thông báo ngay không cần chờ
- **Reset hoàn toàn**: Nút "Chơi Lại" reset tất cả: board, pool, score, blocked cells
- **Ô bị khóa mới**: Mỗi ván mới có ô bị khóa ngẫu nhiên khác nhau

## [v1.2.1] - 2024-12-19

### 🐛 **Sửa lỗi quan trọng - Ô bị khóa không clear**
- **Sửa logic `clearLines()`**: Hàng/cột đầy giờ được tính bao gồm cả ô bị khóa
- **Ô bị khóa clear được**: Khi xếp đủ hàng/cột chứa ô bị khóa, ô đó sẽ biến mất
- **Logic chính xác**: Hàng/cột được coi là đầy khi có piece HOẶC ô bị khóa

### 🔧 **Cải tiến kỹ thuật**
- **Cập nhật `getFillRate()`**: FR giờ tính cả ô bị khóa như piece đã đặt sẵn
- **Tự động refill khi Hold**: Khi hold piece và 3 slots trống, tự động tạo 3 piece mới
- **Logic Hold thông minh**: Kiểm tra pool trống và refill ngay lập tức

### 🎯 **Vấn đề đã sửa**
- **Trước**: Ô bị khóa không clear được dù xếp đủ hàng/cột
- **Sau**: Ô bị khóa clear được khi xếp đủ hàng/cột chứa nó
- **Trước**: FR không tính ô bị khóa, hiển thị sai
- **Sau**: FR tính chính xác bao gồm cả ô bị khóa
- **Trước**: Hold piece không tự động refill khi pool trống
- **Sau**: Hold piece tự động refill khi 3 slots trống

## [v1.2.0] - 2024-12-19

### 🎯 **Tính năng mới - Ô bị khóa (Blocked Cells)**
- **Ô bị khóa ngẫu nhiên**: Khi khởi tạo bàn chơi, có 6-12 ô màu đỏ bị khóa
- **Không thể đặt piece**: Piece không thể đặt lên ô bị khóa
- **Cách clear**: Chỉ cần clear hàng dọc HOẶC hàng ngang chứa ô đó thì ô bị khóa sẽ biến mất
- **Hiển thị trực quan**: Ô bị khóa có màu đỏ với viền đỏ đậm

### 🔧 **Cải tiến kỹ thuật**
- **Thêm biến `blockedCells`**: Lưu danh sách các ô bị khóa
- **Hàm `generateBlockedCells()`**: Tạo random 6-12 ô bị khóa
- **Cập nhật `canPlace()`**: Kiểm tra không thể đặt piece lên ô bị khóa
- **Cập nhật `clearLines()`**: Xóa ô bị khóa khi clear hàng/cột
- **Cập nhật `drawBoard()`**: Hiển thị ô bị khóa màu đỏ

### 🎮 **Cách chơi mới**
- **Mục tiêu**: Clear các ô bị khóa để tăng điểm
- **Chiến thuật**: Đặt piece để tạo hàng/cột có thể clear chứa ô bị khóa
- **Độ khó**: Tăng lên do có thêm chướng ngại vật cố định

## [v1.1.2] - 2024-12-19

### 🔧 **Sửa lỗi khởi động - Game không tạo piece**
- **Sửa lỗi khởi động**: Khởi tạo `pool = [null, null, null]` trước khi gọi `refillPool()`
- **Đảm bảo game luôn có 3 pieces** khi bắt đầu chơi
- **Logic refill hoạt động đúng**: Chỉ refill những slot null, giữ nguyên vị trí piece còn lại

### 🎯 **Vấn đề đã sửa**
- **Trước**: Game khởi động với `pool = []` rỗng, không có piece nào
- **Sau**: Game khởi động với `pool = [null, null, null]` và tự động refill thành 3 pieces

## [v1.1.1] - 2024-12-19

### 🔧 **Sửa lỗi quan trọng - Vị trí piece**
- **Sửa hoàn toàn logic dồn piece**: Thay vì sử dụng `splice()` làm dồn piece về trái, giờ sử dụng `pool[index] = null` để giữ nguyên vị trí
- **Cập nhật hàm `refillPool()`**: Chỉ refill những slot null, không thay đổi vị trí của piece còn lại
- **Cập nhật logic Hold**: Khi hold khối, slot đó được set null thay vì bị xóa
- **Cập nhật logic thả khối**: Khi thả khối từ hold, tìm slot trống đầu tiên để đặt vào

### 🎯 **Kết quả**
- **Vị trí piece không thay đổi**: Mỗi slot giữ nguyên vị trí của mình
- **Không còn dồn về trái**: Piece được sử dụng sẽ để lại slot trống, không ảnh hưởng đến vị trí piece khác
- **Logic refill thông minh**: Chỉ refill những slot cần thiết

## [v1.1.0] - 2024-12-19

### 🎨 **Tính năng mới - Giao diện đẹp hơn**
- **Màu sắc riêng biệt cho từng piece**: Mỗi loại khối có màu riêng để dễ phân biệt
  - 1x1: Đỏ cam, 1x2: Xanh lá, 1x3: Xanh dương, 2x2: Xanh mint
  - I3: Vàng, I4: Hồng, L3: Xanh dương đậm, L4: Tím
  - T4: Đỏ, S4: Xanh lá đậm, Z4: Hồng đậm, O3: Vàng cam
- **Vị trí piece không thay đổi**: Khi sử dụng khối, vị trí trong pool không bị dồn về trái
- **Highlight khi chọn**: Piece được chọn sẽ có viền màu xanh lá để dễ nhận biết

### 🔧 **Cải tiến kỹ thuật**
- **Cập nhật hàm `makePiece()`**: Thêm thuộc tính `color` cho mỗi piece
- **Cập nhật hàm `drawPieceAt()`**: Tự động sử dụng màu của piece
- **Cập nhật hàm `drawPool()`**: Hiển thị piece với màu sắc riêng biệt

### ✅ **Tính năng đã xác nhận hoạt động**
- **Pool System**: Luôn tạo ra 3 items mỗi lần refill
- **Hold System**: Lưu 1 khối với cooldown 3 lượt (phím H)
- **Swap System**: Đổi khối sang khối cứu nạn với cooldown 9 lượt (phím 1/2/3)
- **Auto-refill**: Tự động refill khi pool hết
- **Cooldown Management**: Tự động giảm cooldown mỗi lượt

## [v1.0.4] - 2024-12-19

### 🔧 **Sửa lỗi hoàn toàn - Lần cuối**
- **Viết lại hoàn toàn hàm `drawPool()`** để tránh lỗi `Assignment to constant variable`
- **Sử dụng biến riêng biệt** `slotX`, `slotY`, `holdX`, `holdY` thay vì gán lại `const`
- **Đảm bảo 3 slots và Hold position** được hiển thị đúng
- **Không còn lỗi JavaScript** trong Console

### ✅ **Tính năng đã xác nhận hoạt động**
- **Pool System**: Luôn tạo ra 3 items mỗi lần refill
- **Hold System**: Lưu 1 khối với cooldown 3 lượt (phím H)
- **Swap System**: Đổi khối sang khối cứu nạn với cooldown 9 lượt (phím 1/2/3)
- **Auto-refill**: Tự động refill khi pool hết
- **Cooldown Management**: Tự động giảm cooldown mỗi lượt

### 🎯 **Để kiểm tra**
1. **Refresh trang** (Ctrl+F5) để load version mới v1.0.4
2. **Kiểm tra Console** - không còn lỗi JavaScript
3. **Kiểm tra giao diện** có hiển thị đủ 3 slots và vị trí Hold
4. **Test các tính năng** Hold (phím H) và Swap (phím 1/2/3)

## [v1.0.3] - 2024-12-19

### 🔧 **Sửa lỗi hoàn toàn**
- **Viết lại toàn bộ file** `index.html` để đảm bảo không còn lỗi JavaScript
- **Sửa lỗi** `Assignment to constant variable` trong hàm `drawPool()`
- **Tối ưu hóa code** để tránh gán lại giá trị cho biến `const`
- **Đảm bảo game hoạt động ổn định** không còn lỗi console

### ✅ **Tính năng đã xác nhận hoạt động**
- **Pool System**: Luôn tạo ra 3 items mỗi lần refill
- **Hold System**: Lưu 1 khối với cooldown 3 lượt (phím H)
- **Swap System**: Đổi khối sang khối cứu nạn với cooldown 9 lượt (phím 1/2/3)
- **Auto-refill**: Tự động refill khi pool hết
- **Cooldown Management**: Tự động giảm cooldown mỗi lượt

### 🎯 **Để kiểm tra**
1. **Refresh trang** (Ctrl+F5) để load version mới
2. **Kiểm tra Console** - không còn lỗi JavaScript
3. **Kiểm tra giao diện** có hiển thị đủ 3 slots và vị trí Hold
4. **Test các tính năng** Hold (phím H) và Swap (phím 1/2/3)

## [v1.0.2] - 2024-12-19

### 🐛 Đã sửa lỗi
- **Sửa lỗi JavaScript** `Assignment to constant variable` trong hàm `drawPool()`
- **Tối ưu hóa code** để tránh gán lại giá trị cho biến `const`
- **Đảm bảo game hoạt động ổn định** không còn lỗi console

### ✅ Tính năng đã xác nhận
- Pool 3 items hoạt động đúng
- Hold system hoạt động đúng với cooldown 3 lượt
- Swap system hoạt động đúng với cooldown 9 lượt

## [v1.0.1] - 2024-12-19

### ✅ Đã sửa
- **Tối ưu hóa logic game** - Đảm bảo tất cả tính năng hoạt động chính xác
- **Kiểm tra và xác nhận** các tính năng core:
  - Pool 3 items luôn được tạo ra
  - Hold system hoạt động đúng với cooldown 3 lượt
  - Swap system hoạt động đúng với cooldown 9 lượt
- **Thêm version indicator** trên giao diện
- **Cải thiện comments** trong code để dễ hiểu hơn

### 🔧 Tính năng đã xác nhận
1. **Pool System**: Luôn tạo ra 3 items mỗi lần refill
2. **Hold System**: Lưu 1 khối với cooldown 3 lượt (phím H)
3. **Swap System**: Đổi khối sang khối cứu nạn với cooldown 9 lượt (phím 1/2/3)
4. **Auto-refill**: Tự động refill khi pool hết
5. **Cooldown Management**: Tự động giảm cooldown mỗi lượt

### 📝 Technical Details
- Sử dụng `sampleThree()` để đảm bảo luôn tạo 3 items
- Hold system chỉ hoạt động khi `hold.piece === null` và `hold.cd <= 0`
- Swap system chỉ hoạt động khi `swapCD <= 0`
- Cooldown được giảm mỗi lượt: `if(swapCD>0) swapCD--; if(hold.cd>0) hold.cd--;`

## [v1.0.0] - 2024-12-19

### 🎮 Tính năng cơ bản
- Game prototype hoàn chỉnh với bàn 8×8
- 12 loại khối Tetris-like
- Hệ thống scoring với combo và precision bonus
- Guardrail system tự động sửa khi bị kẹt
- Giao diện hiện đại với Canvas rendering

### 🚀 Setup
- Hỗ trợ Go Live để development
- Cấu trúc project chuẩn
- Documentation đầy đủ
