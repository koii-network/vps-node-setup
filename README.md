# Koii VPS Node Setup Script

## Project Overview

This repository provides a comprehensive setup script for running a Koii Network Node on a Virtual Private Server (VPS). The script automates the process of preparing a Linux environment to run a Koii task node, including system updates, Docker installation, Node.js setup, and Koii CLI configuration.

The Koii Network is a decentralized computing platform that allows users to run tasks and earn rewards by contributing computational resources. This script simplifies the node deployment process for developers and network participants.

## Hardware Requirements

### Minimal Setup
- Processor: 1+ GHz 
- RAM: 2 GB
- Storage: 10 GB SSD
- OS: 64-bit Linux (Ubuntu 24.04 LTS recommended)
- Network: Stable internet connection

### Recommended Setup
- Processor: 2+ GHz multi-core
- RAM: 8 GB
- Storage: 30 GB SSD
- Network: 10+ Mbps upload/download speeds
- OS: 64-bit Linux (Ubuntu 24.04 LTS)

## Getting Started

### Prerequisites
- A VPS running Ubuntu 24.04 LTS
- SSH access to the VPS
- Basic command-line knowledge

### Installation Steps

1. SSH into your VPS
2. Clone this repository
   ```bash
   git clone <repository-url>
   cd koii-vps
   ```

3. Make the setup script executable
   ```bash
   chmod +x setupServer.sh
   ```

4. Run the setup script
   ```bash
   ./setupServer.sh
   ```

## Features / Capabilities

The setup script provides the following key functions:
- System update and upgrade
- Docker and Docker Compose installation
- Node.js (via nvm) installation
- Koii CLI installation
- Automatic Koii wallet creation
- Docker-based Koii task node deployment

## Project Structure

- `setupServer.sh`: Main installation and configuration script
- `docker-compose.yaml`: Docker Compose configuration for the Koii task node
- `.env-local`: Environment configuration file
- `README.md`: Project documentation

## Usage Instructions

The script offers an interactive menu with six options:
1. Update and upgrade system
2. Install Docker and Docker Compose
3. Install nvm and Node.js
4. Install Koii CLI and create a wallet
5. Run Docker Compose
6. Run all steps in sequence

### Important Notes
- You may need to update your PATH when prompted
- Use Finnie wallet to fund your newly created Koii wallet
- Restart the terminal if you encounter path-related issues

## Technologies Used

- Bash scripting
- Docker
- Docker Compose
- Node.js (via nvm)
- Koii Network CLI

## Reward Management

To claim rewards or manage your Koii tasks, use the Koii Task CLI:
```bash
npx @_koii/create-task-cli@latest
```

Key commands:
- Claim Rewards
- Withdraw Staked Funds

## Troubleshooting

- Ensure all manual steps are completed
- Restart the terminal after installing Docker and Koii CLI
- Check Docker logs: `docker logs -f --tail 10 task_node`
- Stop the node: `docker stop task_node`

## Disclaimer

⚠️ This script is under active development. Some manual intervention may be required.

## License

[Specify the license type, e.g., MIT, Apache 2.0]

## Resources

- [Koii Network Documentation](https://www.koii.network/docs)
- [Koii Task CLI Guide](https://www.koii.network/docs/develop/command-line-tool/create-task-cli/install)