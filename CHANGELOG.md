# Block Tetrist Changelog

## [v1.9.16-mobile] - 2024-12-19
### 🚀 Mobile Optimization
- **Complete mobile layout redesign** for 9:16 portrait screens
- **Touch controls** replacing keyboard controls on mobile devices
- **Drag & Drop system** for piece placement with visual preview
- **Mobile control buttons** for Hold and Swap operations
- **Responsive design** with all content fitting in single mobile screen
- **Touch event handling** with proper mobile gesture support
- **Optimized font sizes and spacing** for mobile readability
- **Prevented scrolling** to maintain single-screen experience

### 🎮 New Controls
- **Touch & Drag**: Select piece → drag to board → release to place
- **Hold Button**: Touch-friendly hold operation with cooldown display
- **Swap Buttons**: Touch-friendly swap operations for slots 1, 2, 3
- **Visual feedback**: Drop preview and drag indicators

### 📱 Mobile Features
- **Auto-detection** of mobile devices
- **Adaptive UI** that switches between desktop and mobile controls
- **Touch-optimized** button sizes and spacing
- **Gesture support** for natural mobile interaction

## [v1.9.15] - 2024-12-19
### 🎯 Game Modes
- **4 Game Modes**: Basic, Blocker, Multiplier, Blast
- **Mode-specific mechanics** and scoring systems
- **High Score tracking** for each mode separately

### 🧩 Piece System
- **65 unique pieces** with 4 rotation directions
- **Smart piece generation** with bias system
- **Rescue pieces** for deadlock situations

### 🎨 Visual Enhancements
- **Modern gradient design** with smooth animations
- **Combo text animations** with streak-based messages
- **Bonus piece system** with multiplier effects
- **Durable pieces** with health system (Blocker Mode)
- **Bomb pieces** with explosion mechanics (Blast Mode)

### 🏆 Scoring System
- **Multi-layered scoring**: Cell, Line, Precision, Combo
- **Chain multiplier** system with visual feedback
- **Cross-clear bonuses** for simultaneous row/column clears
- **Bonus piece multipliers** (x2 to x7) with lifetime system

### ⚙️ Game Mechanics
- **Hold system** with 3-turn cooldown
- **Swap system** with 9-turn cooldown and rescue pieces
- **Fill Rate management** with smart bias adjustments
- **Deadlock prevention** with guardrail system

### 🔧 Technical Features
- **Responsive design** for different screen sizes
- **Local storage** for high score persistence
- **Debug information** display
- **Performance optimizations** for smooth gameplay

## [v1.9.0] - 2024-12-19
### 🎮 Initial Release
- **8×8 game board** with smart piece placement
- **Basic scoring system** with line clearing mechanics
- **Piece rotation system** with multiple orientations
- **Core game loop** with pool management
- **Basic UI** with score and turn display
