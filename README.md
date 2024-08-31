<p align=left>
	<a href="https://discord.gg/zHafSd3bTw">
		<img src="https://discordapp.com/api/guilds/1196915612522393651/widget.png?style=banner2" alt="Discord Banner 2"/> 
	</a>
</p>

## About
[Moonlight for Tizen](https://moonlight-stream.org) is an open-source client for NVIDIA GameStream and [Sunshine](https://github.com/LizardByte/Sunshine). It enables streaming games from a powerful desktop to Samsung Smart TVs running Tizen OS 5.5 or higher. For more details, setup guides, or troubleshooting, visit the [Moonlight wiki](https://github.com/moonlight-stream/moonlight-docs/wiki).

This fork simply just disables gamemode unlike Kyro and OneLiberty forks. If you wish to use gamemode while streaming, please use either of those forks.

### Note
As a non-developer with limited coding knowledge, I do my best to maintain the repository and address issues. If you encounter problems, please report them in the issue section. While I can't guarantee a solution, I will certainly investigate.

THIS FORK IS BASED ON OneLiberty Moonlight port. All my fork does is simply disable gamemode on launch/stream. My reason is that it's simply too bright for my eyes.

## Getting Started
To install Moonlight on your Samsung Smart TV, start by ensuring your setup meets the [Prerequisites](https://github.com/OneLiberty/moonlight-chrome-tizen#prerequisites) and follow the [Installation](https://github.com/OneLiberty/moonlight-chrome-tizen#installation) guide.

## Read the pinned issue before getting started: https://github.com/MrPhaze62/moonlight-chrome-tizen-no-gamemode/issues/1

### Prerequisites
You'll need:
- Windows Subsystem for Linux (WSL 2) — [Installation Guide](https://learn.microsoft.com/en-us/windows/wsl/install-manual)
- Docker Desktop — [Installation Guide](https://docs.docker.com/desktop/)
Ensure Docker Desktop is running and close any resource-intensive applications.

### Installation
1. **Enable Developer Mode on Samsung Smart TV**:
   - Navigate to `Apps` panel, enter `12345` on the remote, turn on `Developer mode`, input your PC's IP, and restart the TV.
2. **Launch Docker Image**:
   - Run in Windows PowerShell:
     ```
     docker run -it --rm ghcr.io/mrphaze62/moonlight-chrome-tizen-no-gamemode:samsung_wasm
     ```
3. **Install the Application**:
   - Connect and install via Smart Development Bridge:
     ```
     sdb connect YOUR_TV_IP
     sdb devices
     tizen install -n Moonlight.wgt -t YOUR_DEVICE_ID
     exit
     ```
   - Replace `YOUR_TV_IP` and `YOUR_DEVICE_ID` with your TV's IP and Device ID respectively.

4. **(Optional) Disable Developer Mode**:
   - Revisit the `Apps` panel to turn off Developer mode and restart the TV.

Moonlight should now be available under `Recent Apps` on your Samsung Smart TV.

### Updating
To update Moonlight:
1. Delete the existing app from your TV.
2. Follow the installation instructions to install the latest version.

## Changelogs
View changes and updates in the [CHANGELOG](https://github.com/oneliberty/moonlight-chrome-tizen/blob/samsung_wasm/CHANGELOG.md).

## Contributing
Contributions are welcome! Fork the repo, create pull requests, or open issues. If you find the project useful, consider giving it a star!

## Credits
- Moonlight for Chrome OS is developed and maintained by [Moonlight Developers](https://github.com/moonlight-stream/moonlight-chrome)
- Moonlight for Tizen is based on Chrome OS version which was then adapted and powered by [Samsung Developers](https://github.com/SamsungDForum/moonlight-chrome)
- Dockerfile have been readapted by [pablojrl123](https://github.com/pablojrl123/moonlight-tizen-docker)
- Thanks to [henry2fa](https://github.com/henryfa2) for the discord and more. 
