# CIDR Recon Tool

A simple yet effective automation script for performing basic reconnaissance on CIDR ranges, designed for bug bounty hunters and penetration testers.

## Description

This tool performs a quick reconnaissance pipeline on a given CIDR range by:

1. Extracting TLS certificate information (SAN, Common Name)
2. Resolving DNS records for discovered hosts
3. Probing HTTP services to gather status codes, page titles, and technology stack

The tool follows the KISS principle (Keep It Simple, Stupid) and does one thing well without unnecessary complexity.

## Features

- Lightweight and fast reconnaissance pipeline
- Minimal dependencies (just the required tools)
- Basic input validation
- Clear progress indicators
- Designed to chain with other tools in your workflow

## Installation

1. Ensure you have the required tools installed:
   - [tlsx](https://github.com/projectdiscovery/tlsx)
   - [dnsx](https://github.com/projectdiscovery/dnsx)
   - [httpx](https://github.com/projectdiscovery/httpx)

2. Clone this repository or download the script:
   ```bash
   git clone https://github.com/0xaRY4/cidr-recon.git
   cd cidr-recon
   ```

3. Make the script executable:
   ```bash
   chmod +x cidr-recon.sh
   ```

## Usage

Basic usage:
```bash
./cidr-recon.sh <CIDR>
```

Example:
```bash
./cidr-recon.sh 192.168.0.0/24
```

Show help:
```bash
./cidr-recon.sh --help
```
