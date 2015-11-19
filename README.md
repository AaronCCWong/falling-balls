# Falling Balls
Made in collaboration with Derek Chan.

## Summary
This is a single player game. The goal is to dodge as many balls as possible.

##How to play
Play the game [here](http://www.aaronccwong.com/falling-balls).

## Smooth gameplay
In order to read multiple keydowns utilizing eventListeners at once for smooth gameplay, each keydown changes a boolean value.

```javascript
GameView.prototype.onKeyDown = function(e) {
  var that = this;
  c = e.keyCode;
  switch(c) {
    case 37:
      that.player.left = true;
      break;
    case 39:
      that.player.right = true;
      break;
    case 32:
      that.player.spacebar = true;
      break;
  };
};
```
There is also a onKeyUp function. See [Game View](https://github.com/AaronCCWong/falling-balls/blob/master/lib/gameView.js) for more details.

## Other Technical Features
- Object orientated programming
- Scaleable for more players to be added at once
- Uses physics for gravity and vectors
- Uses Canvas to render everything
- Incorporates live leaderboard.
- Filter's malicious user names

##Future goals
- Use Node.js to add more players and a chatroom
