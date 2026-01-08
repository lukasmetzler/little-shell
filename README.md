# Little Shell

A functional, Unix-like shell implementation written in Rust. This project was developed as part of a systems programming challenge.

## Features

- **Command Execution**: Runs external binaries found in the system `PATH`.
- **Built-in Commands**: Includes native implementations of `echo`, `pwd`, `cd`, `type`, `exit`, and `history`.
- **Pipelines**: Supports multi-stage piping (e.g., `cat file.txt | grep "search" | wc -l`) using `os_pipe`.
- **I/O Redirection**: 
    - Redirect `stdout` (`>`) and `stderr` (`2>`).
    - Append mode for both `stdout` (`>>`) and `stderr` (`2>>`).
- **Advanced History Management**:
    - Persistent history saved to a file specified by the `HISTFILE` environment variable.
    - Support for `history -r` (read), `-w` (write), and `-a` (append) flags.
- **Terminal UI**:
    - Interactive line editing and command history navigation (Up/Down arrows).
    - **Tab-Completion**: Basic autocompletion for commands and builtins.
- **Complex Parsing**: Handles single quotes (`'`), double quotes (`"`), and backslash (`\`) escaping.

## Tech Stack & Dependencies

- **[Rust](https://www.rust-lang.org/)**: The core language for safety and performance.
- **[Rustyline](https://github.com/kkawakam/rustyline)**: A thread-safe readline implementation for the interactive prompt.
- **[os_pipe](https://github.com/oconnor663/os_pipe.rs)**: For handling cross-platform system pipes during pipeline execution.


## Getting Started

### Prerequisites
- [Rust & Cargo](https://rustup.rs/) (latest stable version recommended)

### Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/rust-shell.git](https://github.com/your-username/rust-shell.git)
   cd rust-shell
   cargo run

## About This Project

This is a **learning/practice project**. It was built to understand the intricacies of:

* **Process Management**: How shells manage file descriptors and child processes.
* **Concurrency**: Handling concurrency when running shell builtins inside threads to support piping.
* **Parsing**: String parsing for shell-specific syntax.

While functional, it is not intended to replace a production shell like Bash or Zsh.
Refactoring and Improvements will also be considered in further versions, as at this current stage, the focus is on learning and understanding the underlying concepts.
