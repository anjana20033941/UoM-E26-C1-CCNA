# Cisco IOS Command Modes Overview

Cisco IOS devices use different command modes depending on the task being performed.

### 1. User EXEC Mode (`Switch>`)
- **Purpose**: Used for basic device status monitoring and limited operational commands.
- **Capabilities**: Ping, traceroute, basic device inspection. No configuration changes allowed.

### 2. Privileged EXEC Mode (`Switch#`)
- **Purpose**: Used for detailed status verification, system configuration backups, and troubleshooting.
- **Capabilities**: Access to all `show` commands (e.g., `show running-config`), rebooting the device, and navigating to higher configuration modes.
- **Command to Enter**: `enable`
- **Command to go back to User ExEC mode**: `disable`

### 3. Global Configuration Mode (`Switch(config)#`)
- **Purpose**: Used to make global changes that affect the entire device operation.
- **Capabilities**: Changing device hostnames, setting banner messages, configuring global passwords, etc.
- **Command to Enter**: `configure terminal`

### 4. Subconfiguration Modes
Used to configure specific parts, features, or ports on the Cisco device.

* **Line Configuration Mode (`Switch(config-line)#`)**
  - **Purpose**: Configure access security for Console, SSH, Telnet, or AUX ports.
  - **Command to Enter**: `line console 0` or `line vty 0 15`

* **Interface Configuration Mode (`Switch(config-if)#`)**
  - **Purpose**: Configure specific network ports or virtual interfaces (Assigning IP addresses, enabling ports with `no shutdown`).
  - **Command to Enter**: `interface gigabitethernet 0/0` (or `interface vlan 1`)
