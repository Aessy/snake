# Snake

## Create Game

Create a new game. Player is registered and bound to `game` returned in the response.

### Request
```http
POST /games HTTP/1.1
```

### Response
```http
HTTP/1.1 201 Created
Location: https://snake.payex.com/games/b5d6fd66c28b4b4cab1729d48f5f72eb

{
  "game": "https://snake.payex.com/games/b5d6fd66c28b4b4cab1729d48f5f72eb",
  "states": "https://snake.payex.com/games/b5d6fd66c28b4b4cab1729d48f5f72eb/states"
}
```

## Refresh Game State
Refresh the state of the game to update the position of the snake and food.

### Request
```http
POST /games/b5d6fd66c28b4b4cab1729d48f5f72eb/states

{
  "state": "refresh",
  "width": 75,
  "height": 50,
  "snake": [
    { "x": 5, "y": 6 },
    { "x": 5, "y": 7 },
    { "x": 5, "y": 8 },
    { "x": 6, "y": 8 }
  ],
  "food": [
    { "x": 1, "y": 2 },
    { "x": 2, "y": 5 }
  ]
}
```

### Response
```http
HTTP/1.1 201 Created
Location: https://snake.payex.com/games/b5d6fd66c28b4b4cab1729d48f5f72eb/states/daa1ef6733db46dc9481a5270bf36d40
```

## Game Over
Indicates that the game is over.

### Request
```http
POST /games/b5d6fd66c28b4b4cab1729d48f5f72eb/states

{
  "state": "end",
  "score": 1534,
}
```

### Response
```http
HTTP/1.1 201 Created
Location: https://snake.payex.com/games/b5d6fd66c28b4b4cab1729d48f5f72eb/states/end
```
