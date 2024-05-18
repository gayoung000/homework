# apple 제품 카드

## 과제 내용
그리드를 사용하여 반응형 레이아웃을 구현한다. <br>
* 중단점(breakpoint)는 1024px로 지정 <br>
 - (Small Screen - 1024px 이하 / Large Screen - 1024px 이상)<br>

* theme.css 파일에 제공 된 값(색상, 텍스트 크기, 여백 등)을 사용한다.

#### [Small Screen] <br>
* 1024px 이하 까지 One 라인이며 반응형이다.<br>
* 백그라운드 이미지가 단계별로 변한다.<br>

#### [Large Screen] <br>
* 1024px 이상이 되면 위의 3개 카드 이후로 Two 라인이며 반응형이다. <br>
* 백그라운드 이미지가 포커싱 된다.<br>
<br>

## 과제 설계
* 먼저 Small Screen을 기본 공통 레이아웃으로 삼아 설계했다.
* 카드 컴포넌트화 시키기 위해 카드 1개짜리만 html 구조로 만들었다.<br>
<img src="https://github.com/gayoung000/homework/blob/main/readme_images/apple/html구조.jpeg" width="25%" height="25%"/>
<br>

### :sunny: 카드 컴포넌트화
카드 컴포넌트 결과다. <br>
![카드 컴포넌트](https://github.com/gayoung000/homework/blob/main/readme_images/apple/card_component.gif)

<br>

### :sunny: 그리드 레이아웃
* 먼저, 위에서 만든 CSS 카트 컴포넌트 코드를 "card.css" 로 분리하고, "apple.css"에 @import 하였다. (레이아웃과 컴포넌트 분리)<br>
* html에서 카드 컴포넌트를 총 7개 만들고, 컴포넌트 컨테이너인 .box에 "display: gird;" 속성과 columns 줄은 1줄, row 줄은 auto로 설정했다.<br>
* 카드 1~6 까지 background-image 변경
* 미디어쿼리 속성을 사용해 최소 크기가 1024px일 때, .box 그리드를 2줄로 만들었다. 또한 card 1~3은 columns를 다 차지하도록 설정했다. <br>
![그리드1](https://github.com/gayoung000/homework/blob/main/readme_images/apple/마감준수_최종.gif) 
<br>

![그리드1](https://github.com/gayoung000/homework/blob/main/readme_images/apple/그리드1.png) 
<br>

![그리드2](https://github.com/gayoung000/homework/blob/main/readme_images/apple/그리드2.png)
<br>
<br>

## 과제 시 어려움
* 그리드 레이아웃을 만드는 과정에서 그리드 적용이 이상하게 되었다. 분명 카드 3개에게 column 2개를 다 차지하도록 했는데 1개만 차지하고, 무엇보다 가로 스크롤이 생기는 문제가 있었다.<br>
![과제 시 어려움](https://github.com/gayoung000/homework/blob/main/readme_images/apple/과제시_어려움.gif)
<br>
:heavy_exclamation_mark: **카드 컴포넌트 최상단인 .card-wrapper에 "width: 100vw;"를 줬었는데 100%로 고치니 문제가 해결되었다.**<br>
:heavy_exclamation_mark: **아직도 왜 이런 현상이 일어났는지 모르겠다.. 다시 이 차이점에 대해 공부를 해야겠다!**<br>
