# BB+ Prototype - Block Tetrist Game

## Mô tả
Game puzzle prototype sử dụng HTML5 Canvas với bàn chơi 8×8, các khối Tetris-like và hệ thống scoring nâng cao.

## Tính năng chính
- **Bàn chơi 8×8** với giao diện hiện đại
- **12 loại khối** khác nhau (1x1, 1x2, L3, T4, O3, v.v.)
- **Hệ thống Hold** - lưu khối với cooldown 3 lượt
- **Hệ thống Swap** - đổi khối sang khối cứu nạn với cooldown 9 lượt
- **Combo system** - tăng multiplier khi clear liên tiếp
- **Precision bonus** - nhân điểm khi clear ≥2 line
- **Guardrail system** - tự động sửa khi bị kẹt

## Điều khiển
- **Click chuột trái**: Chọn khối từ pool hoặc đặt lên bàn
- **Click chuột phải**: Bỏ chọn khối
- **Phím H**: Hold khối đang chọn
- **Phím 1/2/3**: Swap khối ở slot tương ứng
- **Click vùng Hold**: Thả khối hold về pool

## Cách chạy với Go Live
1. Mở project trong Cursor
2. Click chuột phải vào file `index.html`
3. Chọn "Go Live" hoặc sử dụng extension Live Server
4. Game sẽ mở trong trình duyệt với URL local

## Cấu trúc project
```
Block Tetrist/
├── index.html          # File game chính
├── README.md           # Hướng dẫn này
└── .gitignore          # Git ignore rules
```

## Phiên bản
- **v1.4.2**: Cải tiến Combo Text - font lớn x5, fade out mượt mà, hiển thị 2 giây
- **v1.4.1**: Combo Text System - hiển thị text động khi clear hàng liên tiếp (Good → Exceptional)
- **v1.4.0**: Hệ thống xoay piece đa dạng - từ 12 pieces lên 32 pieces với 4 hướng xoay
- **v1.3.1**: Cải thiện trải nghiệm - hiển thị piece cuối cùng trước khi thông báo thua
- **v1.3.0**: Thêm hệ thống Game Over - điều kiện thua, thông báo và nút chơi lại
- **v1.2.1**: Sửa lỗi ô bị khóa không clear, cập nhật FR tính ô bị khóa, tự động refill khi Hold
- **v1.2.0**: Thêm tính năng ô bị khóa (Blocked Cells) - 6-12 ô màu đỏ ngẫu nhiên, tăng độ khó game
- **v1.1.2**: Sửa lỗi khởi động - game không tạo piece, đảm bảo luôn có 3 pieces khi bắt đầu
- **v1.1.1**: Sửa hoàn toàn logic dồn piece - vị trí piece không thay đổi khi sử dụng
- **v1.1.0**: Thêm màu sắc riêng biệt cho từng piece, vị trí piece không thay đổi
- **v1.0.4**: Sửa lỗi JavaScript hoàn toàn - Lần cuối, đảm bảo 3 slots và Hold hiển thị đúng
- **v1.0.3**: Sửa lỗi JavaScript hoàn toàn, đảm bảo game hoạt động ổn định
- **v1.0.2**: Sửa lỗi Assignment to constant variable
- **v1.0.1**: Tối ưu hóa logic game, đảm bảo hoạt động chính xác
- **v1.0.0**: Prototype cơ bản với đầy đủ tính năng
- Hỗ trợ Go Live để development và testing

## Tính năng kỹ thuật
- **Canvas rendering** với performance tối ưu
- **Responsive design** cho nhiều kích thước màn hình
- **Modular code structure** dễ maintain và extend
- **No external dependencies** - chạy trực tiếp trên browser

## Development
Game được viết bằng vanilla JavaScript, không cần build tools. Có thể dễ dàng chỉnh sửa:
- Thay đổi scoring system
- Thêm khối mới
- Điều chỉnh difficulty
- Customize giao diện

## Tác giả
BB+ Prototype - Block Tetrist Game
