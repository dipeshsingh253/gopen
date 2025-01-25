# gopen: GitHub CLI Utility

`gopen` is a simple Python script that makes interacting with GitHub easier from the terminal. It allows you to open files in a repository, navigate to specific branches, highlight lines, or even compare branches without switching to the browser manually.

## Features
- Open the current file in GitHub.
- Highlight specific lines in a file.
- Compare branches or commits directly via GitHub.

## Installation

Follow these steps to install `gopen` and set it up for global use:

### 1. Download the Script
Clone the repository or download the `gopen.py` file manually:
```bash
curl -o ~/.local/bin/gopen https://raw.githubusercontent.com/dipeshsingh253/gopen/main/gopen
```

### 2. Make the Script Executable
Ensure the script has the correct permissions:
```bash
chmod +x ~/.local/bin/gopen
```

Ensure `~/.local/bin` is in your `PATH`. Add the following to your shell configuration file (e.g., `~/.bashrc` or `~/.zshrc`):
```bash
export PATH="$HOME/.local/bin:$PATH"
```

Reload your shell:
```bash
source ~/.zshrc  # or source ~/.bashrc
```

### 3. Verify Installation
Test if `gopen` is accessible:
```bash
gopen --help
```

## Usage

### Command Syntax
```bash
gopen [-h] [--branch BRANCH] [--line LINE] [--compare] [--base BASE] [--head HEAD] [file]
```

### Command Options
| Option              | Description                                                |
|---------------------|------------------------------------------------------------|
| `file`              | (Positional) File to open in GitHub.                       |
| `-h, --help`        | Show help message and exit.                                |
| `--branch BRANCH`   | Specify the branch to open (default: current branch).       |
| `--line LINE`       | Highlight a specific line in the file.                     |
| `--compare`         | Open a comparison view in GitHub.                          |
| `--base BASE`       | Specify the base branch for comparison (default: main/master). |
| `--head HEAD`       | Specify the head branch for comparison (default: current branch). |

### Examples
1. **Open a File in GitHub:**
   ```bash
   gopen README.md
   ```

2. **Open a File in a Specific Branch:**
   ```bash
   gopen README.md --branch develop
   ```

3. **Highlight a Specific Line in a File:**
   ```bash
   gopen README.md --line 42
   ```

4. **Compare Branches:**
   ```bash
   gopen --compare --base main --head feature-branch
   ```

## Contributions
Contributions, bug reports, and feature requests are welcome! Feel free to open an issue or submit a pull request.
