# Docker Short Commands

A comprehensive collection of shortcut commands to simplify your Docker workflow. This script installs short, easy-to-remember aliases and helper scripts into your system path.

## 📝 Prerequisites
- Linux/Unix Environment
- Docker installed and running
- `curl` or `wget` (for installation)
- Root/Sudo privileges (for installation)

## 🚀 Features
- **Simplified Commands**: Replace long Docker commands with 3-4 letter shortcuts.
- **Enhanced Output**: Custom formatting for `docker ps` and `docker inspect`.
- **Safety**: Scripts are installed with proper permissions (`755`).
- **Management**: Easy install, uninstall, and update mechanisms.
- **Self-Documenting**: Built-in `dhp` command to list all available shortcuts.

## 📦 Available Commands

| Command | Description | Equivalent Docker Command / Function |
|---------|-------------|--------------------------------------|
| `dhp` | **Help** | **Lists all installed commands** |
| `dpl` | Pull image | `docker pull` |
| `dis` | List images | `docker images` |
| `drn` | Run container | `docker run` |
| `dps` | List all containers | `docker ps -a` |
| `dpe` | List exited containers | `docker ps -a -f "status=exited"` |
| `dhc` | Healthcheck status | Custom script to show container health status |
| `dpp` | List ports | Show container ID, Names, and Ports |
| `dpi` | List running summary | Show ID, Time, Status, Image, Names |
| `dpia` | detailed list | Show Names, ID, Status, Ports, Image, Command, Time |
| `dsp` | Stop container | `docker stop` |
| `dst` | Start container | `docker start` |
| `drt` | Restart container | `docker restart` |
| `dre` | Rename container | `docker rename` |
| `dec` | Exec (bash) | `docker exec -it <container> /bin/bash` |
| `decx` | Exec (sh) | `docker exec -it <container> /bin/sh` |
| `dls` | Logs (tail) | `docker logs --tail 20 -f` |
| `drm` | Remove container | `docker rm -f` |
| `dri` | Remove image | `docker rmi -f` |
| `dit` | Inspect | `docker inspect` |
| `ditj` | Inspect (JSON) | `docker inspect --format "{{json .Config}}"` |
| `dvl` | List volumes | `docker volume ls` |
| `dss` | Stats | `docker stats` |
| `drs` | Remove stopped | Remove all exited containers |
| `dhy` | History | `docker history` |
| `ddi` | Remove dangling | Remove all dangling images |
| `drntest`| Run test container | `docker run -itd --name=test ...` |
| `dup` | Compose Up | `docker compose up -d` (supports profiles) |
| `ddown` | Compose Down | `docker compose down` (supports profiles) |


## 📥 Installation

You can install the commands using one of the following methods:

### Method 1: Direct Install (Linux/WSL2/macOS)

**Using wget:**
```bash
bash <(wget -qO- https://raw.githubusercontent.com/meibraransari/Docker-Short-Command/main/docker_short_command.sh) | sudo bash -s install
```

**Using curl:**
```bash
bash <(curl -s https://raw.githubusercontent.com/meibraransari/Docker-Short-Command/main/docker_short_command.sh) | sudo bash -s install
```

### Method 2: Download First (Works on Windows/Git Bash)

If you encounter the error `bash: /proc/self/fd/xx: No such file or directory`, use this method:

**Using wget:**
```bash
wget https://raw.githubusercontent.com/meibraransari/Docker-Short-Command/main/docker_short_command.sh -O docker_short_command.sh
sudo bash docker_short_command.sh install
```

**Using curl:**
```bash
curl -fsSL https://raw.githubusercontent.com/meibraransari/Docker-Short-Command/main/docker_short_command.sh -o docker_short_command.sh
sudo bash docker_short_command.sh install
```

### Method 3: Pipe to Bash (Alternative)

```bash
curl -fsSL https://raw.githubusercontent.com/meibraransari/Docker-Short-Command/main/docker_short_command.sh | sudo bash -s install
```

> [!NOTE]
> **Windows Users:** Process substitution `<(...)` doesn't work in Git Bash on Windows. Use **Method 2** or **Method 3** instead.

> [!TIP]
> Running the script without arguments will open an interactive menu where you can choose to Install, Uninstall, Help, or Update.

## 🔄 Update

To update your scripts to the latest version found in the repository:

```bash
sudo docker_short_command.sh update
```
*(Note: Since the script itself isn't installed to bin, you might need to re-run the curl/wget command or keep the script locally)*

If you have the script saved locally:
```bash
sudo ./docker_short_command.sh update
```

## 🗑️ Uninstall

To remove all shortcuts and cleanup your system:

```bash
sudo ./docker_short_command.sh uninstall
```

## 🛠️ Usage Examples

**Docker Short Command Help:**
```bash
dhp
```

**Enter a container's shell:**
```bash
dec my-container-name
decx my-container-name
```

**View JSON configuration of a container:**
```bash
ditj my-container-name
```

**Start a specific profile in docker compose:**
```bash
dup my-profile
```


---

## 🧠 About This Project

**Made with ❤️ for DevOps Engineers** 

Powered by **DevOps In Action**, this repository offers **real-world, hands-on DevOps setups** for CI/CD pipelines, containerization, Kubernetes, cloud platforms (AWS, GCP, Azure), and infrastructure at scale.

## 📝 License

This guide is provided as-is for educational and professional use.

## 🤝 Contributing

Feel free to suggest improvements or report issues.


### 💼 Connect with Me 👇😊

*   🔥 [**YouTube**](https://www.youtube.com/@DevOpsinAction?sub_confirmation=1)
*   ✍️ [**Blog**](https://ibraransari.blogspot.com/)
*   💼 [**LinkedIn**](https://www.linkedin.com/in/ansariibrar/)
*   👨‍💻 [**GitHub**](https://github.com/meibraransari?tab=repositories)
*   💬 [**Telegram**](https://t.me/DevOpsinActionTelegram)
*   🐳 [**Docker Hub**](https://hub.docker.com/u/ibraransaridocker)

### ⭐ If You Found This Helpful...

***Please star the repo and share it! Thanks a lot!*** 🌟
