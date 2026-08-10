# 1. WSL에 Ubuntu 20.04 설치

ROS Noetic을 쓰려면 반드시 Ubuntu 20.04 (focal)가 필요합니다.

PowerShell에서:

```powershell
wsl --install -d Ubuntu-20.04
```
또는 Microsoft Store에서 Ubuntu 20.04 LTS를 직접 설치하세요.


# 2. 새 Ubuntu 20.04 환경에서 ROS Noetic 설치

앞서 말씀드린 키 등록 및 저장소 추가 과정을 다시 진행하면 됩니다:


```bash
sudo apt update
sudo apt install curl gnupg2 lsb-release -y

curl -sSL 'http://keyserver.ubuntu.com/pks/lookup?op=get&search=0xC1CF6E31E6BADE8868B172B4F42ED6FBAB17C654' \
| gpg --dearmor | sudo tee /usr/share/keyrings/ros-archive-keyring.gpg > /dev/null

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros/ubuntu focal main" \
| sudo tee /etc/apt/sources.list.d/ros-latest.list

sudo apt update
sudo apt install ros-noetic-desktop-full

```
