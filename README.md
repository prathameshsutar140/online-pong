# 🏓 Single-File Pong — Local & Online
A lightweight, zero-dependency Pong game built in a single file featuring local and peer-to-peer online multiplayer.
---
## 🚀 Game Features
* 🤖 **Single-Player Mode:** Play against an automated computer AI.
* 👥 **Local 2-Player Mode:** Play with a friend on the same device using shared controls.
* 🌐 **Online Peer-to-Peer Mode:** Connect directly with a friend online using manual WebRTC signaling without needing a backend server.
* ⚡ **Zero Dependencies:** Fully self-contained inside a single `pong.html` file.
---
## 🛠️ Technologies Used
* 📄 **HTML5:** Page structure and layout rendering.
* 🎨 **CSS3:** Dark-themed responsive styling.
* ⚡ **JavaScript (ES6):** Game loop, collision physics, and UI logic.
* 🎨 **HTML5 Canvas API:** 2D graphic rendering for paddles, ball, and field.
* 📡 **WebRTC (RTCDataChannel):** Direct peer-to-peer network communication between host and guest players.
---
## ⚙️ How the Game is Made
* **Authoritative Host Architecture:** In online mode, the Host player acts as the server. The host calculates ball physics, wall bounces, paddle collisions, and score tracking, then broadcasts the state to the Client.
* **WebRTC Manual Signaling:** Connects two devices directly across the internet using manual SDP Offer/Answer JSON string exchanges through text boxes.
* **Canvas Rendering Loop:** Uses `requestAnimationFrame` to maintain smooth 60 FPS frame updates and physics steps.
---
## 🎮 How to Play
### 1. Launching the Game
Simply open `pong.html` in any web browser.
### 2. Controls & Game Modes

| Mode | Left Paddle Controls | Right Paddle Controls |
| :--- | :--- | :--- |
| **Single Player** | Mouse **OR** `Up` / `Down` Arrow keys | Computer AI |
| **Local 2-Player** | `W` / `S` keys **OR** Mouse | `Up` / `Down` Arrow keys |
| **Online Host** | Mouse **OR** `Up` / `Down` Arrow keys | Guest (via WebRTC) |
| **Online Join** | Host (via WebRTC) | `Up` / `Down` Arrow keys **OR** Mouse |

### 3. How to Connect Online
1. **Host:** Select **Online — Host** mode, click **Host Online (Create Offer)**, wait a moment, copy the generated text from the Offer box, and send it to your friend.
2. **Guest:** Select **Online — Join** mode, paste the Host's Offer into the input box, click **Join Online (Create Answer)**, copy the generated Answer text, and send it back to the Host.
3. **Host:** Paste the friend's Answer into the **Apply Answer** text box and click **Apply Answer**.
4. Click **Start** to begin playing!
