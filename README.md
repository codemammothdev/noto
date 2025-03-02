# Noto - Simple Command Line Note-Taking Tool

Noto is a lightweight command-line tool for quickly creating and organizing markdown notes. Notes are automatically timestamped and organized chronologically in your Documents folder.

## Features

- Create markdown notes with a single command
- Automatic timestamping for chronological organization
- Automatic opening in VS Code for immediate editing
- Works on macOS and Linux
- Preserves original capitalization in note headers
- Uses lowercase with underscores for consistent file naming
- Organizes notes in daily subfolders for better management

## Installation

1. Clone this repository or download the `noto` script
2. Make the script executable (if not already):
   ```
   chmod +x noto
   ```
3. Move the script to a directory in your PATH:
   ```
   sudo mv noto /usr/local/bin/
   ```
   
   Alternatively, you can add the script's directory to your PATH in your shell profile file.

## Usage

```
noto My Note Title
```

This will:
1. Create a new markdown file in a daily subfolder with the format `~/Documents/noto/YYYY_MM_DD/HH_MM_SS_my_note_title.md`
2. Add a title header with original capitalization ("# My Note Title") and timestamp to the file
3. Open the file in VS Code for editing

## Requirements

- Bash shell (standard on macOS and Linux)
- VS Code with the `code` command installed in PATH
  - To install the `code` command, open VS Code and press `Cmd+Shift+P` (macOS) or `Ctrl+Shift+P` (Linux)
  - Type "shell command" and select "Install 'code' command in PATH"

## File Structure

Notes are saved in daily subfolders within `~/Documents/noto/` with filenames that ensure chronological ordering:

```
~/Documents/noto/
  ├── 2023_05_10/
  │   ├── 09_20_45_meeting_notes.md
  │   └── 14_30_12_project_ideas.md
  ├── 2023_05_11/
  │   └── 08_30_22_daily_tasks.md
  └── ...
```

## Customization

You can modify the script to change:
- The base directory for notes
- The date and time formats
- The template for new notes
- The editor used to open notes 