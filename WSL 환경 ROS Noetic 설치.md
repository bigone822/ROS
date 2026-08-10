# 🔑 ROS Noetic 설치 절차 (Ubuntu 20.04 focal)

ROS Noetic을 쓰려면 반드시 Ubuntu 20.04 (focal)가 필요합니다.

PowerShell에서:

```powershell
wsl --install -d Ubuntu-20.04
```
또는 Microsoft Store에서 Ubuntu 20.04 LTS를 직접 설치하세요.

1. 필수 패키지 설치
```bash
sudo apt update
sudo apt install curl gnupg2 lsb-release -y
```

2. ROS 키 등록

```bash
curl -sSL 'http://keyserver.ubuntu.com/pks/lookup?op=get&search=0xC1CF6E31E6BADE8868B172B4F42ED6FBAB17C654' \
| gpg --dearmor | sudo tee /usr/share/keyrings/ros-archive-keyring.gpg > /dev/null
```

3. APT 저장소 추가

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros/ubuntu focal main" \
| sudo tee /etc/apt/sources.list.d/ros-latest.list
```

4. 업데이트 후 설치

``` bash
sudo apt update
sudo apt install ros-noetic-desktop-full
```

5. 환경 변수 설정

``` bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

## 설치확인

``` bash
rosversion -d
```
