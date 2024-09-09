# 📝 Bubbles Code Text Editor

**Bubbles Code Text Editor** is a powerful, feature-rich code editor designed for developers who need a simple, efficient, and lightweight tool to write, save, and execute code. Built using **Rust** and **eframe::egui**, the editor supports multiple programming languages, including Python, JavaScript (Node.js), Rust, Batch, and PowerShell. It also offers essential features such as file management, auto-save, and real-time code execution.

## 🌟 Key Features

### 1. Multi-language Support:
- Write and execute code in **Python**, **JavaScript (Node.js)**, **Rust**, **Batch**, and **PowerShell** directly from the editor.

### 2. File Management:
- **Save** your work to a file or **load** an existing file with ease using the simple file input dialog.

### 3. Code Execution:
- **Run code instantly**: Execute the code you’ve written directly within the editor for supported languages.
- Output from execution is displayed in a dedicated output section.

### 4. Auto-save:
- Automatically save your code at a user-defined interval, so you don’t have to worry about losing your work.

### 5. Clear Interface:
- Built using **eframe::egui**, the user interface is clean and easy to navigate.
- Real-time editing with support for **code editor** features like a monospaced font and large text areas for enhanced readability.

### 6. Language-Specific Execution:
- **Python**: Execute Python code directly.
- **JavaScript**: Use Node.js to run JavaScript code.
- **Rust**: Compile and run Rust programs using `rustc`.
- **Batch**: Execute Batch commands in a Windows environment.
- **PowerShell**: Run PowerShell scripts on supported platforms.

## 🛠️ Installation Instructions

To run **Bubbles Code Text Editor** on your machine, follow these steps:

### Prerequisites:
1. Install **Rust**: If you don't have Rust installed, you can get it:
-  [Windows 64 Bit RUST Installer](https://static.rust-lang.org/rustup/dist/x86_64-pc-windows-msvc/rustup-init.exe)
-  [Windows 32 Bit RUST Installer](https://static.rust-lang.org/rustup/dist/i686-pc-windows-msvc/rustup-init.exe)
2. Install **Node.js**: Required for running JavaScript code. Download and install it from the [Node.js official website](https://nodejs.org/).

### Steps to Run:
1. **Clone the repository:**
   ```
   git clone https://github.com/kernferm/bubbles-code-text-editor.git
   cd bubbles-code-text-editor
   ```

2. **Build and run the application:**
   ```
   cargo run
   ```

3. ***The application will open the editor, and you can start coding in your preferred language.***

## 🔧 Usage Instructions

A) **Writing and Running Code:** 

1. Select the language of your code (e.g., Python, Rust, JavaScript) by clicking the respective button at the top of the editor.
2. Write or paste your code into the editor.
3. To run the code, click on the `▶️ Run Code` button. The output will be displayed below the editor.

B) **File Management:**
- To save the code to a file:
1. Enter the file path in the provided input field.
2. Click on `💾 Save` to save your current work.

- To `load` an existing file:
1. Enter the file path in the input field.
2. Click `📂 Load` to open the file in the editor.

C) **Auto-Save:**

1. Enable `Auto-Save` by checking the box labeled `Enable Auto-Save`.
2. Set the interval (in minutes) for how frequently you want the editor to auto-save your work.

D) **Clearing the Editor:**

1. Click `🗑️ Clear` to remove all content from the editor and reset the output and status messages.

## 🚀 How It Works
- The `Bubbles Code Text Editor` supports multiple languages, and here's how the code execution works for each:

1. **Python:** Runs the code using the `python` command.
2. **JavaScript:** Uses Node.js (`node`) to execute JavaScript code.
3. **Rust:** Compiles Rust code using `rustc`, then executes the compiled binary.
4. **Batch:** Executes Batch commands via `cmd.exe` on Windows systems.
5. **PowerShell:** Executes PowerShell commands via `powershell` on supported platforms.

## **Auto-Save Mechanism:**

- Auto-save is implemented using asynchronous operations powered by `Tokio`. When auto-save is enabled, the editor saves the file at the specified intervals without user intervention.

## **Code Output:**

- Output from running the code is captured and displayed in the editor’s output section. This feature works by executing the appropriate system command based on the selected language and capturing the result of the execution.

## **🏗️ Project Structure**

```
/src
  └── main.rs           # Main application code
  └── notepad_app.rs     # Implementation of NotepadApp
Cargo.toml               # Project dependencies and metadata
README.md                # Project documentation
```

## **🧩 Dependencies**

- **eframe:** The main framework for building the user interface.
- **Tokio:** Used for asynchronous operations like auto-save.
- **std::process:** Standard Rust library for executing external processes.
- **fs:** Standard Rust file system operations for saving/loading files.

## **🚧 Future Enhancements**

- Add syntax highlighting for different languages.
- Expand support for additional programming languages.
- Improve error handling and better output formatting.
- Add customizable themes for the user interface.


## **🤝 Contributing**

We welcome contributions to **Bubbles Code Text Editor**. If you would like to contribute, please fork the repository, make your changes, and submit a pull request. 

Feel free to submit issues and feature requests via the [GitHub Issues page](https://github.com/kernferm/bubbles-code-text-editor/issues). Your feedback helps improve the project!


## **🎉 Acknowledgments**

Special thanks to the Rust community for providing excellent tools and libraries. This project is inspired by a need for a simple yet powerful code editor that supports multiple languages and is easy to use.

## 📄 License

**Bubbles Code Text Editor** is proprietary software, and the owner retains all rights to the project. You may contribute to the project, but by doing so, you agree to grant the owner an irrevocable, perpetual, royalty-free license to use, modify, and distribute your contributions. 

While contributions are credited, contributors do not retain ownership or control over any part of the project, and the final decision regarding contributions remains with the owner. No part of the codebase may be reproduced, distributed, or transmitted in any form without explicit permission from the owner.





















