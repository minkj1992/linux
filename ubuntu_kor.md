# Ubuntu 18.04 kor
> 우분투 한글입력 with 

- `i-bus`: 그냥 한글이 변경안되고, 되더라도 설정을 잡아주어야 하는게 있고, 그렇게 하더라도 제대로 입력이 안되는 느낌 (chrome에서 한글 변환 안됬었음)
- `fcitx`: 정말 별로다. 입력할때마다 버퍼링생기는 것도 그렇고 최악임
- `UIM`: 최고

## UIM 설정방법
> https://progtrend.blogspot.com/2018/06/ubuntu-1804-uim.html?showComment=1585914590990#c1853594931924376468

- 너무나 감사한 블로그
- 정리해주셔서 너무 감사합니다.

- **한가지 에러는 xmodmap은 18.04 기준으로 .sh로 설정해주던지 해야 했다.**
- 이를 해결하기 위해서는 bin 파일을 수정하던지, `Tweaks`에서 `Keyboard & Mouse > Additional Layout Options > Korean Hangul/Hanja keys > Right Alt as Hangul, right Ctrl as Hanja 체크` 하면된다.