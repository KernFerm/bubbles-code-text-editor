# Bubbles Code Text Editor

Bubbles Code Text Editor is a versatile and lightweight code editor designed for writing, executing, and testing code in multiple programming languages. It is ideal for developers who need a simple but powerful environment to quickly test snippets of code, save projects, and debug in various languages, all from a single interface. This editor supports Python, HTML, JavaScript (Node.js), Rust, Batchfiles, PowerShell, and CSS.

**This project was built on a 64-bit Windows system**, ensuring compatibility with Windows environments, but it can be modified to run on other platforms such as Linux and macOS with minimal changes.

## Key Features

- **Multi-Language Support**: Write and execute code in Python, HTML, JavaScript (Node.js), Rust, CSS, Batchfile, and PowerShell.
- **Code Execution**: Instantly run your code from within the editor and see the output in real time.
- **Auto-Save Functionality**: Keep your work safe with automatic saving at user-defined intervals.
- **Basic File Operations**: Open, save, and edit files with ease, including file format flexibility (e.g., `.py`, `.html`, `.js`, `.bat`, `.ps1`, etc.).
- **Integrated Output Display**: View the output or errors generated from the code execution directly within the editor.
- **Cross-Language Workflow**: Seamlessly switch between languages, and execute code in each environment without leaving the editor.
- **64-bit System Optimized**: The editor is designed and optimized for 64-bit Windows systems, ensuring smooth execution of even resource-intensive tasks.

## System Requirements

### **Operating System**: 
- **Windows**: Bubbles Code Text Editor was developed and tested on a 64-bit Windows system. It is fully compatible with Windows 10 and above.
- **64-bit Architecture**: The editor is designed for 64-bit systems, providing optimal performance for heavier applications and multi-language support.

### **Dependencies**:
- **Rust**: The core of the editor is built in Rust. Make sure you have the latest version installed.
- **Python**: For executing Python code, you need the Python interpreter installed.
- **Node.js**: Required for executing JavaScript code.
- **Rustc**: The Rust compiler is required to run Rust code.
- **PowerShell**: For executing PowerShell scripts.

### **Additional Tools**:
- **cmd.exe**: Available on Windows for running batch files (`.bat`).
- **PowerShell**: Available by default on modern Windows versions for running PowerShell scripts (`.ps1`).

---

## Installation Instructions

### 1. **Clone the Repository**
   Start by cloning the repository from GitHub:

   ```
   git clone https://github.com/kernferm/bubbles-code-text-editor.git
   cd bubbles-code-text-editor
   ```

## 2. **Install Rust and Cargo**
- If you don't have Rust installed on your system, you can install it by running the following command:

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

- For Windows users, you can also download the Rust installer

[RUST 64Bit Windows](https://static.rust-lang.org/rustup/dist/x86_64-pc-windows-msvc/rustup-init.exe)
[RUST 32Bit Windows](https://static.rust-lang.org/rustup/dist/i686-pc-windows-msvc/rustup-init.exe)
- Follow the instructions when installing `RUST`. 

## 3. **Install Additional Dependencies**
Bubbles Code Text Editor depends on eframe, egui, and tokio. You don’t need to install these manually; they will be pulled in by Cargo when you compile the project.
