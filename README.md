# 📡 another-sender

**another-sender** is a command-line tool for sending command files over UDP (SPI and I2C coming soon). Designed for embedded development, hardware testing, and automation workflows.

---

## ✨ Features

- 📂 Command file folder selection
- 🧠 Configurable parser types: `text`, `hex`, `json`
- 🔧 Adjustable delay between lines
- 🌐 UDP communication support (SPI/I2C extensible)
- 💾 Persistent configuration via `command.meta.json` and `udp_config.json`
- 🧼 Clean CLI interface with interactive menus

---

## 🚀 Installation

```bash
pip install another-sender
```

Or for development:

```bash
git clone https://github.com/minipcb/another-sender.git
cd another-sender
pip install -e .
```

---

## 🛠 Usage

Launch the CLI:

```bash
another-sender
```

Or check the version:

```bash
another-sender --version
```

---

## 🧩 Menu Options

- `A` – Send all files in the selected folder
- `T` – Set delay (in seconds) between sending each line
- `C` – Change active command folder (`commands/`)
- `M` – Change communication mode (`UDP`, `SPI`, `I2C`)
- `P` – Change parser type (`text`, `hex`, `json`)
- Select a file number to send a specific file
- `Q` – Quit

---

## 🧾 Command File Format

Command files are plain text and support:
- Blank lines and `#` comments (ignored)
- Commands interpreted based on parser type

### Example (`text`)
```txt
# type: text
PING
RESET
START
```

### Example (`hex`)
```txt
01 FF A0 0D
02 00 3B
```

---

## 🔄 Persistent Config

Stored in:

- `command.meta.json`
  - Communication mode
  - Parser type
  - Command folder
- `udp_config.json`
  - IP address and port
  - Delay setting

---

## 📁 Folder Structure

```bash
commands/
├── default/
│   ├── INIT_SYSTEM.txt
│   ├── CMD_ALL.txt
```

---

## 📌 Roadmap

- [x] UDP Support
- [x] Multi-parser logic
- [x] Config metadata file
- [ ] SPI and I2C backend integration
- [ ] Rich-based TUI
- [ ] Batch mode (`--send <file>`)

---

## 📃 License

MIT License © 2025 Nolan Manteufel
