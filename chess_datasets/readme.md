# Chess Games Dataset

The **`chess_games_selected.csv`** file contains a subset of 1000 chess games.  
The original dataset is available at:  
[Download the full dataset](https://drive.google.com/file/d/1-7e-7wuW54uZP3EAmsilv0ScOhSpO1tY/view?usp=sharing).

## Column Descriptions

- **`game_id`**: Unique identifier for the game.  
- **`ai_player`**: Indicates whether the AI player is `white` or  `black`.  
- **`white_elo`**: ELO rating of the White player.  
- **`black_elo`**: ELO rating of the Black player.  
- **`winner`**: The winner of the game (`white`, `black`, or `draw`).  
- **`total_moves`**: Total number of moves played in the game.  
- **`eco`**: ECO (Encyclopaedia of Chess Openings) code assigned to the game.  
- **`moves_list`**: A list of sequential chess moves played in this game in algebraic notation.  
- **`move_category`**: A list categorizing each move:  
  - `1`: Opening (Start)  
  - `2`: Middlegame  
  - `3`: Endgame  
