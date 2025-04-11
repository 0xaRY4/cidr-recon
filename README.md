# CIDR Recon Tool

![Requirements](https://img.shields.io/badge/dependencies-tlsx,dnsx,httpx-green)

A lightweight reconnaissance pipeline for security professionals to quickly scan CIDR ranges.

##  Features

- Single-command CIDR reconnaissance
- TLS certificate extraction (SAN/CN)
- DNS resolution pipeline
- HTTP service detection
- Clean, parseable output

##  Installation

1. Install dependencies:
```bash
go install github.com/projectdiscovery/tlsx/cmd/tlsx@latest
go install github.com/projectdiscovery/dnsx/cmd/dnsx@latest
go install github.com/projectdiscovery/httpx/cmd/httpx@latest
```

2. Download the script:
```bash
wget https://raw.githubusercontent.com/0xaRY4/cidr-recon/main/cidr-recon.sh
chmod +x cidr-recon.sh
```

## 🛠 Usage

```bash
./cidr-recon.sh [OPTIONS] <INPUT>
```

### Basic Usage
| Command | Description |
|---------|-------------|
| `./cidr-recon.sh 192.168.1.0/24` | Scan single CIDR |
| `./cidr-recon.sh -l cidrs.txt` | Scan CIDR list |
| `./cidr-recon.sh -l cidrs.txt -o results.txt` | Save output |

### Options
| Flag | Description |
|------|-------------|
| `-l` | File containing CIDR list |
| `-o` | Output file |
| `--help` | Show help message |

## 📝 Example Output

```
https://example.com 200 Welcome [nginx,php]
http://test.site 301 Redirect [apache]
```

## 📌 Dependencies

- [tlsx](https://github.com/projectdiscovery/tlsx)
- [dnsx](https://github.com/projectdiscovery/dnsx)
- [httpx](https://github.com/projectdiscovery/httpx)
