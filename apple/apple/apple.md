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

```html
<div class="card-wrapper card-1">
  <a href="/" class="card-link-wrapper" target="_self" aria-hidden="true"></a>
  <article class="card-text-wrapper">
    <h2>iPad Pro</h2>
    <p class="subhead">놀라우리만치 얇다.
      <br class="br-small">엄청나게 강력하다.
    </p>
    <p class="callout">출시일 추후 공개</p>
    <div class="button-link">
      <button class="more-button" type="button" onclick="location.href='/'">더 알아보기</button>
      <button class="price-button" type="button" onclick="location.href='/'">가격 보기</button>
    </div>
  </article>
</div>
```
<br>

### :sunny: 카드 컴포넌트화
카드 컴포넌트 결과다. <br>
<img src="https://github.com/gayoung000/homework/blob/main/readme_images/apple/card_component.gif" width="80%" height="80%"/>
<br>
<br>

### :sunny: 그리드 레이아웃
* 먼저, 위에서 만든 CSS 카트 컴포넌트 코드를 "card.css" 로 분리하고, "apple.css"에 @import 하였다. (레이아웃과 컴포넌트 분리)<br>
* html에서 카드 컴포넌트를 총 7개 만들고, 컴포넌트 컨테이너인 .box에 "display: gird;" 속성과 columns 줄은 1줄, row 줄은 auto로 설정했다.<br>
* 카드 1~6 까지 background-image 변경
* 미디어쿼리 속성을 사용해 최소 크기가 1024px일 때, .box 그리드를 2줄로 만들었다. 또한 card 1~3은 columns를 다 차지하도록 설정했다. <br>
<img src="https://github.com/gayoung000/homework/blob/main/readme_images/apple/마감준수_최종.gif" width="80%" height="80%"/>
<br>
<br>

## 과제 시 어려움
* 그리드 레이아웃을 만드는 과정에서 그리드 적용이 이상하게 되었다. 분명 카드 3개에게 column 2개를 다 차지하도록 했는데 1개만 차지하고, 무엇보다 가로 스크롤이 생기는 문제가 있었다.<br>
<img src="https://github.com/gayoung000/homework/blob/main/readme_images/apple/과제시_어려움.gif" width="80%" height="80%"/><br>
:heavy_exclamation_mark: **카드 컴포넌트 최상단인 .card-wrapper에 "width: 100vw;"를 줬었는데 100%로 고치니 문제가 해결되었다.**<br>
:heavy_exclamation_mark: **아직도 왜 이런 현상이 일어났는지 모르겠다.. 다시 이 차이점에 대해 공부를 해야겠다!**<br>

<br>
<br>

# 과제 마감시간 이후 작업
* html text 내용 바꾸기 :white_check_mark:
* 흰색 배경 카드 폰트 컬러 블랙으로 지정 :white_check_mark:
* Large Screen 상단 여백, 글자 크기 바꾸기 :white_check_mark:
* 카드 6번의 background-position을 y축 방향으로 조금 내렸다. :white_check_mark:
* 카드 범위 내 어디를 눌러도 link로 연결되게 하기(추가로 하면 좋을 것!)
* navigation 바 만들기(추가로 하면 좋을 것!)<br>

<img src="https://github.com/gayoung000/homework/blob/main/readme_images/apple/최종2.gif" width="80%" height="80%"/><br>
