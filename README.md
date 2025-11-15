# 🔧 WEYN - Facebook Tools Suite

```
 ██     ██ ███████ ██    ██ ███    ██
 ██     ██ ██       ██  ██  ████   ██
 ██  █  ██ █████     ████   ██ ██  ██
 ██ ███ ██ ██         ██    ██  ██ ██
  ███ ███  ███████    ██    ██   ████

    FACEBOOK TOOLS SUITE
```

A powerful command-line toolkit for Facebook account management. Perfect for **Termux (Android)**, Linux, Mac, and Windows!

## ✨ Features

🔹 **6 Powerful Tools in One**
1. Link to UID|Password Converter
2. Access Token Generator
3. Cookie Extractor
4. AppState Generator
5. C_USER Extractor
6. All-in-One Data Export

🔹 **User-Friendly Interface**
- Menu-driven navigation
- Back button on all screens
- Clear screen functionality
- Color-coded output
- Real-time progress

🔹 **Bulk Processing**
- Process multiple accounts at once
- Real-time success/fail indicators
- Auto-save to timestamped files

🔹 **Cross-Platform**
- Works on Termux (Android)
- Linux / Mac / Windows
- No root required

## 🚀 Quick Start

### On Termux (Android)
```bash
pkg update && pkg upgrade
pkg install python git
pip install requests beautifulsoup4
python converter.py
```

### On PC (Linux/Mac/Windows)
```bash
pip install requests beautifulsoup4
python converter.py
```

## 📖 How to Use

1. **Run the tool**
   ```bash
   python converter.py
   ```

2. **Select from menu** (1-6)
   - Each option has a specific purpose
   - Follow the on-screen instructions

3. **Input your data**
   - Format: `uid|password` for most tools
   - Paste multiple lines for bulk processing
   - Press Enter twice to start processing

4. **Save results**
   - Choose to save when prompted
   - Files saved with timestamps
   - Easy to copy and use

## 🛠️ Available Tools

### [1] Link to UID|Password Converter
Convert Facebook profile links to UID|password format
- Input: Facebook profile URLs
- Output: `uid|password`

### [2] Get Access Token
Generate Facebook access tokens
- Input: `uid|password`
- Output: Access tokens

### [3] Get Cookie
Extract Facebook session cookies
- Input: `uid|password`
- Output: Cookie strings

### [4] Get AppState
Generate Facebook appstate JSON
- Input: `uid|password`
- Output: AppState JSON

### [5] Get C_USER
Extract C_USER values
- Input: `uid|password`
- Output: C_USER values

### [6] Get All
Get everything in one go!
- Input: `uid|password`
- Output: Token + Cookie + AppState + C_USER

## 📝 Input Format

```
uid|password
```

**UID can be:**
- Email: `user@example.com|password`
- Phone: `+1234567890|password`
- Username: `john.doe|password`

## 💾 Output Files

Results are saved to timestamped files:
- `results.txt` - Link converter results
- `token_YYYYMMDD_HHMMSS.txt` - Access tokens
- `cookie_YYYYMMDD_HHMMSS.txt` - Cookie data
- `appstate_YYYYMMDD_HHMMSS.txt` - AppState JSON
- `c_user_YYYYMMDD_HHMMSS.txt` - C_USER values
- `all_YYYYMMDD_HHMMSS.txt` - Complete data

## 📱 For Termux Users

See [TERMUX_SETUP.md](TERMUX_SETUP.md) for detailed Android setup instructions.

**Quick Tips:**
- Use Hacker's Keyboard for easier typing
- Long-press to copy results
- Files save to your current directory

## 🔧 Dependencies

```bash
pip install requests beautifulsoup4
```

## 🎨 Features

✅ **Compact design** - minimal spacing  
✅ **Easy copy** - no tabs/indentation on results  
✅ **Clear sections** - "═══ COPY BELOW ═══" markers  
✅ Menu-driven interface  
✅ Back navigation  
✅ Bulk processing  
✅ Auto-save results  
✅ Real-time progress  
✅ Color-coded output  
✅ Cross-platform  
✅ Termux compatible  

## 📚 Documentation

- [TERMUX_SETUP.md](TERMUX_SETUP.md) - Termux installation guide
- [replit.md](replit.md) - Full documentation

## ⚠️ Security Note

- Keep your tokens and cookies secure
- Never share result files publicly
- For educational/personal use only
- Respect Facebook's terms of service

## 🤝 Credits

Developed by **WEYN DUMP**

Token generation functionality integrated from [yuennix/token_getter](https://github.com/yuennix/token_getter)

---

**Enjoy using WEYN Tools! 🚀**
