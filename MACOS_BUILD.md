# Building OMIP on macOS

This document provides instructions for building the OMIP application on a macOS system.

## Prerequisites

Before you can build OMIP, you need to install the following prerequisites:

1.  **Xcode Command Line Tools**: These tools provide essential developers tools for macOS. You can install them by running the following command in your terminal:
    ```bash
    xcode-select --install
    ```

2.  **Go**: OMIP is written in Go, so you will need to install the Go programming language. You can download it from the official Go website: [https://golang.org/dl/](https://golang.org/dl/)

    Alternatively, you can use Homebrew to install Go:
    ```bash
    brew install go
    ```

## Building the Application

Once you have installed the prerequisites, you can build the OMIP application.

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/Wilm0rien/omip.git
    cd omip
    ```

2.  **Build the application**:
    You can build the application in two modes: GUI mode and command-line mode.

    *   **GUI Mode**:
        To build the GUI version of the application, run the following command:
        ```bash
        go build -o omip_gui -ldflags="-X main.CmdLineOpt=default_gui" omip.go
        ```
        This will create an executable file named `omip_gui` in the current directory. You can run it by double-clicking the file or by running the following command in your terminal:
        ```bash
        ./omip_gui
        ```

    *   **Command-Line Mode**:
        To build the command-line version of the application, run the following command:
        ```bash
        go build -o omip_cmd -ldflags="-X main.CmdLineOpt=default_cmd" omip.go
        ```
        This will create an executable file named `omip_cmd` in the current directory. You can run it from your terminal:
        ```bash
        ./omip_cmd
        ```