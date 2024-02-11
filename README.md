# Script Security TeleBot

A Telegram bot to scan and detect malicious code in user uploaded files, especially ZIP files and shell scripts.

## Getting started

### Requirements

- Python 3.x
- Install the required dependency with this command:
  ```bash
  pip install python-telegram-bot==13.15
  ```

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/RiProG-id/Script-Security-TeleBot.git
   ```

2. Enter the project's directory:
   ```bash
   cd Script-Security-TeleBot
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Replace `'BOT_TOKEN_ANDA'` in `main.py` with your Telegram bot token.

5. Run the bot:
   ```bash
   python main.py
   ```

## Bot command

- `/start`: Start the bot, sends a welcome message along with the source code link.
- Sending a document (ZIP or script shell) will trigger the bot to scan for malicious code.

## How it works

- The bot scans the ZIP file to find malicious code in the files inside.
- The bot checks the shell script for commands and patterns deemed hazardous. 

## Hazardous code detected

The bot scans for the following harmful codes:

- `rm -rf`: Force recursive deletion.
- `if=/dev/null`: Redirect input to null.
- `if=/dev/zero`: Redirect input to zero.
- `cmd erase`: Windows command to delete files.
- `apparmor`: A security framework for Linux.
- `setenforce`: Set the enforcement state for SELinux.
- `shred -f`: Shred the files.
- `ufw disable`: Disable Uncomplicated Firewall on Linux.
- `iptables -F`: Flush all iptables rules on Linux.
- `setfacl`: Set file access control on Linux.
- `/proc/sysrq_trigger`: Triggering action on the Linux kernel through `/proc/sysrq_trigger`.
- `:(){ :|:& };:`: Bomb fork, a dangerous shell function.
