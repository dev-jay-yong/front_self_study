### Sass란?
1. 기본적으로 컴파일을 진행해서 css파일로 만들어주어야 함.
2. 아래 이미지와 같이 Nesting(중첩)구조를 사용함.
3. Sass는 파이썬과 같이 들여쓰기로 중첩구조를 구분하기 때문에 들여쓰기에 주의해야 한다. (scss는 {}를 통해 구분)


![캡처2](https://user-images.githubusercontent.com/96015600/162417897-bf26fbd3-269f-47fa-878e-20537c02472f.PNG)
(이미지 출처 - 제로베이스)


### Sass 7-1 패턴

- ### sass/
  - <b>abstracts/</b>
    - _variables.scss (Sass 변수)
    - _functions.scss (Sass 함수)
    - _mixins.scss (Sass 믹스인)
    - _placeholders.scss (Sass 플레이스홀더)
    
  - <b>base/</b>
    - _reset.scss (리셋/정규화)
    - _typography.scss (타이포그래피 규칙)
    - _ (기타)
    
  - <b>components/</b>
    - _buttons.scss (버튼)
    - _carousel.scss (캐러셀)
    - _cover.scss (커버)
    - _dropdown.scss (드롭다운)
    - _ (기타)

  - <b>layout/</b>
    - _navigation.scss (네비게이션)
    - _grid.scss (그리드 시스템)
    - _header.scss (헤더)
    - _footer.scss (푸터)
    - _sidebar.scss (사이드바)
    - _forms.scss (폼)
    - _ (기타) 

  - <b>pages/</b>
    - _home.scss (홈 한정 스타일)
    - _contatct.scss (연락처 한정 스타일)
    - _ (기타)

  - <b>themes/</b>
    - _theme.scss (디폴트 테마)
    - _admin.scss (관리자 테마)
    - _ (기타)

  - venders/
    - _bootstrap.scss (Bootstrap)
    - _jquery-ui.scss (jQuery UI)
    - _ (기타)
  
  - main.scss (메인 Sass 파일)

이때 파일명에 _가 붙는 경우 @import 되어 사용될 것으로 파악한다.

### Sass 변수
```scss
$h1-size: 5em;
$h1-color: blue;
$h1-align: center;
$gray100: #ddd;

h1 {
  font-size: $h1-size;
  color: $h1-color;
  text-align: $h1-align;
}

div {
  color: $h1-color
}
```

### Sass @mixin
```scss
@mixin ellipsis{
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}

p {
  width: 300px;
  @include ellipsis;
}
```