# Block Tetrist - Changelog

## [v1.9.15] - 2024-12-19
### 🔧 Technical Improvements
- **Enhanced Piece Format**: Changed from space-based to "o"-based empty cell representation
- **Improved Readability**: Updated piece definitions to use "o" for empty cells (0) and "x" for filled cells (1)
- **Multi-line Format**: Converted all piece definitions to multi-line format for better visual clarity
- **Consistent Notation**: All pieces now use consistent "o" and "x" notation throughout

### 📝 Code Quality
- **Better Visual Representation**: "o" clearly represents empty cells, making piece shapes easier to understand
- **Enhanced Maintainability**: Multi-line format makes it easier to see piece patterns and modify them
- **Improved Documentation**: Added clear comments explaining the "o" and "x" format
- **Cleaner Code**: Eliminated confusion between spaces and actual empty cells

### 🎯 Examples of New Format
- **Before**: `"L3": decodePiece("x ", "xx")`
- **After**: `"L3": decodePiece("xo", "xx")`
- **Before**: `"R2x2R": decodePiece("xx", "xx", " x")`
- **After**: `"R2x2R": decodePiece("xx", "xx", "ox")`

### 📊 Format Standards
- **"x"**: Represents filled cells (value 1)
- **"o"**: Represents empty cells (value 0)
- **Multi-line**: Each piece definition spans multiple lines for clarity
- **Consistent**: All 65 pieces follow the same format pattern

---

## [v1.9.14] - 2024-12-19

## [v1.8.4] - 2024-12-19
### 🐛 Bug Fixes
- **Fixed Duplicate Piece Names**: Resolved naming conflicts that caused pieces to overwrite each other
- **Corrected Piece Count**: Updated from incorrect "44 pieces" to accurate "71 pieces" total
- **Fixed Cross Shape Rotations**: Cross shape now has 4 distinct rotation variants instead of identical copies
- **Resolved Naming Conflicts**: 
  - T3 → T6 (6-cell T-shape)
  - R2x2 → R2x2R (2x2 + right extension)
  - T4 duplicate → T4B (4-cell T-shape variant)

### 🔧 Technical Improvements
- **Unique Piece Identifiers**: All pieces now have distinct names to prevent overwriting
- **Accurate Documentation**: Updated comments and debug info to reflect correct piece count
- **Proper Rotation Variants**: Fixed Cross shape to have meaningful rotation differences

### 📝 Documentation
- **Updated Version Number**: From v1.8.3 to v1.8.4
- **Corrected Piece Count**: Debug info now shows accurate "Total Pieces: 71"
- **Enhanced Comments**: Updated PIECES object comment to reflect actual piece count

## [v1.8.1] - 2024-12-19
### 🐛 Bug Fixes
- **Fixed Bomb in Basic Mode**: Bomb pieces no longer appear or function in Basic Mode
- **Mode-Specific Logic**: All bomb-related functions now properly check game mode before execution
- **Fill Rate Calculation**: Fixed getFillRate() to only count bomb pieces in Blast Mode
- **Line Clear Logic**: Fixed clearLines() to only process bomb pieces in Blast Mode
- **Rendering**: Fixed drawBoard() to only display bomb pieces in Blast Mode

### 🔧 Technical Improvements
- **Conditional Execution**: Added game mode checks for all bomb-related functions
- **Performance**: Reduced unnecessary bomb processing in non-Blast modes
- **Code Consistency**: Ensured all game features respect mode restrictions

## [v1.8.0] - 2024-12-19
### ✨ New Features
- **Bomb System**: Added explosive bomb pieces that create 3x3 explosion areas
- **Strategic Bomb Placement**: Bombs spawn when Fill Rate exceeds 60% (once per game)
- **3x3 Explosion Mechanics**: Bomb explosion clears pieces in 3x3 area with bomb at center
- **Bomb-Bonus Interaction**: Bombs can activate bonus pieces in explosion area for extra points
- **Lifetime Management**: Bombs automatically disappear after 1-2 turns if not activated

### 🎯 Gameplay Mechanics
- **Fill Rate Trigger**: Bombs only spawn when board is more than 60% filled
- **One Bomb Per Game**: Maximum 1 bomb can exist per game session
- **Explosion Scoring**: Bombs award points for each piece cleared in explosion area
- **Bonus Activation**: Bonus pieces in explosion area are activated and award multiplier points
- **Strategic Depth**: Players must decide when to trigger bombs for maximum effect

### 🎨 Visual Enhancements
- **Bomb Piece Design**: Red-colored pieces with white borders and lifetime indicators
- **Explosion Animation**: "BOOM!" text animation when bombs explode
- **Lifetime Display**: Shows remaining turns before bomb disappears
- **Visual Distinction**: Bombs are clearly different from bonus pieces

### 🔧 Technical Improvements
- **Bomb State Management**: Added bombPieces array and bombSpawned flag
- **Explosion Algorithm**: 3x3 area calculation with board boundary handling
- **Lifetime System**: Automatic lifetime decrease and cleanup
- **Integration**: Seamless integration with existing bonus and durable piece systems

### 📝 Documentation
- **Updated Version Number**: From v1.6.2 to v1.7.0
- **Enhanced Debug Info**: Added bomb count to debug panel
- **Comprehensive Logging**: Added console logs for bomb system behavior tracking

---

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
