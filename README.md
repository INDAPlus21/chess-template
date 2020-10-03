# Chess Template

This is a dependency to `rust-task-6`. No need to download.

## Use

Import the library to your GUI application by adding the following to your `Cargo.toml` file.
```toml
[dependencies]
chess_template = { git = "https://github.com/INDAPlus20/chess-template.git" }
```

Then, reference the library by adding the following to your Rust files.
```rust
use chess_template::{ Game, GameState, Colour, PieceType };
```

## API Documentation

The API follows the documentation as given in the instructions to rust-task-3 with the exceptions of some public enumerables. 

### Enumerables
| **Enumerable** | **Values** | **Description** |
|----------------|------------|-----------------|
| `GameState`    | `InProgress`, `Check`, `GameOver` | Represents the state that a game can have. |
| `Colour`       | `White`, `Black` | Represents the colour of a chess piece. |
| `PieceType`    | `King`, `Queen`, `Bishop`, `Knight`, `Rook`, `Pawn` | Represents the type of a chess piece. |

### Structure `Game`
*As stated in the rust-task-3 assignment.*
| **Function** | **Description** |
|--------------|-----------------|
| `pub fn new() -> Game` | Initialises a new board with pieces. |
| `pub fn make_move(&mut self, _from: String, _to: String) -> Option<GameState>` | If the current game state is `InProgress` and the move is legal, move a piece and return the resulting state of the game. |
| `pub fn set_promotion(&mut self, _piece: String) -> ()` | Set the piece type that a peasant becames following a promotion. |
| `pub fn get_game_state(&self) -> GameState` | Get the current game state. |
| `pub fn get_possible_moves(&self, _position: String) -> Optional<Vec<String>>` | If a piece is standing on the given tile, return all possible new positions of that piece. Don't forget to the rules for check. _(optional)_ Don't forget to include en passent and castling. |

Positions are given as strings with the format `"<file><rank>"`.