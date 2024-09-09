## Check `.rs` file thanks :) 


# 📝 Bubbles Code Text Editor

**Bubbles Code Text Editor** is a powerful, feature-rich code editor designed for developers who need a simple, efficient, and lightweight tool to write, save, and execute code. Built using **Rust** and **eframe::egui**, the editor supports multiple programming languages, including **Python**, **JavaScript** (`Node.js`), **Rust**, **Batch**, and **PowerShell**. It also offers essential features such as file management, auto-save, and real-time code execution.

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

---

## 🛠️ Building and Running Instructions (for 64-bit and 32-bit systems)

### Prerequisites:

1. **Install Rust**: Ensure that you have Rust installed. Use the following installers based on your system:
   - [Windows 64-bit Rust Installer](https://static.rust-lang.org/rustup/dist/x86_64-pc-windows-msvc/rustup-init.exe)
   - [Windows 32-bit Rust Installer](https://static.rust-lang.org/rustup/dist/i686-pc-windows-msvc/rustup-init.exe)

2. **Install Node.js**: Required for running JavaScript code. Download and install it from the [Node.js official website](https://nodejs.org/).

## 🛠️ Building and Running on a 32-bit System

By default, when you compile Rust code on a `64-bit system`, it targets `64-bit architecture`. However, Rust allows you to `build` and `run` applications for `32-bit systems` by specifying the appropriate target. Below is an explanation on how to set it up.

### Steps to Build and Run for 32-bit Systems:

1. **Install Rust (if not installed)**

   Make sure you have installed the Rust toolchain on your machine:

   - [Windows 32-bit Rust Installer](https://static.rust-lang.org/rustup/dist/i686-pc-windows-msvc/rustup-init.exe)

2. **Add the 32-bit Target**

   Since the program is built on a `64-bit system`, you'll need to add the `32-bit target` to allow building for `32-bit systems`.

   In your terminal, run the following command to add the 32-bit target:
   ```
   rustup target add i686-pc-windows-msvc
   ```

## Build for 32-bit Architecture

This command tells Rust to add support for compiling to `32-bit Windows systems`.

Once you’ve added the 32-bit target, you can build the project specifically for 32-bit using the `--target` flag.

### To build for 32-bit:

```
cargo build --target=i686-pc-windows-msvc
```
- This command will compile your project for the `32-bit target`. The resulting executable will be compatible with `32-bit Windows systems`.

## Run the Program (Optional)

After building the program, you can run the `32-bit version` directly by specifying the `target`.

### Run the following command:

```
cargo run --target=i686-pc-windows-msvc
```
This will compile and immediately run the 32-bit version of the **Bubbles Code Text Editor**.

## Why This is Needed:

- **Default Target (64-bit)**: If you're on a 64-bit system, Rust will automatically build and run for the `x86_64-pc-windows-msvc` target, which is the 64-bit version.
- **Cross-compiling for 32-bit**: By specifying `i686-pc-windows-msvc`, you ensure the binary is compiled for 32-bit systems, enabling it to run on older machines or systems that only support 32-bit executables.

## Common Issues and Fixes:

- **Missing 32-bit libraries**: If you encounter errors while building for the 32-bit target (e.g., missing libraries), you may need to install additional 32-bit development tools. On Windows, installing the MSVC 32-bit build tools will solve this.

- **Running on a 32-bit system**: After building the 32-bit executable on a 64-bit system, transfer the resulting binary to a 32-bit machine for testing. The binary should work as expected on any 32-bit Windows system.

## Recap:

### Add 32-bit target using:
```
rustup target add i686-pc-windows-msvc
```

### Build for 32-bit using:
```
cargo build --target=i686-pc-windows-msvc
```

### Run for 32-bit using:
```
cargo run --target=i686-pc-windows-msvc
```

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

3. **Start using the editor:** The application will open the editor, and you can start coding in your preferred language.

## 🔧 Usage Instructions

### A) Writing and Running Code:
1. Select the language of your code (e.g., Python, Rust, JavaScript) by clicking the respective button at the top of the editor.
2. Write or paste your code into the editor.
3. To run the code, click on the "▶️ Run Code" button. The output will be displayed below the editor.

### B) File Management:
#### To save the code to a file:
1. Enter the file path in the provided input field.
2. Click on "💾 Save" to save your current work.

#### To load an existing file:
1. Enter the file path in the input field.
2. Click "📂 Load" to open the file in the editor.

### C) Auto-Save:
1. Enable Auto-Save by checking the box labeled "Enable Auto-Save".
2. Set the interval (in minutes) for how frequently you want the editor to auto-save your work.

### D) Clearing the Editor:
1. Click "🗑️ Clear" to remove all content from the editor and reset the output and status messages.

## 🚀 How It Works

### Code Execution:
The Bubbles Code Text Editor supports multiple languages, and here's how the code execution works for each:

- **Python**: Runs the code using the `python` command.
- **JavaScript**: Uses Node.js (`node`) to execute JavaScript code.
- **Rust**: Compiles Rust code using `rustc`, then executes the compiled binary.
- **Batch**: Executes Batch commands via `cmd.exe` on Windows systems.
- **PowerShell**: Executes PowerShell commands via `powershell` on supported platforms.

### Auto-Save Mechanism:
Auto-save is implemented using asynchronous operations powered by **Tokio**. When auto-save is enabled, the editor saves the file at the specified intervals without user intervention.

### Code Output:
Output from running the code is captured and displayed in the editor’s output section. This feature works by executing the appropriate system command based on the selected language and capturing the result of the execution.

## 🏗️ Project Structure
```
/src
  └── main.rs           # Main application code
  └── notepad_app.rs     # Implementation of NotepadApp
Cargo.toml               # Project dependencies and metadata
README.md                # Project documentation
```

## 🧩 Dependencies
- **eframe**: The main framework for building the user interface.
- **Tokio**: Used for asynchronous operations like auto-save.
- **std::process**: Standard Rust library for executing external processes.
- **fs**: Standard Rust file system operations for saving/loading files.

## 🚧 Future Enhancements
- Add syntax highlighting for different languages.
- Expand support for additional programming languages.
- Improve error handling and better output formatting.
- Add customizable themes for the user interface.

## 🤝 Contributing
We welcome contributions to **Bubbles Code Text Editor**. If you would like to contribute, please fork the repository, make your changes, and submit a pull request. We appreciate your help in improving the project!

## 📄 License
**Bubbles Code Text Editor** is proprietary software, and the owner retains all rights to the project. You may contribute to the project, but by doing so, you agree to grant the owner an irrevocable, perpetual, royalty-free license to use, modify, and distribute your contributions.

While contributions are credited, contributors do not retain ownership or control over any part of the project, and the final decision regarding contributions remains with the owner. No part of the codebase may be reproduced, distributed, or transmitted in any form without explicit permission from the owner.
