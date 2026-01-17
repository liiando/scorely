# Scorely

A powerful and versatile score tracking application designed for streamers, content creators, and gaming events. Scorely provides real-time score display with extensive customization options, perfect for OBS, TikTok, and other streaming platforms.

## Features

### 🎮 Multi-Player Score Tracking
- **4 Independent Score Boards**: Track scores for up to 4 players or teams simultaneously
- **Real-time Updates**: Scores update instantly across all connected displays
- **Easy Controls**: Simple + and - buttons for quick score adjustments
- **Score Goals**: Set target scores with progress tracking

### 🎨 Advanced Customization
Each score board can be fully customized:

**Typography**
- 60+ Google Fonts (Sans-Serif, Display, Serif, Monospace, Handwriting)
- Windows system fonts (Arial, Segoe UI, Times New Roman, etc.)
- Adjustable title and score sizes (12px to 120px)
- Custom text colors

**Layout & Design**
- Background color with enable/disable toggle
- Customizable borders (color, thickness, rounded corners)
- Title positioning (Top, Bottom, Left, Right)
- Multiple display formats:
  - Simple: "10"
  - With Goal: "10 / 50"
  - Progress: "10 sur 50"

**Element Visibility**
- Toggle visibility for title, score, goal, and separator
- Show/hide background and borders independently

### 📊 Profile Management
- **20 Profile Slots**: Create and manage up to 20 different game configurations
- **Quick Switching**: Instantly switch between profiles
- **Profile Actions**: Create, rename, duplicate, and delete profiles
- **Auto-Save**: All changes are automatically saved

### 🔌 Webhook API Integration
Control scores programmatically with simple HTTP requests:

**Simple URL Format**
```
GET  http://127.0.0.1:8080/score1/+200    # Add 200 points
GET  http://127.0.0.1:8080/score1/-150    # Subtract 150 points
GET  http://127.0.0.1:8080/score1/reset   # Reset to 0
GET  http://127.0.0.1:8080/score1/x2/5m   # 2x multiplier for 5 minutes
```

**RESTful JSON API**
```
POST   /api/score      {"player": 1, "value": 200}
PUT    /api/score      {"player": 1, "value": 500}
PATCH  /api/score      {"player": 1, "action": "add", "value": 100}
DELETE /api/score      {"player": 1}
POST   /api/multiplier {"player": 1, "multiplier": 2, "duration": 5}
GET    /api/status     # Get all scores and multipliers
```

### 🖥️ OBS & Streaming Integration
- **Transparent Background**: Perfect for OBS overlays
- **4 Dedicated Display Pages**: Separate pages for each score board
- **Real-time WebSocket Updates**: Instant synchronization
- **Multiplier Display**: Animated blinking effect for active multipliers
- **Browser Source Compatible**: Works with OBS, TikTok, and other platforms

### 🌍 Multi-Language Support
Available in 26 languages including:
- English, French, Spanish, German, Italian
- Portuguese, Dutch, Polish, Russian, Chinese
- Japanese, Korean, Arabic, and many more

### 🎯 Score Multipliers
- **Temporary Boosts**: Activate multipliers (x2, x3, x5, etc.) for limited time
- **Visual Feedback**: Animated display shows active multiplier
- **Time Tracking**: Shows remaining time for each multiplier
- **Customizable**: Adjust display interval (500ms to 10s)

### ⚙️ Settings & Preferences
- **Theme Options**: Light, Dark, or System theme
- **Auto-Save**: Automatic profile saving
- **Notifications**: Enable/disable system notifications
- **Auto-Update**: Built-in update system for seamless upgrades

### 🔄 Auto-Update System
- **Automatic Checks**: Checks for updates on startup
- **One-Click Updates**: Download and install updates automatically
- **Version Tracking**: Always know your current version
- **Seamless Restart**: Application restarts after update

## Getting Started

1. **Launch Scorely**: Run the application
2. **Customize Your Scores**: Visit the Settings page to configure each score board
3. **Add to OBS**: Use browser source with URL `http://127.0.0.1:2627/score1`
4. **Control Scores**: Use the main interface or webhook API to update scores

## Server Ports

- **HTTP Server**: Port 2627 (Display pages for OBS/TikTok)
- **Webhook API**: Port 8080 (Score control API)

## Display URLs

- Home: `http://127.0.0.1:2627/`
- Score 1: `http://127.0.0.1:2627/score1`
- Score 2: `http://127.0.0.1:2627/score2`
- Score 3: `http://127.0.0.1:2627/score3`
- Score 4: `http://127.0.0.1:2627/score4`

## Use Cases

- **Gaming Tournaments**: Track scores for competitive matches
- **Quiz Shows**: Display team scores in real-time
- **Charity Streams**: Track donation goals and progress
- **Fitness Challenges**: Monitor workout scores and achievements
- **Educational Games**: Classroom score tracking
- **Live Events**: Real-time score displays for any competition

## Version

Current Version: 1.0.0

---

**Scorely** - Professional score tracking for streamers and content creators.