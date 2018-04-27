**Create a game**
----
  Create a new game. Player is registered and bound to a `game_id` returned in the response.

* **URL**

  /create_game

* **Method:**
  
  `POST`
  
* **Data Params**
    None

* **Success Response:**

  Example:
```json
  {
    "game_id":234,
  }
```
  **Code:** 200

**Refresh game board**
----
  Refresh the game board.

* **URL**

  /refresh

* **Method:**
  
  `POST`
  
* **Data Params**

  Example:
```json
 {
    "game_id":234,
    "width":75,
    "height":50,
    "snake":[[5,6],[5,7],[5,8],[6,8]],
    "food":[[1,2],[2,5]]
  }
```

* **Success Response:**

  **Code:** 200

**Game Over**
----
  Game over

* **URL**

  /game_over

* **Method:**
  
  `POST`
  
* **Data Params**

  Example:
```json
 {
    "game_id":273473,
    "score":1534
  }
```

* **Success Response:**

  **Code:** 200
