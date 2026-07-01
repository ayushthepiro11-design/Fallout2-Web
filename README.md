# ☢️ Fallout 2 Web Client

Play the classic post-apocalyptic RPG **Fallout 2** directly inside your web browser. This is an unofficial web port powered by Emscripten and WebAssembly (`fallout2-ce`), fully optimized for static web hosting.

---

## 🚀 How to Play

To play the game, you need to supply your own original Fallout 2 game assets. This client does **not** host, package, or distribute any copyrighted files.

1. Open the web application.
2. Drag and drop the following files from your local Fallout 2 installation directory (GOG, Steam, or original CD):
   * **`MASTER.DAT`**
   * **`CRITTER.DAT`**
3. Wait a few seconds for the client to save these files into your browser's **IndexedDB** local storage. *(This is a one-time process; assets are persisted locally).*
4. Click **Initialize Game Runtime** to boot the game.
5. Press **F11** or click the fullscreen toggle to play in fullscreen.

---

## ⚡ Key Features

* **Persistent Offline Storage:** Uses browser IndexedDB to save your game files locally. The next time you visit the page, the game boots up instantly without re-uploading.
* **WebGL Rendering:** Pixel-perfect rendering with aspect-ratio scaling to preserve the retro CRT presentation.
* **Input Interceptor:** Captures key controls and blocks default browser events (like backspace, tab, or context menu) from interrupting your gameplay.
* **Reset Storage Button:** Clear saved databanks in one click to re-upload files or change GOG/Steam assets.

---

## 🛠️ Self-Hosting & Running Locally

If you want to run this client locally on your own machine:

### 1. Clone the repository
```bash
git clone https://github.com/ayushthepiro11-design/Fallout2-Web.git
cd Fallout2-Web
```

### 2. Run a local server
Because of browser CORS and WebAssembly security restrictions, you cannot launch this by double-clicking `index.html`. You must run it through a local web server.

* **Using Python:**
  ```bash
  python -m http.server 8081
  ```
* **Using Node.js:**
  ```bash
  npx serve .
  ```

Open your browser and navigate to `http://localhost:8081`.

---

## 🌐 Deployment

This project is pre-configured for seamless deployment to static hosting platforms like **Vercel** or **Netlify**.

The included `vercel.json` file automatically handles setting up the required security headers (COOP and COEP) and MIME types necessary for WebAssembly runtimes:

* **Cross-Origin-Opener-Policy:** `same-origin`
* **Cross-Origin-Embedder-Policy:** `require-corp`

Simply link this repository to your hosting provider of choice and trigger a deployment.

---

## 🎖️ Credits & Acknowledgments

This web client is built on top of incredible open-source projects:

* **[fallout2-ce](https://github.com/alexbatalov/fallout2-ce)** - The modern C++ community engine rewrite of Fallout 2 by Alex Batalov.
* **[Emscripten Compiler](https://emscripten.org/)** - The toolchain that compiled the engine source code into WebAssembly and JavaScript.
* **[Simple DirectMedia Layer (SDL2)](https://www.libsdl.org/)** - Low-level hardware access layer used for rendering, input routing, and audio.
* **IndexedDB API & HTML5 WebGL** - Browser technologies used to persistent-cache assets locally and render the game canvas.

---

## ⚖️ Legal Disclaimer

* This is an unofficial community project.
* Fallout 2 is a registered trademark of Bethesda Softworks / ZeniMax Media.
* No game files, audio, graphics, or proprietary assets are stored in this repository. All assets remain the copyright of their respective owners.
