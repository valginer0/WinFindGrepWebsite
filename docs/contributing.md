# Contributing to WinFindGrep

We welcome contributions to WinFindGrep!

## How to Contribute

- **Reporting Bugs:** Please open an issue on our [GitHub Issues](https://github.com/valginer0/WinFindGrep/issues) page. <!-- Assuming main project repo for issues -->
- **Suggesting Enhancements:** Open an issue to discuss your ideas.
- **Code Contributions:**
    1. Fork the repository.
    2. Create a new branch (`git checkout -b feature/YourFeature`).
    3. Make your changes.
    4. Commit your changes (`git commit -m 'Add some feature'`).
    5. Push to the branch (`git push origin feature/YourFeature`).
    6. Open a Pull Request.

## Development Setup

If you wish to contribute code or build WinFindGrep from source, here's how to set up your development environment:

**Prerequisites:**

*   A Windows operating system.
*   An IDE that supports .NET development, such as:
    *   JetBrains Rider (Recommended)
    *   Visual Studio
*   .NET 9.0 SDK (as the application is built with C# and .NET 9.0 using Windows Forms).

**Building the Application:**

1.  **Get the Source Code:**
    *   Fork the [WinFindGrep repository](https://github.com/valginer0/WinFindGrep) to your GitHub account.
    *   Clone your forked repository to your local machine: 
        ```bash
        git clone https://github.com/YOUR_USERNAME/WinFindGrep.git
        ```
    *   Alternatively, you can download the source code archive directly from GitHub.

2.  **Open and Build the Project:**
    *   Open the `WinFindGrep.sln` solution file in JetBrains Rider or Visual Studio.
    *   Build the solution. This will restore any necessary NuGet packages and compile the application.

3.  **Running for Development:**
    *   You should be able to run the application directly from your IDE for testing and development purposes.

4.  **Creating a Standalone Executable (for testing a release-like build):**
    *   If you want to create a standalone `.exe` similar to the official releases, use the "Publish" feature in your IDE.
    *   Key settings for publishing typically include:
        *   **Deployment Mode:** Self-contained (to include the .NET runtime).
        *   **File Publish Options:** Produce single file (to bundle everything into one `.exe`).

We encourage you to follow existing code style and patterns. If you're introducing a new feature or a significant change, please consider opening an issue first to discuss your ideas!
