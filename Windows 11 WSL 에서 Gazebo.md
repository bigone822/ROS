# 🚀 Windows 11 Pro WSLg에서 Gazebo 실행하기

1. WSL 업데이트

```powershell
wsl --update
wsl --shutdown
```

최신 WSLg 버전으로 업데이트해야 GUI 지원이 활성화됩니다.

2. Ubuntu 20.04에서 Gazebo 설치

```bash
sudo apt update
sudo apt upgrade -y
sudo apt install -y gazebo11 libgazebo11-dev
```

3. DISPLAY 환경변수 확인

WSLg에서는 자동으로 DISPLAY 변수가 설정됩니다. 확인해보세요:

```bash
echo $DISPLAY
```
보통 :0 형태로 잡혀 있으면 정상입니다.

4. Gazebo 실행

```bash
gazebo
```
