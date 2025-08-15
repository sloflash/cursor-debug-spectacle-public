# Cursor Debug Spectacle 🎭

> A VS Code extension that shows variables from the previous line during Python debugging sessions.

<img width="794" height="828" alt="Main" src="https://github.com/user-attachments/assets/257fc1df-45f2-43f8-ac25-099af028362d" />


![VS Code Extension](https://img.shields.io/badge/VS%20Code-Extension-blue)
![Python](https://img.shields.io/badge/Python-Debugging-green)
![Version](https://img.shields.io/badge/version-1.0.0-orange)

## ✨ Features

- 🐍 **Python debugging support** - Works seamlessly with debugpy
- 📊 **Smart variable tracking** - Shows only variables used in the previous line of code
- 🎯 **Intelligent parsing** - Automatically extracts variable names from Python code
- 🔍 **Clean DebugView panel** - Integrated UI next to Terminal and Ports
- 🚀 **Performance optimized** - Minimal overhead during debugging

## 🚀 Installation

### Method 1: Download and Install
1. Download the latest `cursor-debug-spectacle-*.vsix` file
2. Install it in VS Code:
   ```bash
   code --install-extension cursor-debug-spectacle-1.0.0.vsix
   ```

### Method 2: VS Code Extensions Panel
1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Search for "Cursor Debug Spectacle"
4. Click Install

## 📖 Usage

1. **Install the extension**
2. **Open your Python file** in VS Code
3. **Start debugging** your Python code (F5 or Debug panel)
4. **Set breakpoints** and step through your code (F10/F11)
5. **Check the "Debug View" panel** - it will show variables from the previous line

### Example

```python
a = 10          # When stopped here: shows nothing
b = 20          # When stopped here: shows [a]
c = a + b       # When stopped here: shows [b]
result = a * c  # When stopped here: shows [c, a]
```

## 🔧 How It Works

The extension:
1. **Detects Python debug sessions** using VS Code's debug API
2. **Listens for breakpoint stops** via `onDidChangeActiveStackItem`
3. **Parses the previous line** to extract variable names
4. **Retrieves variable values** from the debug adapter
5. **Displays them** in a clean webview panel

## 📋 Requirements

- **VS Code**: 1.74.0 or higher
- **Python**: Any version supported by debugpy
- **Debugger**: Uses Python's built-in debugpy (included with Python extension)

## 🎯 Use Cases

Perfect for:
- **Learning Python** - See how variables change line by line
- **Debugging complex logic** - Track variable flow
- **Code reviews** - Understand variable dependencies
- **Teaching** - Demonstrate variable scope and changes

## 🔧 Configuration

No configuration needed! The extension works out of the box with Python debugging.

## 🐛 Troubleshooting

**Panel not showing?**
- Make sure you're debugging Python code with breakpoints
- Check that the "Debug View" tab appears in the bottom panel area

**Variables not appearing?**
- Ensure you're stepping through code (F10) not just running (F5)
- Variables only show after the debugger stops at a breakpoint

## 🤝 Contributing

This is a private repository. The extension is distributed via the public releases.

## 📄 License

MIT License - see LICENSE file for details.

## 🔗 Links

- [Download Latest Release](https://github.com/sloflash/cursor-debug-spectacle-public)
- [VS Code Debugging Guide](https://code.visualstudio.com/docs/editor/debugging)
- [Python in VS Code](https://code.visualstudio.com/docs/languages/python)

---

**Made with ❤️ for a better debugging experience**

*Enhance your Python debugging workflow with intelligent variable tracking!*
