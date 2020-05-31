# 디폴트 터미널 변경하기
> `Terminator`를 깔고 나니 18.04우분투 환경에서 `ctrl + alt + t`명령어가 디폴트 터미널이 아닌, 터미네이터를 키는 현상이 발생하였다.


## Solution

```bash
minkj1992@minkj1992-900X5L:~$ sudo update-alternatives --config x-terminal-emulator
[sudo] minkj1992의 암호: 
대체 항목 x-terminal-emulator에 대해 (/usr/bin/x-terminal-emulator 제공) 2개 선택이 있습니다.

  선택       경로                           우선순� 상태
------------------------------------------------------------
  0            /usr/bin/terminator               50        자동 모드
* 1            /usr/bin/gnome-terminal.wrapper   40        수동 모드
  2            /usr/bin/terminator               50        수동 모드

Press <enter> to keep the current choice[*], or type selection number: 
```

위의 명령어를 통하여 terminator가 아닌 `/usr/bin/gnome-terminal.wrapper`의 크놈 터미널을 디폴트 터미널로 지정하도록 한다.


