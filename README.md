# Network Port Scanner GUI

A lightweight TCP port scanner with a graphical user interface built with Python and Tkinter.

## Features

- **Simple 3-field interface** – enter a target host, start port, and end port
- **Multi-threaded scanning** – up to 500 concurrent threads for fast results
- **Service identification** – automatically labels well-known ports (FTP, SSH, HTTP, HTTPS, MySQL, RDP, etc.)
- **Real-time progress** – progress bar and elapsed-time counter update live during a scan
- **Stop at any time** – cancel a running scan gracefully
- **Save results** – export discovered open ports to a `.txt` file
- **Cross-platform** – runs on Windows, macOS, and Linux

## Requirements

- Python 3.7 or newer
- Tkinter (included in the standard Python distribution; on Debian/Ubuntu install `python3-tk`)

No third-party packages are required.

--------------------------------------------
## Installation

```bash
git clone https://github.com/techtrainer20/nmap_portscan_gui.git
cd nmap_portscan_gui
```

## Usage

```bash
python portscanergui.py
```

1. Enter the **Target** – an IP address (e.g. `192.168.1.1`) or hostname (e.g. `scanme.nmap.org`).
2. Set the **Start Port** and **End Port** (defaults: `1` – `1024`).
3. Click **Start Scan**. Open ports appear in real time in the results pane.
4. Click **Stop** to cancel a scan early.
5. After a scan completes, click **Save Results** to write the open-port list to a text file.

## Detected Services

The following ports are automatically labelled:

| Port | Service   |
|------|-----------|
| 21   | FTP       |
| 22   | SSH       |
| 23   | Telnet    |
| 25   | SMTP      |
| 53   | DNS       |
| 80   | HTTP      |
| 110  | POP3      |
| 143  | IMAP      |
| 443  | HTTPS     |
| 3306 | MySQL     |
| 3389 | RDP       |
| 5900 | VNC       |
| 8080 | HTTP-Alt  |

Ports not in the list are reported as `Unknown`.

--------------------------------------------
## Project Structure

```
nmap_portscan_gui/
├── portscanergui.py   # Main application (scanner + GUI)
└── README.md
```

## Disclaimer

Use this tool only on hosts and networks you own or have explicit permission to scan. Unauthorized port scanning may be illegal in your jurisdiction.

----------------------------------------------------------------------------------------

# 🚀## Getting Started
Follow these instructions to get a local copy of the port scanner up and running.

Prerequisites
Language: Python 3.8+ (or your specific language)

Permissions: This tool requires administrative/root privileges to perform certain types of scans (e.g., ICMP or SYN scans).

Installation
Clone the repository

Bash
git clone https://github.com/yourusername/network-port-scanner.git
cd network-port-scanner
Set up a virtual environment (Optional but Recommended)

Bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
Install dependencies

Bash
pip install -r requirements.txt
Usage
To run a basic scan on a target IP or hostname:

Bash
# Basic scan (may require sudo on Linux/macOS)
sudo python main.py --target 192.168.1.1
Common Arguments:

-p, --ports: Specify a range (e.g., 1-1024).

-t, --type: Choose scan type (TCP, SYN, UDP).

-v, --verbose: Enable detailed output.

----------------------------------------------------------------------------------------

## License

This project is released under the [MIT License](https://opensource.org/licenses/MIT).

