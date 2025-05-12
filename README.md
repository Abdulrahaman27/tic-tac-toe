```markdown
# ⭕ Tic-Tac-Toe (C# Console)

![Tic-Tac-Toe Demo](tictactoe-demo.gif) *(optional animated preview)*

## 🎮 Features
- **Classic 3x3 grid gameplay**
- **Turn-based player system**:
  - Player 1: `X`
  - Player 2: `O`
- **Win detection**: All 8 possible winning combinations
- **Input validation**:
  - Prevents overwriting occupied spaces
  - Handles invalid inputs gracefully
- **Visual feedback**:
  - Clear board rendering
  - Turn indicators
  - Win/tie announcements

## 🚀 Quick Start
```bash
dotnet run
```

## 🖥️ Code Architecture
```csharp
Program.cs
├── Main Game Loop
│   ├── DrawBoard()          // Renders the 3x3 grid
│   ├── CheckWin()           // Detects wins/draws (8 conditions)
│   ├── DrawX()/DrawO()      // Marks player moves
│   └── Input Validation     // Prevents illegal moves
```

## 🕹️ How to Play
1. Players alternate turns entering numbers 1-9
2. Current player's symbol is automatically placed
3. Game ends when:
   - A player gets 3 in a row (any direction)
   - All spaces are filled (tie)

## 📺 Sample Gameplay
```
Player 1: X and Player 2: O

     |     |     
  1  |  2  |  3  
_____|_____|_____
     |     |     
  4  |  5  |  6  
_____|_____|_____
     |     |     
  7  |  8  |  9  

Player 1's turn
5  // Player input
```

## 🛡️ Error Handling
- **Occupied space**:
  ``` 
  Sorry the row 5 is already marked with X
  Please wait 2 seconds while board reloads...
  ```
- **Invalid input**: Auto-rejects non-numeric entries

## 🔧 Potential Enhancements
1. **AI Opponent**:
   - Implement minimax algorithm
2. **Enhanced UI**:
   - Add colors with `Console.Color`
   - Use `Spectre.Console` for borders
3. **Features**:
   - Score tracking
   - Player name input
   - Resizable board

## 📊 Win Condition Logic
```csharp
// Checks all 8 possible winning combinations
if (spaces[0] == spaces[1] && spaces[1] == spaces[2] || // Row 1
    spaces[3] == spaces[4] && spaces[4] == spaces[5] || // Row 2
    spaces[6] == spaces[7] && spaces[7] == spaces[8] || // Row 3
    /* ... 5 more conditions ... */)
{
    return 1; // Win detected
}
```

## 📜 License
MIT License - Free for personal and educational use
```
