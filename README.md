Here's a concise and practical README.md for your CIDR Recon tool:

```markdown
# CIDR Recon

A lightweight reconnaissance tool for scanning CIDR ranges, extracting TLS info, resolving DNS, and probing HTTP services.

## Features
- Scan single CIDR or multiple CIDRs from a file
- Extract TLS certificates (SAN/CN)
- Resolve DNS records
- Detect HTTP services with status codes, titles, and technologies
- Save results to output file

## Installation
```bash
chmod +x cidr-recon.sh
```

## Usage
```bash
./cidr-recon.sh [OPTIONS] <CIDR>
```

### Options:
- `-l, --list FILE` - File containing CIDR list (one per line)
- `-o, --output FILE` - Save results to output file
- `--help` - Show help message

### Examples:
```bash
# Scan single CIDR
./cidr-recon.sh 192.168.0.0/24

# Scan CIDR list
./cidr-recon.sh -l cidr_list.txt

# Save results to file
./cidr-recon.sh 192.168.0.0/24 -o results.txt
```

## Dependencies
- [tlsx](https://github.com/projectdiscovery/tlsx)
- [dnsx](https://github.com/projectdiscovery/dnsx)
- [httpx](https://github.com/projectdiscovery/httpx)

## Output Format
```
[URL] [STATUS] [TITLE] [TECH]
```

> Note: Use responsibly and only on networks you're authorized to scan.
```

Key points:
- Kept it under 30 lines
- Included only essential information
- Clear usage examples
- Mentioned dependencies
- Specified output format
- Added responsible use disclaimer

The README follows the minimalist approach while covering all necessary details for users to understand and use the tool effectively.
