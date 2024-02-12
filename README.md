# kagami

A Telegram bot to scan and detect malicious code in user uploaded files, especially ZIPs and shell scripts.

## Getting started

### Requirements

- Python 3.x
- python-telegram-bot==13.15

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/fukiame/kagami.git
   ```

2. Enter the project's directory:
   ```bash
   cd kagami
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Replace `'PLACE_BOT_TOKEN_HERE'` in `main.py` with your Telegram bot token.

5. Run the bot:
   ```bash
   python main.py
   ```

## Bot command

- `/start`: Start the bot.

## How it works

- The bot scans user uploaded ZIP files and scripts to find malicious code.
