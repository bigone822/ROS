01
패키지 목록 업데이트
최신 패키지 정보를 가져와 설치 오류를 방지합니다.

터미널에서 실행

```
`bash
sudo apt update
sudo apt upgrade -y
```
02
Gazebo 저장소 추가
Gazebo 공식 패키지를 설치하기 위해 저장소를 등록합니다.

터미널에서 실행

sudo apt install wget -y

wget https://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -

sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable focal main" > /etc/apt/sources.list.d/gazebo-stable.list'

03
저장소 갱신
추가된 저장소를 반영하여 패키지 목록을 갱신합니다.

터미널에서 실행

sudo apt update

04
Gazebo 설치
핵심 단계
원하는 버전의 Gazebo를 설치합니다.

터미널에서 실행

최신 버전 설치: sudo apt install gazebo11 -y

개발 라이브러리 포함 설치: sudo apt install libgazebo11-dev -y

05
설치 확인
Gazebo가 정상적으로 실행되는지 확인합니다.

터미널에서 실행

gazebo

GUI가 실행되면 설치 성공
