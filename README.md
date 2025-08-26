# Block Tetrist 🎮

**Game Đặt Khối Thông Minh - Bàn 8×8** | Version: **v1.5.0**

Một trò chơi puzzle thông minh kết hợp giữa Tetris và Block Puzzle, với hệ thống chiến thuật sâu sắc và giao diện hiện đại.

## ✨ **Tính Năng Chính**

### 🎯 **Core Gameplay**
- **Bàn chơi 8×8**: Grid-based puzzle với 64 ô
- **32 Unique Pieces**: 12 loại cơ bản + 20 hướng xoay khác nhau
- **Pool System**: 3 pieces sẵn sàng để chọn
- **Hold System**: Lưu 1 piece để sử dụng sau (CD 3 lượt)
- **Swap System**: Thay thế piece khẩn cấp (CD 9 lượt)

### 🚀 **Durable Pieces System (v1.5.0)**
- **Pieces có độ bền**: Thay thế ô bị khóa với pieces có durability 2-5 hits
- **Cross Clear Bonus**: Giảm durability đặc biệt khi clear cả hàng và cột
  - **1x1 cross**: -3 durability
  - **2x1 hoặc 1x2 cross**: -4 durability  
  - **2x2 cross**: -6 durability
  - **2x3 hoặc 3x2+ cross**: Clear TẤT CẢ durable pieces!
- **Visual Feedback**: Hiển thị số durability với màu sắc thay đổi

### 🎮 **Advanced Systems**
- **Combo Streak**: Hệ thống combo liên tiếp (Good → Nice! → Great! → ... → Ultimate!)
- **Strategic Obstacles**: Durable pieces tạo thách thức chiến thuật
- **Fill Rate Management**: Tự động điều chỉnh độ khó dựa trên board state
- **Rescue System**: Tự động sửa khi pool không thể đặt được

## 🎯 **Cách Chơi**

### 📱 **Điều Khiển**
- **Chuột trái**: Chọn piece từ pool, đặt lên board
- **Chuột phải**: Bỏ chọn piece
- **Phím H**: Hold piece đang chọn
- **Phím 1/2/3**: Swap piece ở slot tương ứng

### 🎲 **Mục Tiêu**
1. **Đặt pieces** để tạo hàng/cột hoàn chỉnh
2. **Clear lines** để tăng điểm và tạo khoảng trống
3. **Quản lý durable pieces** - cần nhiều lần hit để clear
4. **Tạo cross clears** để nhận bonus durability reduction
5. **Duy trì combo streak** để tăng điểm tối đa

### 🏆 **Hệ Thống Điểm**
- **Base Score**: 1 điểm cho mỗi ô đặt
- **Line Bonus**: 10 điểm cho mỗi line clear
- **Precision Bonus**: 1.2× cho 2 lines, 1.5× cho 3+ lines
- **Combo Multiplier**: Tối đa 1.5× cho combo liên tiếp
- **Cross Clear Bonus**: Điểm thưởng đặc biệt cho cross clears

## 🔧 **Technical Features**

### 🎨 **UI/UX**
- **Responsive Design**: Tối ưu cho mọi kích thước màn hình
- **Smooth Animations**: Hiệu ứng mượt mà cho combo text và transitions
- **Modern Styling**: Gradient colors, shadows, và visual feedback
- **Accessibility**: High contrast và clear visual indicators

### 💾 **Performance**
- **Canvas Rendering**: Smooth 60fps gameplay
- **Efficient Algorithms**: Optimized line clearing và game over detection
- **Memory Management**: Smart piece pooling và cleanup
- **Local Storage**: Lưu high score và game state

### 🧠 **AI & Logic**
- **Intelligent Pool Generation**: Bias system cho rescue pieces
- **Guardrail System**: Tự động sửa impossible game states
- **Strategic Piece Distribution**: Balanced piece weights cho gameplay fair
- **Adaptive Difficulty**: Điều chỉnh độ khó dựa trên player performance

## 🚀 **Installation & Setup**

### 📥 **Quick Start**
1. **Clone repository** hoặc download source code
2. **Mở `index.html`** trong browser hiện đại
3. **Bắt đầu chơi** ngay lập tức!

### 🌐 **Browser Support**
- **Chrome/Edge**: ✅ Full support
- **Firefox**: ✅ Full support  
- **Safari**: ✅ Full support
- **Mobile**: ✅ Responsive design

### 📱 **Mobile Experience**
- **Touch Controls**: Tối ưu cho màn hình cảm ứng
- **Responsive Layout**: Tự động điều chỉnh cho mobile
- **Performance**: Smooth gameplay trên mobile devices

## 🎮 **Game Modes & Features**

### 🏁 **Classic Mode**
- **Endless Gameplay**: Chơi cho đến khi không thể đặt piece
- **Score Tracking**: Theo dõi điểm số và high score
- **Progressive Difficulty**: Độ khó tăng dần theo thời gian

### 🎯 **Strategic Elements**
- **Durable Pieces Management**: Lập kế hoạch nhiều lượt để clear
- **Cross Clear Planning**: Tạo chiến thuật để nhận bonus
- **Resource Management**: Sử dụng hold và swap một cách thông minh

## 🔮 **Roadmap & Future Features**

### 🚧 **Planned Updates**
- **Multiple Game Modes**: Time attack, puzzle mode, challenge mode
- **Power-ups System**: Special abilities và temporary bonuses
- **Achievement System**: Unlockable rewards và milestones
- **Multiplayer Support**: Competitive và cooperative modes

### 💡 **Community Suggestions**
- **Custom Themes**: Player-created visual themes
- **Level Editor**: Create và share custom levels
- **Statistics Dashboard**: Detailed performance analytics
- **Social Features**: Leaderboards và friend challenges

## 🤝 **Contributing**

### 🐛 **Bug Reports**
- **GitHub Issues**: Report bugs và suggest improvements
- **Detailed Descriptions**: Include steps to reproduce
- **System Information**: Browser, OS, và device details

### 💻 **Code Contributions**
- **Fork & Pull Request**: Standard GitHub workflow
- **Code Style**: Follow existing conventions
- **Testing**: Ensure changes work across browsers

### 📚 **Documentation**
- **README Updates**: Improve clarity và completeness
- **Code Comments**: Add helpful explanations
- **User Guides**: Create tutorials và tips

## 📄 **License**

**MIT License** - Xem file `LICENSE` để biết chi tiết.

## 🙏 **Acknowledgments**

- **Inspiration**: Classic Tetris và modern puzzle games
- **Community**: Feedback và suggestions từ players
- **Open Source**: Libraries và tools sử dụng trong development

---

**🎮 Chơi ngay tại: `index.html`**

**📧 Contact**: GitHub Issues hoặc Discussions

**⭐ Star**: Nếu bạn thích game này!

---

*Last Updated: December 19, 2024 | Version: v1.5.0*
