# Block Tetrist - Changelog

## v1.9.18-mode-drag-fix (Latest)
**Game Mode Selection & Drag & Drop Fixes**

### 🎮 Game Mode System Fixes
- **Fixed mode selector display**: Mode selector now shows correctly when game starts
- **Added startup mode selection**: Players can now choose game mode before starting
- **Improved mode switching**: Better handling of mode changes and game resets
- **Enhanced user guidance**: Added helpful messages when mode selector is displayed

### 🖱️ Drag & Drop Improvements
- **Fixed drag & drop conflicts**: Resolved issues between drag & drop and click-to-place systems
- **Enhanced visual feedback**: Added cursor changes and hover effects during drag operations
- **Improved error handling**: Better handling of failed drops and edge cases
- **Unified interaction**: Consistent drag & drop behavior across desktop and mobile

### 🐛 Bug Fixes
- **Fixed piece selection conflicts**: Clear selection when starting drag operations
- **Fixed drop validation**: Improved piece placement validation and error recovery
- **Fixed mobile touch handling**: Better touch event integration with drag & drop
- **Fixed visual glitches**: Resolved cursor and visual feedback issues

### ✨ User Experience Enhancements
- **Better instructions**: Added drag & drop guidance in game legend
- **Visual cues**: Enhanced hover effects and cursor feedback
- **Responsive design**: Improved mobile drag & drop experience
- **Error prevention**: Better handling of invalid drop operations

---

## v1.9.17-mobile-fix
**Mobile Layout & Functionality Fixes**

### 🎯 Layout & Size Improvements
- **Increased canvas size on mobile**: Changed from `max-height: 60vh` to `max-height: 80vh` for better mobile experience
- **Mobile-specific canvas sizing**: Added `max-height: 90vh` and `width: 95vw` in mobile media queries
- **Larger game board cells**: Increased `CELL` size from 60px to 80px on mobile devices
- **Better positioning**: Adjusted `BOARD_Y` from 40 to 60 and `POOL_Y` from 620 to 580 on mobile for optimal spacing

### 🐛 Bug Fixes
- **Fixed drag & drop functionality**: Corrected `startDrag()` function to not remove pieces from pool immediately
- **Fixed piece placement**: Streamlined `endDrag()` function to use `placePieceOnBoard()` helper
- **Fixed touch event handling**: Resolved conflicts between canvas event listeners and touch events
- **Fixed syntax errors**: Corrected indentation and structure issues in drag & drop functions

### 📱 Mobile Experience
- **Larger touch targets**: Game board now occupies at least 50% of mobile screen height
- **Better visual feedback**: Improved drag preview and piece rendering during touch operations
- **Responsive layout**: Canvas automatically adjusts to mobile viewport dimensions

### 🔧 Technical Improvements
- **Cleaner code structure**: Simplified drag & drop logic for better maintainability
- **Mobile detection**: Enhanced mobile-specific constants and positioning
- **Event handling**: Improved touch event integration with existing game logic

---

## v1.9.16-mobile
**Major Mobile Optimization Release**

### 🎮 Complete Mobile Adaptation
- **Responsive Layout**: Redesigned for 9:16 vertical mobile screens
- **Touch Controls**: Replaced keyboard shortcuts with on-screen buttons
- **Drag & Drop**: New piece placement system (hold piece, drag to board, release to place)
- **Single Screen Experience**: All layout information fits without scrolling

### 📱 Mobile-Specific Features
- **Mobile Control Buttons**: Dedicated Hold, Swap 1, Swap 2, Swap 3 buttons
- **Touch Event Handling**: Full support for `touchstart`, `touchmove`, `touchend`
- **Responsive Design**: CSS media queries for mobile optimization
- **Touch-Friendly UI**: Larger buttons, better spacing, mobile-optimized fonts

### 🎯 Input System Overhaul
- **Desktop vs Mobile**: Different interaction modes (click-to-place vs drag-and-drop)
- **Event Listeners**: Refactored to support both mouse and touch input
- **Piece Management**: Enhanced drag preview and visual feedback
- **Control Instructions**: Context-sensitive help text for different devices

### 🔧 Code Improvements
- **Helper Functions**: New `placePieceOnBoard()` function for common logic
- **Mobile Detection**: `navigator.userAgent` based mobile detection
- **State Management**: Added drag & drop variables and state tracking
- **Performance**: Optimized rendering with drag previews

---

## v1.9.15
**Game Mode System & Advanced Features**

### 🎮 New Game Modes
- **Basic Mode**: Standard chain multiplier gameplay
- **Blocker Mode**: Durable pieces with precision bonuses
- **Multiplier Mode**: Bonus point system with multipliers
- **Blast Mode**: Bomb explosion mechanics

### ⭐ Advanced Gameplay Features
- **Durable Pieces**: Red pieces requiring multiple hits to clear
- **Bonus Pieces**: Multiplier pieces (x2-x7) with lifetime system
- **Bomb Pieces**: Explosive pieces that clear 3x3 areas
- **Precision Bonuses**: Extra points for clearing multiple lines

### 🏆 Enhanced Scoring System
- **Mode-Specific High Scores**: Separate tracking for each game mode
- **Combo System**: Progressive multiplier increases
- **Bonus Multipliers**: Stacking bonus point calculations
- **Cross Bonuses**: Special rewards for clearing rows and columns simultaneously

### 🔧 Technical Improvements
- **Local Storage**: Persistent high scores across sessions
- **Game State Management**: Enhanced state tracking and persistence
- **Piece Generation**: Improved piece spawning algorithms
- **Performance Optimization**: Better rendering and update cycles

---

## v1.9.14
**Core Gameplay & UI Enhancements**

### 🎯 Game Mechanics
- **8x8 Game Board**: Optimized board size for strategic gameplay
- **Piece Pool System**: 3-piece pool with smart refilling
- **Line Clearing**: Row and column clearing mechanics
- **Scoring System**: Base scoring with combo multipliers

### 🎨 User Interface
- **Modern Design**: Gradient backgrounds and smooth animations
- **Responsive Layout**: Flexible design for different screen sizes
- **Visual Feedback**: Hover effects and transition animations
- **Game Statistics**: Real-time score, turn, and combo display

### 🔧 Core Systems
- **Piece Management**: 65 unique piece types with rotations
- **Grid System**: Efficient board state management
- **Event Handling**: Mouse and keyboard input support
- **Rendering Engine**: HTML5 Canvas-based graphics

---

## v1.9.13
**Initial Release & Foundation**

### 🚀 Project Setup
- **HTML5 Canvas**: Core rendering technology
- **JavaScript Game Logic**: Complete game state management
- **CSS Styling**: Modern, responsive design system
- **Basic Gameplay**: Core tetris-like mechanics

### 📁 Project Structure
- **Single File Architecture**: All code in `index.html`
- **Modular Functions**: Organized, maintainable code structure
- **Documentation**: Comprehensive README and changelog
- **Version Control**: Incremental version tracking system
