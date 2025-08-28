# Block Tetrist - Game Đặt Khối Thông Minh

## 🎮 Giới Thiệu
Block Tetrist là một game puzzle chiến thuật với bàn chơi 8×8, nơi người chơi đặt các khối có hình dạng khác nhau để tạo thành hàng và cột hoàn chỉnh. Game được thiết kế với giao diện hiện đại và nhiều tính năng nâng cao.

## ✨ Tính Năng Chính

### 🎯 4 Game Modes
- **Basic Mode**: Chain multiplier cơ bản
- **Blocker Mode**: Durable pieces + Precision bonus
- **Multiplier Mode**: Bonus points system
- **Blast Mode**: Bomb explosion system

### 🧩 Hệ Thống Khối
- **65 loại khối** với 4 hướng xoay khác nhau
- **Smart piece generation** với bias system
- **Rescue pieces** cho tình huống kẹt

### 🏆 Hệ Thống Điểm
- **Multi-layered scoring**: Cell, Line, Precision, Combo
- **Chain multiplier** với visual feedback
- **Cross-clear bonuses** cho việc clear đồng thời hàng/cột
- **Bonus piece multipliers** (x2 đến x7) với hệ thống lifetime

### 🎨 Giao Diện
- **Modern gradient design** với smooth animations
- **Combo text animations** với streak-based messages
- **Responsive design** cho mọi kích thước màn hình
- **Mobile-optimized** với touch controls

## 📱 Mobile Optimization (v1.9.16+)

### 🚀 Tính Năng Mobile
- **Complete mobile layout redesign** cho màn hình dọc 9:16
- **Touch controls** thay thế keyboard controls trên mobile
- **Drag & Drop system** với visual preview
- **Mobile control buttons** cho Hold và Swap operations
- **Responsive design** với tất cả nội dung vừa trong 1 màn hình mobile

### 🎮 Điều Khiển Mobile
- **Touch & Drag**: Chọn khối → kéo lên bàn chơi → thả để đặt
- **Hold Button**: Nút Hold thân thiện với touch và hiển thị cooldown
- **Swap Buttons**: Nút Swap thân thiện với touch cho slot 1, 2, 3
- **Visual feedback**: Drop preview và drag indicators

### 📱 Mobile Features
- **Auto-detection** của mobile devices
- **Adaptive UI** chuyển đổi giữa desktop và mobile controls
- **Touch-optimized** button sizes và spacing
- **Gesture support** cho natural mobile interaction

## 🎮 Cách Chơi

### 🖱️ Desktop Controls
- **Click** vào khối trong pool để chọn
- **Click** lên ô trên bàn để đặt khối
- **H** - Hold khối đang chọn
- **1/2/3** - Swap khối slot 1/2/3
- **Chuột phải** - Bỏ chọn

### 📱 Mobile Controls
- **Touch & Drag**: Chạm vào khối → kéo lên bàn chơi → thả để đặt
- **Hold Button**: Nút Hold với cooldown display
- **Swap Buttons**: Nút Swap cho từng slot với cooldown display

### 🎯 Mục Tiêu
- Đặt khối để tạo thành hàng/cột hoàn chỉnh
- Clear càng nhiều line càng tốt
- Duy trì combo để tăng điểm
- Quản lý Fill Rate thông minh
- Clear các ô có độ bền (màu đỏ) để tăng điểm

## 🏆 Hệ Thống Điểm

### 📊 Scoring Components
- **Cell Points**: Điểm cơ bản cho mỗi ô đặt
- **Line Bonus**: Bonus cho việc clear hàng/cột
- **Precision Bonus**: Bonus cho việc clear nhiều line cùng lúc
- **Combo Multiplier**: Nhân điểm theo streak liên tiếp
- **Bonus Multipliers**: Nhân điểm từ bonus pieces (x2-x7)

### 🔄 Chain System
- Clear liên tiếp tăng multiplier (≤1.5×)
- Combo tích lũy theo thời gian
- Reset combo khi không clear line

## 🎨 Game Modes

### 🎯 Basic Mode
- Chain multiplier cơ bản
- Không có special mechanics
- Tập trung vào gameplay cốt lõi

### 🛡️ Blocker Mode
- Durable pieces với độ bền
- Precision bonus cho việc clear nhiều line
- Strategic depth với health management

### ⭐ Multiplier Mode
- Bonus pieces spawn sau line clear
- Multiplier stacking system
- High-risk, high-reward gameplay

### 💣 Blast Mode
- Bomb pieces với explosion mechanics
- 3x3 explosion areas
- Strategic bomb placement và timing

## 🔧 Technical Features

### 💾 Data Persistence
- **Local Storage** cho high scores
- **Mode-specific** high score tracking
- **Persistent settings** giữa sessions

### 🎮 Performance
- **Canvas rendering** với hardware acceleration
- **Optimized algorithms** cho smooth gameplay
- **Responsive design** cho mọi device

### 🌐 Cross-Platform
- **HTML5/JavaScript** - chạy trên mọi browser
- **Touch support** cho mobile devices
- **Keyboard support** cho desktop

## 📱 Mobile Experience

### 📐 Layout Optimization
- **9:16 Portrait** layout optimization
- **Single screen** experience (không scroll)
- **Touch-friendly** button sizes
- **Optimized spacing** cho mobile readability

### 🎯 Touch Controls
- **Natural gestures** cho piece placement
- **Visual feedback** cho mọi action
- **Intuitive UI** cho mobile users
- **Responsive touch** handling

## 🚀 Cài Đặt & Chạy

### 📥 Download
1. Clone repository hoặc download source code
2. Mở `index.html` trong browser
3. Chọn game mode và bắt đầu chơi

### 🌐 Online Play
- Game có thể chạy trực tiếp từ file HTML
- Không cần server hoặc internet connection
- Tương thích với mọi modern browser

### 📱 Mobile Setup
- Mở game trên mobile browser
- Game tự động detect mobile device
- UI tự động chuyển sang mobile mode

## 📊 System Requirements

### 💻 Desktop
- Modern browser với HTML5 support
- JavaScript enabled
- Minimum 1024x768 resolution

### 📱 Mobile
- iOS 12+ hoặc Android 8+
- Modern mobile browser
- Touch screen support
- Portrait orientation recommended

## 🔄 Version History

### v1.9.16-mobile (Latest)
- Complete mobile optimization
- Touch controls và drag & drop
- 9:16 portrait layout
- Mobile-optimized UI

### v1.9.15
- 4 game modes
- 65 unique pieces
- Advanced scoring system
- Modern UI design

## 🤝 Contributing
Game được phát triển với mục tiêu tạo ra trải nghiệm puzzle game tốt nhất cho cả desktop và mobile. Mọi feedback và suggestions đều được welcome!

## 📄 License
Game được phát triển cho mục đích giáo dục và giải trí. Feel free to use và modify theo nhu cầu của bạn.

---

**🎮 Chơi ngay và thử thách bản thân với Block Tetrist!**
