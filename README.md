#사전 작업
우분투 설치 [https://github.com/varteam/Install-Ubuntu14.04]

# Install-Docker-On-Ubuntu
우분투에 Docker 를 설치하는 방법

우분투에 ssh 접속

    sudo apt-get update
    sudo apt-get upgrade
    reboot
    
    
    //after reboot
    wget -qO- https://get.docker.com/ | sh

위와 같이 설치를 하게 되면 Ubuntu 의 버전과 관계 없이 알아서(?) 설치되는 스크립트가 실행된다.

설치가 완료되면

    sudo usermod -aG docker <계정ID>
    exit
    //재 로그인을 해야 한다.

를 하게 되면 해당 계정에서는 docker 를 sudo 없이 사용할 수 있다.

결과 확인 방법

    //버전확인
    (sudo) docker -v
    Docker version 1.5.0, build a8a31ef    //04.08 에 설치한 최신 버전
    
    //테스트
    Docker run hello-world
    
자동으로 이미지를 다운 받고 컨테이너를 생성해서 명령을 실행시킨 뒤 컨테이너를 종료한다.

#이후 작업
도쿠 설치[https://github.com/varteam/Install-Dokku-on-ubuntu]
도커UI 설치 [https://github.com/varteam/Install-DockerUI-For-Docker-Management]
Shipyard 설치 []
