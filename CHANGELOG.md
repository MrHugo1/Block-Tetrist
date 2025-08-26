# Block Tetrist - Changelog

## [v1.6.2] - 2024-12-19
### 🐛 Bug Fixes
- **Fixed Bonus System Spawn Logic**: Bonus pieces now spawn on existing pieces instead of empty cells
- **Fixed Bonus Piece Removal Timing**: Bonus pieces are now spawned before removing cleared ones
- **Fixed Line Clear Logic**: Bonus pieces are now properly counted as part of lines for clearing
- **Restored 30% Spawn Chance**: Changed from 100% test spawn back to intended 30% chance
- **Added Comprehensive Debug Logging**: Added console.log statements to track bonus system behavior

### 🔧 Technical Improvements
- **Improved Bonus Spawn Algorithm**: Now correctly finds positions on existing pieces for bonus placement
- **Enhanced Debug Information**: Added detailed logging for bonus piece creation, removal, and rendering
- **Fixed Lifetime Management**: Bonus pieces now properly decrease lifetime and get removed when expired

### 📝 Documentation
- **Updated Version Number**: From v1.6.1 to v1.6.2
- **Enhanced Test Suite**: Created comprehensive test file (test.html) for bonus system validation

---

## [v1.6.1] - 2024-12-19
### 🐛 Bug Fixes
- **Fixed Bonus System Spawn Logic**: Corrected logic to spawn bonus pieces on empty cells after line clear
- **Added Debug Logging**: Added console.log statements to troubleshoot bonus spawning issues
- **Temporary 100% Spawn Rate**: Set spawn chance to 100% for testing purposes

---

## [v1.6.0] - 2024-12-19
### ✨ New Features
- **Bonus Points System**: Added bonus pieces with multipliers (x2, x3, x4, x5, x6, x7)
- **Dynamic Spawn System**: 30% chance to spawn 2-3 bonus pieces after line clear
- **Lifetime Management**: Bonus pieces automatically disappear after 2-4 turns based on multiplier
- **Multiplier Stacking**: Multiple bonus pieces in same line multiply together (x2 × x5 = x10)
- **Visual Feedback**: Bonus score text displays "+X points" for 2 seconds after clearing

### 🎨 Visual Enhancements
- **Color-Coded Bonus Pieces**: Green (x2-3), Yellow (x4-5), Red (x6-7)
- **Multiplier Display**: Shows "x2", "x3", etc. on bonus pieces
- **Lifetime Counter**: Displays remaining turns on each bonus piece
- **Bonus Score Animation**: Floating text shows bonus points earned

### 🎯 Gameplay Mechanics
- **Strategic Placement**: Bonus pieces appear on existing pieces, not empty cells
- **Maximum Limit**: Maximum 4 bonus pieces on board at any time
- **Scoring Integration**: Bonus multipliers apply to all points in cleared lines
- **Auto-Cleanup**: Expired bonus pieces automatically removed from board

---

## [v1.5.0] - 2024-12-19
### ✨ New Features
- **Durable Pieces System**: Added pieces with durability that require multiple clears
- **Cross Clear Bonus**: Special bonus for clearing both rows and columns simultaneously
- **Enhanced Combo System**: Added combo streak counter with escalating text feedback
- **Game Over Detection**: Improved game over logic with victory condition

### 🎨 Visual Enhancements
- **Durability Display**: Shows remaining durability on durable pieces
- **Combo Text Animation**: "Good", "Nice", "Great", "Amazing", etc. with animations
- **Cross Clear Feedback**: Special text for cross clear achievements
- **High Score Indicator**: Visual indicator when achieving new high score

### 🎯 Gameplay Mechanics
- **Durability System**: Pieces with 2-5 durability require multiple line clears
- **Cross Clear Mechanics**: Simultaneous row/column clear provides durability reduction bonus
- **Combo Streak**: Consecutive line clears build combo multiplier
- **Strategic Depth**: Players must manage durable pieces strategically

---

## [v1.4.0] - 2024-12-19
### ✨ New Features
- **32 Piece Types**: Added all rotations for L3, L4, T4 pieces
- **Enhanced Pool System**: Improved pool refill logic with rescue pieces
- **Hold System**: Added ability to hold one piece (3-turn cooldown)
- **Swap System**: Emergency piece swapping with 9-turn cooldown

### 🎯 Gameplay Mechanics
- **Piece Rotation**: Full 4-direction rotation support for L and T pieces
- **Strategic Depth**: Hold and swap mechanics add tactical options
- **Rescue System**: Automatic rescue pieces when pool becomes unplayable
- **Cooldown Management**: Strategic timing of hold and swap abilities

---

## [v1.3.0] - 2024-12-19
### ✨ New Features
- **Enhanced Scoring**: Added precision bonuses for clearing multiple lines
- **Combo System**: Chain multiplier increases with consecutive line clears
- **Fill Rate Management**: Strategic depth through fill rate optimization
- **High Score Persistence**: Local storage for high score tracking

### 🎯 Gameplay Mechanics
- **Precision Bonuses**: 1.2× for 2 lines, 1.5× for 3+ lines
- **Chain Multipliers**: Up to 1.5× multiplier for consecutive clears
- **Strategic Placement**: Balance between immediate points and board management

---

## [v1.2.0] - 2024-12-19
### ✨ New Features
- **Piece Pool System**: 3-piece pool for strategic piece selection
- **Enhanced UI**: Improved visual design with gradients and animations
- **Responsive Design**: Mobile-friendly interface adaptations
- **Game Statistics**: Real-time display of score, turns, and fill rate

### 🎨 Visual Enhancements
- **Modern UI Design**: Gradient backgrounds and smooth transitions
- **Piece Visualization**: Clear piece representation with colors
- **Interactive Elements**: Hover effects and visual feedback
- **Mobile Optimization**: Responsive layout for various screen sizes

---

## [v1.1.0] - 2024-12-19
### ✨ New Features
- **Basic Game Mechanics**: Core piece placement and line clearing
- **8×8 Board**: Compact playing field for strategic gameplay
- **Multiple Piece Types**: Various piece shapes and sizes
- **Basic Scoring**: Points for piece placement and line clearing

### 🎯 Core Gameplay
- **Piece Placement**: Click to place selected pieces on board
- **Line Clearing**: Complete rows/columns to clear them
- **Score Accumulation**: Earn points through strategic play
- **Game Over Detection**: End game when no more moves possible

---

## [v1.0.0] - 2024-12-19
### 🎉 Initial Release
- **Block Tetrist**: Strategic puzzle game with 8×8 board
- **Core Mechanics**: Place pieces to create complete lines
- **Basic UI**: Functional game interface with canvas rendering
- **Foundation**: Established codebase for future enhancements
