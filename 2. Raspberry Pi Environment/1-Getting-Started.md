# Raspberry Pi Getting Started

## Operating System Setup

1. Download [Raspberry Pi Imager](https://www.raspberrypi.com/documentation/computers/getting-started.html#raspberry-pi-imager)
2. Choose Device :arrow_right: Choose OS ➡️ Choose Storage
3. Set up additional settings by clicking `Edit Settings` and fill in the following information:
    - General Tab
        - `Set hostname`: `raspberrypi.local`
        - `Set username and password`:
            - `Username`:
            - `Password`:
        - `Configure wireless LAN`:
            - `SSID`:
            - `Password`:
    - Services Tab
        - ✅ `Enable SSH`
        - Check 🔵 `Allow public-key authentication only`
        - Fill the form with the `id_rsa.pub` public key from the `.ssh` folder (available in Windows, macOS, or Linux)
    - Options Tab
        - ✅ Eject media when finished
        - ✅ Enable telemetry

## Headless Connection

1. After installing the operating system, connect the Raspberry Pi headless without using any peripherals attached to the Raspberry Pi. Only insert the microSD card and power on the Raspberry Pi.
2. Log in headless via SSH through PowerShell in Windows or Terminal in macOS or Linux using the command:
   ```bash
   ssh {username}@raspberrypi.local
   ```
3. Before performing any updates, check the IP address connected to the Raspberry Pi by typing the command:
   ```bash
   hostname -I
   ```
   Take note of the IP address that typically starts with `192.168.x.x`, since after the update, connecting via SSH in step 2 will not work.
4. Update the system using the following commands:

    ```bash
    sudo apt update
    sudo apt upgrade -y
    ```

   The system will then automatically reboot.

5. Connect again using SSH, but this time use the IP address by typing the command:
   ```bash
   ssh {username}@{ip_address}
   ```

## Enable VNC Desktop

1. To use desktop mode remotely via [Real-VNC](https://www.realvnc.com/en/connect/download/viewer/), set up as follows:

    ```bash
    sudo raspi-config
    ```

    - Choose Interface Options and enable VNC. The system will then automatically reboot.

2. After the reboot, enter the IP address and name information in the VNC client.

   **Note:** This will only work if your desktop/laptop is connected to the same network as the Raspberry Pi. A solution using a Virtual Private Network (VPN) will be explained in `2-Setup-VPN-Tailscale.md`, which allows both devices to be connected even when they are not on the same network.