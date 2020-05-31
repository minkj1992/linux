# [Ubuntu] apt-get 패키지 다운로드 서버(sources.list) 변경하기
> Linux(Ubuntu)에서 apt-get 패키지를 다운로드하는 서버를 변경해보자



## 환경 및 선수조건
Linux(Ubuntu 16.04)


## sources.list
- 파일 경로 및 열기
- 파일은 `/etc/apt/`에 위치

    $ cd /etc/apt/
    $ vim sources.list


## 기본 설정
기본적으로 지역을 한국으로 설정하시고 한국어로 언어를 설정하시면 /etc/apt/sources.list에 빨간색으로 http://kr.archive.ubuntu.com/ubuntu/로 나와있을겁니다.


![](https://twpower.github.io/images/20180303_99/source-list.png)


## 문제 혹은 에러
간혹 아래 나와 있는 문제들처럼 설치할 수 없다고 오류가 뜰 때가 있는데 저장소에서 해당패키지에 대한 정보를 가지고 있지 않거나 일시적으로 서버가 작동하지 않을 수도 있다.

    E: 아카이브를 받을 수 없습니다. 아마도 apt-get update를 실행해야 하거나 --fix-missing 옵션을 줘서 실행해야 할 것입니다.
    
    E: Unable to fetch some archives, maybe run apt-get update or try with --fix-missing?

위와 같은 상황일 때 apt-get의 패키지 서버를 다른 주소로 해서 다시 실행하면 제대로 설치되는 경우도 있다.



## apt-get 서버 변경
`http://kr.archive.ubuntu.com/ubuntu/` -> `http://ftp.daumkakao.com/ubuntu/`로 변경

파일 편집기 vim에서 파일(/etc/apt/sources.list)을 열고 아래와 같은 명령어로 문자열을 치환해줍니다.

    :%s/kr.archive.ubuntu.com/ftp.daumkakao.com


## 동작 확인
apt-get를 통해서 제대로 동작하는지 확인

    $ sudo apt-get update; sudo apt-get upgrade -y;


[참고자료](http://inasie.tistory.com/39)
