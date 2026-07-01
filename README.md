# ☢️ Fallout 2 Web Client

Play the classic post-apocalyptic RPG **Fallout 2** directly inside your web browser. This is an unofficial web port powered by Emscripten and WebAssembly (`fallout2-ce`), optimized for hosting on static web servers (like Vercel).

---

## 🚀 How to Play

To play the game, you need to bring your own original Fallout 2 game assets. This client does **not** host or distribute any copyrighted files.

1. Open the hosted web application.
2. Drag and drop the following files from your local Fallout 2 installation folder (GOG, Steam, or original CD):
   * **`MASTER.DAT`**
   * **`CRITTER.DAT`**
3. Wait a few seconds for the client to save these files into your browser's **IndexedDB** storage. *(You only need to do this once!)*
4. Click **Initialize Game Runtime** to boot the game.
5. Press **F11** or click the fullscreen toggle to play in fullscreen.

---

## ⚡ Key Features

* **Persistent Offline Storage:** Uses browser IndexedDB to save your game files locally. The next time you visit the page, the game boots up instantly without re-uploading.
* **WebGL Rendering:** Pixel-perfect rendering with aspect-ratio scaling to keep the retro CRT look.
* **Input Lock:** Traps input controls and prevents browser key defaults (like backspace, tab, or context menu) from interrupting your gameplay.
* **Reset Database Button:** Easily clear your saved databanks to re-upload files or change GOG/Steam assets in one click.

---

## 🛠️ Self-Hosting & Running Locally

If you want to run this client locally on your own computer:

### 1. Clone the repository
```bash
git clone <your-repository-url>
cd legal-app
```

### 2. Run a local server
Because of browser CORS and WebAssembly security restrictions, you cannot launch this by double-clicking `index.html`. You must run it through a local HTTP server.

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

## 🌐 Deploying to Vercel

The repository includes a pre-configured `vercel.json` file. It sets up the required security headers (COOP and COEP) and MIME types necessary for WebAssembly runtimes:

1. Connect your repository to your Vercel account.
2. Click **Deploy**. Vercel will automatically handle the rest as a zero-config static site.

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
