# 🎯 Skaalat - The Guessing Game

A mobile-friendly web game where intuition meets numbers! One player becomes the guesser while others help them find the secret target number through clever questioning.

## 🎮 How to Play

### Game Setup
1. Choose a scale (1-10 or 1-20)
2. Press "Start Game" to generate a random target number
3. Show the target number to all players EXCEPT the guesser
4. Hand the device to the guesser

### Gameplay
- The guesser sees a grid of numbers from the chosen scale
- Ask other players to rate something on that scale
- Example: "Rate the smell of this room from 1-10"
- Based on their answers, select the number you think matches the secret target
- You can change your guess as many times as you want
- Press "Lock In Guess" when you're ready to finalize

### Scoring
- **Accuracy**: How close your final guess is to the target
- **Time**: Faster completion gives bonus points
- **Efficiency**: Fewer guess changes = higher score

## ✨ Features

- **Mobile-Responsive Design**: Works perfectly on phones and tablets
- **Two Scale Options**: 1-10 for beginners, 1-20 for experts
- **Real-time Statistics**: Track accuracy, time, and score
- **Beautiful UI**: Modern gradient design with smooth animations
- **Progress Tracking**: Saves your game statistics locally
- **No Internet Required**: Works offline once loaded

## 🎨 Technical Details

- **Framework**: Vanilla HTML, CSS, and JavaScript
- **Design**: Modern glassmorphism with gradient backgrounds
- **Responsive**: Adapts to any screen size
- **Performance**: Lightweight and fast loading
- **Storage**: Uses localStorage for progress persistence

## 🚀 Getting Started

1. Open `index.html` in any modern web browser
2. No installation or setup required
3. Works on desktop, mobile, and tablet devices

## 🎯 Game Mechanics

### Accuracy Calculation
- Perfect guess = 100% accuracy
- Each number off = proportional accuracy loss
- Based on the maximum possible difference in the scale

### Score Formula
- Base score = Accuracy × 10
- Time bonus = 100 - seconds taken
- Change penalty = Number of guess changes × 5
- Final score = Base + Time bonus - Change penalty

## 📱 Mobile Optimization

- Touch-friendly buttons and interface
- Responsive grid layout that adapts to screen size
- Optimized for portrait and landscape orientations
- Prevents zoom on input fields (iOS compatibility)

## 🎨 Design Features

- **Glassmorphism**: Translucent backgrounds with blur effects
- **Gradient Animations**: Smooth color transitions
- **Hover Effects**: Interactive button animations
- **Fade Transitions**: Smooth screen transitions
- **Color-coded Elements**: Different colors for different actions

## 🔧 Customization

The game is easily customizable:
- Modify scales in the JavaScript code
- Adjust scoring formula in `calculateFinalScore()`
- Change colors and styling in the CSS
- Add new features by extending the game state

## 📊 Statistics Tracked

- Total games played
- Best score achieved
- Average accuracy
- Total play time
- Guess change patterns

## 🎉 Future Enhancements

- Sound effects and audio feedback
- Global leaderboard system
- Additional scale options (1-50, 1-100)
- Tutorial mode for new players
- Multiplayer support
- Achievement system

---

**Created with ❤️ for fun and learning!**

*Skaalat - Where every guess tells a story!*
