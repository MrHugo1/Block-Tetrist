# 🎮 Block Tetrist - Game Đặt Khối Thông Minh

**Phiên bản:** v1.9.16  
**Ngày cập nhật:** 19/12/2024

Một game puzzle thông minh với bàn chơi 8×8, kết hợp giữa chiến thuật đặt khối và hệ thống điểm phức tạp.

## ✨ Tính Năng Mới Nhất (v1.8.0)

### 🎮 Hệ Thống Game Modes
- **4 Chế Độ Chơi**: Basic, Blocker, Multiplier, Blast
- **Basic Mode**: Chain multiplier cơ bản
- **Blocker Mode**: Durable pieces + Precision bonus
- **Multiplier Mode**: Bonus points system
- **Blast Mode**: Bomb explosion system
- **High Score Riêng Biệt**: Mỗi mode có điểm cao nhất riêng

### 💣 Hệ Thống Bomb (Blast Mode)
- **Ô Bomb Chiến Thuật**: Xuất hiện khi Fill Rate > 60% (1 lần/1 ván)
- **Nổ 3x3 Thông Minh**: Bomb nổ vùng 3x3 với bomb ở trung tâm
- **Kích Hoạt Bonus**: Bomb có thể kích hoạt ô bonus trong vùng nổ
- **Tính Điểm Nổ**: Mỗi ô bị nổ cho điểm tương ứng
- **Lifetime Management**: Bomb tự biến mất sau 1-2 lượt nếu không nổ

### 🎁 Hệ Thống Bonus Points
- **Ô Bonus x2-x7**: Xuất hiện sau khi clear line (30% chance)
- **Nhân Điểm Thông Minh**: Clear line chứa ô bonus → nhân điểm tương ứng
- **Nhân Dồn**: Nhiều ô bonus cùng lúc → nhân dồn (x2 × x5 = x10)
- **Tự Động Biến Mất**: Ô bonus tồn tại 2-4 lượt tùy theo hệ số nhân

### 🔧 Sửa Lỗi Quan Trọng
- **Sửa Logic Spawn**: Bonus pieces giờ spawn trên pieces có sẵn, không phải ô trống
- **Sửa Thứ Tự Xử Lý**: Spawn bonus mới trước khi xóa bonus cũ
- **Sửa Logic Clear Line**: Bonus pieces được tính đúng trong việc clear line
- **Thêm Debug Logging**: Console.log chi tiết để track hoạt động của bonus system

## 🎯 Tính Năng Chính

### 🧩 Hệ Thống Khối
- **71 Loại Khối**: Bao gồm tất cả hướng xoay (0°, 90°, 180°, 270°)
- **Pool 3 Khối**: Chọn khối từ 3 khối có sẵn
- **Hold System**: Lưu 1 khối (CD 3 lượt)
- **Swap System**: Đổi khối cứu nạn (CD 9 lượt)

### 🏆 Hệ Thống Điểm
- **Chain Multiplier**: Clear liên tiếp tăng multiplier (≤1.5×)
- **Precision Bonus**: Clear ≥2 line nhân điểm (1.2× / 1.5×)
- **Combo System**: Tích lũy theo thời gian
- **Bonus Multiplier**: Ô x2-x7 nhân điểm khi clear line

### 🎨 Giao Diện
- **Thiết Kế Hiện Đại**: Gradient, animation mượt mà
- **Responsive**: Tối ưu cho mọi kích thước màn hình
- **Visual Feedback**: Text animation, combo display
- **Debug Panel**: Thông tin chi tiết về game state

## 🎮 Cách Chơi

### 📱 Điều Khiển
- **Chuột trái**: Chọn khối từ pool, click đặt lên bàn
- **Chuột phải**: Bỏ chọn khối
- **Phím H**: Hold khối đang chọn
- **Phím 1/2/3**: Swap khối slot tương ứng

### 📱 **Mobile Controls (Mới!)**
- **Touch**: Tap để chọn và đặt khối
- **Long Press**: Giữ 500ms để bỏ chọn khối
- **Virtual Buttons**: Hold, Swap 1/2/3, Deselect
- **Responsive**: Tự động điều chỉnh cho màn hình dọc

### 🎯 Mục Tiêu
- Đặt khối để tạo thành hàng/cột hoàn chỉnh
- Clear càng nhiều line càng tốt
- Duy trì combo để tăng điểm
- Quản lý Fill Rate thông minh
- Clear các ô có độ bền (màu đỏ) để tăng điểm
- Tận dụng ô bonus để nhân điểm
- **Chiến thuật sử dụng bomb**: Kích hoạt bomb đúng thời điểm để tối đa hóa điểm

## 🔧 Cài Đặt & Chạy

### 📋 Yêu Cầu
- Trình duyệt web hiện đại (Chrome, Firefox, Safari, Edge)
- Hỗ trợ HTML5 Canvas
- JavaScript enabled
- **Mobile**: iOS Safari 12+, Chrome Mobile 70+, Samsung Internet 10+

