# RubeCube

An accessible 3D Rubik's cube game built for playing with a [QuadStick](https://www.quadstick.com/)
(a mouth-operated joystick with sip-and-puff switches). Everything is in one file, `index.html`, with
no build step and nothing to install: open it in any modern browser, or send the file to someone.

## Playing

- The cube sits in the middle, seen from slightly left and above, with one button per layer placed right
  against the edge it turns: along the left edge for rows, along the bottom edge for columns, and along the
  bottom of the right side for the front, middle and back slices (left click twists them counter-clockwise as seen from the front). Each button
  is slanted to follow the cube edge it sits on.
- **Left click** turns a layer the way the big arrow points. **Right click** turns it the other way.
- Hover over a button first and the pieces it will move get a pink outline.
- The dashed buttons turn the whole cube to show other sides: they sit one step further out, with Spin on the
  left, Tip spanning under the Left and Middle columns and Roll spanning under the Mid and Back slices. This never counts as a move.
- The game bar at the top has Undo, Redo, Scramble and Reset. Scramble and Reset ask for a second click
  while a game is in progress.
- Nothing needs dragging, holding, or pressing two things together, and nothing times out.
- The game is saved in the browser automatically.

Settings cover turn speed, text size, color letters on the stickers (for color blindness), the timer, and
cube notation on the buttons.

## Keys and the QuadStick card

The **Keys** button opens the keybind mode. Every action can take any key or mouse button (right,
middle or side buttons), and keys can be removed. There are two presets:

- **QuadStick card** (default), matching the card in BetterTalk:

  | Gesture | Sends | In the game |
  |---|---|---|
  | Puff, center | Left click | Presses the button under the pointer |
  | Sip, center | Right click | Turns the pointed button the other way |
  | Puff, left | Tab | Moves the yellow frame to the next button |
  | Sip, right | Enter | Presses the framed button |
  | Soft sip, center | Ctrl-C | Presses the framed button the other way |
  | Puff, right | Backspace | Undo |
  | Soft puff, right | Delete | Redo |
  | Sip, left | Esc | Cancel or close |
  | Soft sip, left / right | Ctrl-X / Ctrl-V | Spin the whole cube left / right |

  The arrow keys move the yellow frame, and the letter keys R, L, U, D, F, B, M, E and S turn layers.
- **Letter keys**: R, L, U, D, F, B, M, E and S turn layers, I reverses the next turn, and the arrow
  keys and Q/W turn the whole cube.

Input follows BetterTalk's safe-input rules. A key acts once per press and holding it does not repeat.
Doubled or bounced signals are debounced, and presses in the first 0.4 seconds after the window gains
focus are ignored.

## Publishing with GitHub Pages

In the repository settings, under **Pages**, choose "Deploy from a branch", then `main` and `/ (root)`.
The game will then be served at `https://nelcyon.github.io/rubecube/`.
