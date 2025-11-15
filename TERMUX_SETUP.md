# WEYN Tools - Termux Setup Guide

## Quick Installation for Termux (Android)

### Step 1: Update Termux
```bash
pkg update && pkg upgrade
```

### Step 2: Install Python and Git
```bash
pkg install python git
```

### Step 3: Install Required Python Packages
```bash
pip install requests beautifulsoup4
```

### Step 4: Clone and Run
```bash
# Clone your repository
git clone <your-repo-url>
cd <repo-name>

# Run the tool
python converter.py
```

## Features That Work on Termux
✅ All menu options fully functional
✅ Clear screen works perfectly
✅ Color-coded output
✅ File saving and loading
✅ Bulk processing
✅ Back navigation
✅ All 6 tools available

## Usage on Termux

### Navigation
- Use number keys (1-6) to select menu options
- Press 0 to exit
- Type 'y' or 'n' for yes/no prompts
- Press Enter to submit input

### Input Methods
- **Single line input**: Type and press Enter
- **Multi-line input**: 
  - Paste multiple lines
  - Press Enter twice to finish
- **Cancel**: Press Ctrl+C (volume down + C)

### File Access
All saved files will be in your current directory:
```bash
ls *.txt          # List all result files
cat tokens_*.txt  # View token files
rm *.txt          # Delete all result files
```

## Tips for Termux Users

1. **Use Hacker's Keyboard** for easier typing
2. **Enable storage access**: `termux-setup-storage`
3. **Copy results easily**: Long press to select text
4. **Run in background**: Use `tmux` or `screen`

## Troubleshooting

### "No module named 'requests'"
```bash
pip install requests beautifulsoup4
```

### "Permission denied"
```bash
chmod +x converter.py
./converter.py
```

### Can't paste text
- Use Termux's built-in paste feature
- Or type manually line by line

### Colors not showing
- Termux supports colors by default
- If colors don't work, try: `export TERM=xterm-256color`

## Advanced: Running in Background

To keep the tool running when you close Termux:

```bash
# Install tmux
pkg install tmux

# Start a tmux session
tmux new -s weyn

# Run the tool
python converter.py

# Detach: Press Ctrl+B, then D
# Reattach later: tmux attach -t weyn
```

## Quick Start Example

```bash
$ python converter.py

# Main menu appears
# Choose [2] Get Access Token

# Paste your accounts:
user@email.com|password123
+1234567890|mypass456
# Press Enter twice

# Results appear instantly!
# Save to file when prompted
```

## Performance on Android
- ✅ Fast processing
- ✅ Low battery usage
- ✅ Works offline (after installation)
- ✅ No root required

Enjoy using WEYN Tools on your Android device! 🚀
