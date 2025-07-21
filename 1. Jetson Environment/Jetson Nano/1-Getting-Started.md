# Jetson Nano Getting Started

## Operating System Setup

1. Download latest JetPack 4.6.1 from this [link](https://developer.nvidia.com/embedded/jetpack-sdk-461)
2. Flash SD Card using [balenaEtcher](https://etcher.balena.io/)

## Setup Command

### a. Initial Setup

```bash
sudo apt-get update
sudo apt-get -y upgrade
sudo apt install curl
```

### b. Python Setup

```bash
sudo apt install python3-pip
sudo apt install python-pip
```

### c. Jetson Stats

```bash
sudo -H pip3 install -U jetson-stats
```