### 🚀 Chạy Game
1. Tải file `index.html`
2. Mở bằng trình duyệt web
3. Bắt đầu chơi ngay lập tức!

### 📱 **Mobile Gaming**
- **Portrait Mode**: Tối ưu cho màn hình dọc
- **Touch Controls**: Điều khiển bằng ngón tay
- **Responsive Design**: Tự động điều chỉnh kích thước
- **Virtual Buttons**: Nút điều khiển ảo cho mobile

### 🧪 Test Bonus System
- Mở file `test.html` để kiểm tra hệ thống bonus
- Chạy comprehensive test suite
- Xem console.log để debug

## 📊 Thống Kê Game

### 📈 Scoring System
- **Đặt khối**: 1 điểm/ô
- **Clear line**: 10 điểm/line
- **Precision bonus**: 1.2× (2 lines), 1.5× (3+ lines)
- **Chain multiplier**: Tối đa 1.5×
- **Bonus multiplier**: x2 đến x7 (nhân dồn)
- **Bomb explosion**: 1 điểm/ô bị nổ + bonus points từ bonus pieces

### 🎲 Game Mechanics
- **Bàn chơi**: 8×8 ô
- **Khối tối đa**: 71 loại với 4 hướng xoay
- **Pool size**: 3 khối
- **Bonus pieces**: Tối đa 4 ô trên bàn
- **Durable pieces**: 6-12 ô với độ bền 2-5
- **Bomb pieces**: Tối đa 1 ô trên bàn (khi FR > 60%)

## 🐛 Báo Cáo Lỗi & Đóng Góp

### 📝 Báo Cáo Lỗi
Nếu gặp vấn đề, vui lòng:
1. Kiểm tra console log để xem debug info
2. Ghi lại các bước để tái hiện lỗi
3. Mô tả chi tiết vấn đề gặp phải

### 🔧 Đóng Góp Code
Để đóng góp:
1. Fork repository
2. Tạo feature branch
3. Commit changes với message rõ ràng
4. Tạo Pull Request

## 📜 Lịch Sử Phiên Bản

### v1.8.4 (19/12/2024)
- 🐛 Sửa lỗi duplicate piece names gây overwrite
- 🔧 Cập nhật piece count chính xác từ 44 → 71 pieces
- 🎯 Sửa Cross shape rotations để có 4 hướng khác nhau
- 📝 Cập nhật documentation và debug info

### v1.8.3 (19/12/2024)
- ✨ Thêm 12 pieces mới với 4 hướng xoay mỗi loại
- 🧩 Tổng cộng 71 pieces (tăng từ 32)
- 🎨 Màu sắc riêng biệt cho từng loại piece mới
- 🔧 Cải thiện hệ thống sinh piece và rotation

### v1.8.0 (19/12/2024)
- ✨ Thêm hệ thống game modes hoàn chỉnh với 4 chế độ chơi
- 🎮 Basic Mode: Chain multiplier cơ bản
- 🛡️ Blocker Mode: Durable pieces + Precision bonus
- ⭐ Multiplier Mode: Bonus points system
- 💣 Blast Mode: Bomb explosion system
- 🏆 High score riêng biệt cho từng mode
- 🎨 Giao diện chọn mode đẹp mắt với popup

### v1.7.0 (19/12/2024)
- ✨ Thêm hệ thống bomb hoàn chỉnh với nổ 3x3
- 🎯 Bomb spawn khi Fill Rate > 60% (1 lần/1 ván)
- 💥 Bomb có thể kích hoạt bonus pieces trong vùng nổ
- 🔧 Tích hợp bomb system với bonus và durable pieces
- 📝 Cập nhật version và documentation

### v1.6.2 (19/12/2024)
- 🐛 Sửa toàn bộ hệ thống bonus points
- 🔧 Cải thiện logic spawn và xử lý bonus
- 📝 Thêm comprehensive debug logging
- 🧪 Tạo test suite cho bonus system

### v1.6.1 (19/12/2024)
- 🐛 Sửa logic spawn bonus pieces
- 🔧 Thêm debug logging
- 📊 Tạm thời set spawn chance = 100%

### v1.6.0 (19/12/2024)
- ✨ Thêm hệ thống bonus points hoàn chỉnh
- 🎨 Color coding cho bonus pieces
- 🎯 Lifetime management system
- 📊 Multiplier stacking mechanics

### v1.5.0 (19/12/2024)
- ✨ Hệ thống durable pieces
- 🎯 Cross clear bonus mechanics
- 🏆 Enhanced combo system
- 🎮 Improved game over logic

Xem [CHANGELOG.md](CHANGELOG.md) để biết chi tiết đầy đủ.

## 📄 Giấy Phép

Dự án này được phát hành dưới giấy phép MIT. Xem file LICENSE để biết thêm chi tiết.

## 🙏 Lời Cảm Ơn

Cảm ơn tất cả những ai đã đóng góp ý tưởng và phản hồi để cải thiện game!

---

**🎮 Chúc bạn chơi game vui vẻ và đạt điểm cao! 🏆**
