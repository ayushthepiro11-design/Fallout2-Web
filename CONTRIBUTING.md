# Contributing to Fallout 2 Web Client

Thank you for showing interest in contributing to the Fallout 2 Web Client project! Contributions from the community help make this web port smoother, faster, and more robust.

---

## 🛠️ Code of Conduct

* Be respectful and professional in all communications.
* Maintain clean, readable, and well-commented code.
* Do not commit or distribute copyrighted Fallout 2 game assets (`.dat` files) to the repository.

---

## 🚀 How to Contribute

### 1. Report Bugs & Request Features
If you find a bug or have an idea to improve the application:
* Search the existing issues to ensure it hasn't been reported yet.
* Open a new issue with a clear description, steps to reproduce, and screenshots if applicable.

### 2. Submit Pull Requests
To submit a code change:
1. Fork the repository.
2. Create a new branch for your feature or bug fix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes and test them locally (e.g., using `python -m http.server 8081`).
4. Commit your changes with clear, descriptive, and conventional commit messages (e.g., `feat: add feature`, `fix: resolve issue`).
5. Push to your fork and submit a Pull Request to the `main` branch.

---

## 🎨 Development & Style Guide

* **Vanilla Stack:** The interface is built using standard HTML5, modern vanilla CSS, and clean JavaScript.
* **Optimization:** Keep performance in mind. Avoid layout thrashing, use passive event listeners where applicable, and minimize CPU overhead to ensure the WebAssembly runtime has maximum resources.
