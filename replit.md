# WEYN - Facebook Tools Suite

## Overview
This is a Python CLI tool suite for Facebook account management. It combines multiple tools:
1. **Link to UID|Password Converter** - Converts Facebook profile links to UIDs with custom password
2. **Access Token Generator** - Generates Facebook access tokens from credentials
3. **Cookie Generator** - Extracts Facebook session cookies
4. **AppState Generator** - Generates Facebook appstate JSON
5. **C_USER Generator** - Extracts C_USER values from accounts

Perfect for **Termux (Android)**, Linux, Mac, and Windows!

## Project Structure
- `converter.py` - Main Python script with menu-driven interface
- `.gitignore` - Git ignore file for Python projects
- `pyproject.toml` - Python project configuration
- `uv.lock` - Dependency lock file

## Dependencies
- Python 3.12+
- requests - HTTP library for making web requests
- beautifulsoup4 - HTML parsing library

## How to Use

### Running the Tool
1. Run the program: `python converter.py`
2. Select an option from the main menu (1-6)
3. Follow the prompts for your chosen tool
4. Use the back option to return to main menu
5. Press 0 to exit

### Menu Options
- **[1] Link to UID|Password Converter**
  - Enter a custom password
  - Paste Facebook profile links (one per line)
  - Get formatted `uid|password` results
  
- **[2] Get Access Token**
  - Paste accounts in `uid|password` format
  - Press Enter twice when done
  - Get access tokens for each account
  
- **[3] Get Cookie**
  - Same input format as above
  - Extracts full cookie strings
  
- **[4] Get AppState**
  - Same input format
  - Generates appstate JSON for each account
  
- **[5] Get C_USER**
  - Same input format
  - Extracts c_user values
  
- **[6] Get All**
  - Gets Token + Cookie + AppState + C_USER in one go
  - Complete data export for each account

### For Termux Users
This tool works perfectly on Termux! Install and run:
```bash
pkg update && pkg upgrade
pkg install python git
pip install requests beautifulsoup4
git clone <your-repo-url>
cd <repo-name>
python converter.py
```

## Features
- **Compact Interface**: Minimal spacing, maximum efficiency
- **Easy Copy**: Results without tabs/indentation for instant copying
- **Clear Copy Sections**: "═══ COPY BELOW ═══" markers for easy selection
- **Menu-Driven**: Quick navigation with numbered options
- **Back Navigation**: Return to main menu from any tool
- **Bulk Processing**: Process multiple accounts at once
- **Real-time Progress**: See results as they're processed
- **Auto-Save**: Option to save results to timestamped files
- **Cross-Platform**: Works on Termux, Linux, Mac, Windows
- **Color-Coded Output**: Easy-to-read colored terminal output

## Input Formats

### Link to UID Converter
- Enter any Facebook profile URL:
  - `https://www.facebook.com/username`
  - `https://m.facebook.com/username`
  - `https://facebook.com/profile.php?id=123456`
  - One link per line
  - Press Enter on blank line to finish

### Token/Cookie/AppState Generators
- Format: `uid|password`
- UID can be email, phone, or username
- Examples:
  - `user@example.com|password123`
  - `+1234567890|mypass`
  - `john.doe|secretpass`
- Paste multiple accounts (one per line)
- Press Enter twice to process

## Output Files
All results can be saved to timestamped files:
- Link converter: `results.txt` (or custom name)
- Token generator: `token_YYYYMMDD_HHMMSS.txt`
- Cookie generator: `cookie_YYYYMMDD_HHMMSS.txt`
- AppState generator: `appstate_YYYYMMDD_HHMMSS.txt`
- C_USER generator: `c_user_YYYYMMDD_HHMMSS.txt`
- All data: `all_YYYYMMDD_HHMMSS.txt`

## Technical Details
- **Link to UID Converter**: Uses web scraping with BeautifulSoup
- **Token Generators**: Uses Facebook's b-api authentication endpoint
- **Smart URL Handling**: Auto-converts URLs to mbasic format
- **Session Management**: Maintains sessions for efficient requests
- **Error Handling**: Catches network errors and invalid credentials
- **Termux Compatible**: Uses `clear` command (works on Android)

## Recent Changes
- 2025-11-15: Major Enhancement - Combined Tools Suite
  - Added menu-driven interface with 6 options
  - Integrated token/cookie/appstate generators from yuennix/token_getter
  - Added back navigation to all tools
  - Implemented clear screen functionality
  - Made fully compatible with Termux
  - Added option to get all data at once
  - Color-coded interface for better UX
  - Timestamped file saves for all tools

- 2025-11-15: UI/UX improvements
  - Changed banner color to purple
  - Added colored output for better readability
  - Added "ALL RESULTS (Easy Copy)" sections
  - Improved error messages
  
- 2025-11-15: Initial project setup in Replit
  - Installed Python dependencies (requests, beautifulsoup4)
  - Set up CLI workflow
  - Created documentation

## Notes
- This is a command-line tool (CLI/TUI)
- No frontend or backend server required
- Runs in console output mode
- All results can be saved to text files
- Perfect for bulk account management
- Works great on mobile (Termux) and desktop

## Troubleshooting

### On Termux
- **"No module named 'requests'"**: Run `pip install requests beautifulsoup4`
- **Permission denied**: Make executable with `chmod +x converter.py`

### General
- Press `Ctrl+C` to cancel at any time
- Type back options to return to menu
- Check your network connection if login fails
- Invalid credentials will show specific error messages

## Security Notes
- Never share your access tokens or cookies publicly
- Keep result files secure
- This tool is for educational/personal use
- Respect Facebook's terms of service
