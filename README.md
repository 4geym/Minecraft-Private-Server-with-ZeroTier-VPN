# Minecraft Server with ZeroTier VPN

## Project Description
This project is a gaming infrastructure based on a mini-PC running Ubuntu. 
I set up a Minecraft server, ensured secure connectivity via ZeroTier, automated the server startup using systemd, and integrated player activity monitoring.

## Technologies Used
- **OS:** Ubuntu
- **Networking:** ZeroTier
- **Automation:** systemd (systemctl)
- **Monitoring:** Plan-Player-Analytics
- **Game Server:** Minecraft

## Key Features
- **Minecraft server on Ubuntu with automatic startup via systemd**
- **Friend connection through a virtual local network (ZeroTier)**
- **Two servers running on the same IP but different ports**
- **Player activity and server load monitoring via web interface (Plan-Player-Analytics)**
- **Automatic server restart in case of crashes or PC reboots**

## Installation and Setup (Brief Overview)
### 1. Installing ZeroTier and Creating a Network
- Installed ZeroTier on the server and client PCs.
- Created a virtual local network and manually added users to the pool.
- Assigned an IP address to the server.

### 2. Running the Minecraft Server
- Installed and launched Minecraft server.
- Configured two servers on different ports.
- Added the **Plan-Player-Analytics** plugin for monitoring.

### 3. Automating Server Startup with systemd
Created a systemd service for automatic Minecraft server startup:
```
sudo systemctl enable minecraft-server
sudo systemctl start minecraft-server
```
Now, the server restarts automatically in case of crashes or after a system reboot.

## Conclusion and Future Improvements
The server runs stably, friends can connect, and I don’t have to worry about failures. Possible future improvements include:
- **Automatic world backups (e.g., using cron + rsync)**

---

This project was created for personal use to enjoy gaming with friends. 🎮
