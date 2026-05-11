
# f9-Paste2Project

Paste your folder structure and generate the entire project instantly from the terminal.

---

## Overview

f9-Paste2Project is a lightweight CLI utility for Windows that converts a pasted folder tree structure into real files and directories on your system.

Instead of manually creating folders and files one by one, you can simply paste the structure and let f9 build the project for you automatically.

This is especially useful for quickly setting up new projects, recreating repository structures, testing layouts, and development scaffolding.

---

## Features

- Automatically creates nested folders
- Instantly generates files from tree structure input
- Supports standard tree-style syntax (`├──`, `│`, `└──`)
- Fast and lightweight
- Smart indentation and hierarchy detection
- Optimized for Windows CLI usage
- Simple installation with minimal setup

---

## Project Structure

```text
f9/
├── f9.py
├── f9_Installer.bat
└── README.md
````

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/forex911/f9-paste2project.git
cd f9
```

---

## Automatic Setup (Recommended)

Run the installer:

```bash
f9_Installer.bat
```

### What the Installer Does

* Copies project files to:

```text
C:\Users\<your-user>\AppData\Local\f9
```

* Creates the `f9` command (`f9.bat`)
* Safely adds the directory to the User PATH without truncation issues

---

## Important

After installation, restart your terminal:

* Command Prompt
* PowerShell
* VS Code Terminal

This ensures the `f9` command is recognized properly.

---

## Usage

### Step 1: Run the Command

```bash
f9
```

---

### Step 2: Paste Your Folder Structure

Example:

```text
my-app/
├── src/
│   ├── index.js
│   └── app.js
├── public/
│   └── index.html
└── package.json
```

---

### Step 3: Finish Input

Press:

```text
CTRL + Z
ENTER
```

This signals the end of input in Windows.

---

## Example Output

```text
DIR:  my-app
DIR:  my-app/src
FILE: my-app/src/index.js
FILE: my-app/src/app.js
DIR:  my-app/public
FILE: my-app/public/index.html
FILE: my-app/package.json
```

Your project structure is now created instantly.

---

## How It Works

The tool:

* Reads pasted input line by line
* Detects indentation and nesting levels
* Uses a stack-based structure to track directories
* Creates folders using `Path.mkdir()`
* Creates files using `Path.touch()`

This ensures accurate recreation of the provided structure.

---

## Common Use Cases

* Quickly starting new projects
* Recreating GitHub repository structures
* Testing folder layouts
* Competitive programming templates
* Backend and frontend scaffolding
* Rapid prototyping

---

## Notes

* Use proper tree structure formatting
* Folder names should end with `/`
* Avoid invalid file names
* Restart terminal after installation

---

## Troubleshooting

### `f9` Command Not Recognized

* Restart the terminal
* Ensure PATH contains:

```text
C:\Users\<your-user>\AppData\Local\f9
```

Check using:

```bash
echo %PATH%
```

If missing, add it manually via Environment Variables.

---

### PATH Truncation Issues

Avoid using:

```bash
setx PATH
```

This may truncate long PATH values.

Use the installer instead, which safely updates the registry.

Also remove broken entries such as:

```text
C:\Users\<your-user>\AppDat
```

---

### Command Works Only with Full Path

Example:

```text
C:\Users\<your-user>\AppData\Local\f9\f9.bat
```

This means PATH is not configured correctly.

Add the folder to PATH manually or re-run the installer.

---

### Permission Issues

* Run terminal as Administrator if needed
* Ensure write access to the target directory

---

### Incorrect Structure Creation

Make sure the structure uses proper formatting:

* `├──`
* `│`
* `└──`

Folders should end with `/`

Avoid unnecessary spaces or invalid characters.

---

### Nothing Happens After Paste

Ensure you finish input using:

```text
CTRL + Z
ENTER
```

Without this, Windows will continue waiting for input.

---

### Python Not Installed

Verify Python installation:

```bash
python --version
```

If Python is not installed, install it before running the tool.

---

## Future Improvements

Planned enhancements include:

* Linux support
* macOS support
* JSON and YAML input support
* GUI version
* VS Code extension
* Template saving and reuse

---

## Contributing

Pull requests and improvements are welcome.

---

## Support

If this project is useful to you, consider giving it a star on GitHub.

---

## Author

F9

---

## License

MIT License

```
```
