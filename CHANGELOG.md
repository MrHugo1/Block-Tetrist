# Changelog

## [v1.5.0] - 2024-12-19

### ✨ New Features
- **Durable Pieces System**: Replaced blocked cells with pieces that have durability (2-5 hits)
- **Cross Clear Bonus**: Special durability reduction when clearing both rows and columns simultaneously
  - 1x1 cross: -3 durability
  - 2x1 or 1x2 cross: -4 durability  
  - 2x2 cross: -6 durability
  - 2x3 or 3x2+ cross: Clear ALL durable pieces on board
- **Enhanced Visual Feedback**: Durable pieces show durability numbers with color intensity

### 🛠️ Bug Fixes
- **Cross Clear Logic**: Fixed double-counting of cross bonus on durable pieces
- **Game Over Logic**: Fixed premature game over when lines could be cleared
- **Line Clearing Order**: Ensure lines are cleared BEFORE checking game over conditions
- **Pool Refill**: Fixed pool not refilling after implementing durable pieces system

### 🎮 Gameplay Improvements
- **Strategic Depth**: Players must plan multiple hits on durable pieces
- **Cross Clear Strategy**: Encourages creating simultaneous row/column clears
- **Visual Clarity**: Durability numbers make piece strength immediately apparent

### 🔧 Technical Improvements
- **State Management**: Refactored from `blockedCells` to `durablePieces` system
- **Performance**: Optimized cross clear detection and durability calculations
- **Code Quality**: Improved logic flow for line clearing and game over detection

---

## [v1.4.3] - 2024-12-19

### ✨ New Features
- **Consecutive Combo System**: Changed from lines cleared per turn to consecutive streak tracking
- **Enhanced Combo Text**: 10-level combo system with escalating feedback
  - 1st: "Good", 2nd: "Nice!", 3rd: "Great!", 4th: "Amazing!", 5th: "Fantastic!"
  - 6th: "Incredible!", 7th: "Unbelievable!", 8th: "Legendary!", 9th: "Godlike!", 10th+: "Ultimate!"

### 🛠️ Bug Fixes
- **Combo Reset**: Streak resets to 0 when no lines are cleared
- **Game Over Logic**: Refined conditions for detecting unplaceable pieces vs. empty pool

---

## [v1.4.2] - 2024-12-19

### ✨ New Features
- **Enhanced Combo Text System**: Dynamic text feedback for clearing multiple lines
- **Animated Combo Display**: Fade-out animation for combo text with scaling effects
- **Improved Game Over UI**: Replaced full-screen overlay with subtle on-board notification

### 🛠️ Bug Fixes
- **Game Over Detection**: Fixed logic to properly distinguish between empty pool and unplaceable pieces
- **Auto-refill System**: Re-enabled automatic pool refilling when empty
- **UI Responsiveness**: Improved game over button placement and styling

---

## [v1.4.1] - 2024-12-19

### ✨ New Features
- **Game Over Refinement**: Added "Chơi Lại" (Play Again) button below game information
- **Improved Game Over Logic**: Better detection of when game should end vs. continue

### 🛠️ Bug Fixes
- **Game Over Conditions**: Fixed premature game over when board still has empty cells
- **Pool Management**: Improved handling of empty pool scenarios

---

## [v1.4.0] - 2024-12-19

### ✨ New Features
- **32 Unique Pieces**: Expanded from 12 base pieces to 32 with various rotation states
- **Enhanced Rotation System**: 4-direction rotation for L3, L4, T4 pieces
- **Improved Piece Variety**: Added rotated versions of existing pieces for more strategic options

### 🎮 Gameplay Improvements
- **Strategic Depth**: More piece options increase planning complexity
- **Visual Variety**: Different rotation states provide visual distinction

---

## [v1.3.0] - 2024-12-19

### ✨ New Features
- **Hold System**: Save selected piece for later use (3-turn cooldown)
- **Swap System**: Emergency piece replacement with rescue pieces (9-turn cooldown)
- **Rescue Piece Set**: Special pieces available for swap when pool becomes unplayable

### 🎮 Gameplay Improvements
- **Strategic Planning**: Hold system allows better piece management
- **Emergency Recovery**: Swap system prevents impossible game states
- **Cooldown Management**: Strategic timing of hold and swap abilities

---

## [v1.2.0] - 2024-12-19

### ✨ New Features
- **Blocked Cells System**: Randomly generated obstacles that cannot be placed upon
- **Strategic Obstacles**: Blocked cells add complexity and require planning to clear
- **Fill Rate Management**: Intelligent piece generation based on board state

### 🎮 Gameplay Improvements
- **Strategic Depth**: Players must work around obstacles
- **Risk Management**: Balancing piece placement with obstacle clearing

---

## [v1.1.0] - 2024-12-19

### ✨ New Features
- **Pool System**: 3-piece selection pool for upcoming moves
- **Basic Scoring**: Points for placed pieces and cleared lines
- **Combo System**: Multiplier system for consecutive successful moves
- **Fill Rate Display**: Visual indicator of board completion percentage

### 🎮 Gameplay Improvements
- **Strategic Planning**: Players can see upcoming pieces
- **Score Tracking**: Clear feedback on performance
- **Visual Feedback**: Immediate response to player actions

---

## [v1.0.0] - 2024-12-19

### ✨ Initial Release
- **8×8 Game Board**: Classic grid-based puzzle gameplay
- **Basic Piece Placement**: Click-based piece placement system
- **Line Clearing**: Complete rows and columns to clear them
- **Responsive Design**: Modern UI with smooth animations
- **Local Storage**: High score persistence
