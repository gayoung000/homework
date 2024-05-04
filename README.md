# homework
테킷 프론트엔드 스쿨 10기 과제 저장소
<br/>
<br/>

## [HTML]
1. css 파일과 nomalize, reset 스타일시트 연결.
2. main 안에 container를 div로 만들고 "아바타 상태 관리 박스"라 칭함.
3. img와 상태 원을 하나의 세트로 관리하기 위해 이를 "avatars-setbox"란 div로 묶어줬다. 
   -> 이렇게 "avatars-setbox"는 총 8개가 나온다.
4. 상태 원 class 에 on/off 두가지를 각각 맞게 부여.
<br/>
<br/>

## [CSS 공통 부분]
1. main, container 크기 설정 
: 우선 main과 container은 같은 width: 350px을 줬다. 350 준 이유는 그 뒤에 나온다.

2. 이미지 크기 -> avatars-setbox 크기 설정
: 이미지 크기가 가로 세로 64px 이고 "avatars-setbox" 는 이미지 가로 세로에 맞춰 크기를 똑같이 설정했다. 

3. avatars-setbox 마진 설정
: "avatars-setbox"에 margin: 10px 을 주어 나란히 배열되었을 때 이미지 간격이 20px이 된다. 

4. 1번의 이유..
: 10+64+20+64+20+64+20+64+10 해서 336px이 나와 처음에 container 너비를 336으로 주었으나...무슨 일인지 4번째 이미지가 다음 줄로 넘어가는 현상이 나타났다. 통 해결이 안돼서 그냥 350으로 좀 넉넉히 주었다. 내가 의도한 대로 나오지 않아 꼼수를 쓴거라 이부분은 나중에 짚고 넘어가야 할 듯.

: 왜 굳이 avatars-setbox 마진 설정하지? 그냥 마진 안주고 20+64+20+64+20+64+20+64로, 즉 전체 cotainer안에 사이드 패딩없이(이미지의 마진값 없이) 간격 20으로 일정하게 배치시키게 하면 안되나? 할 수 있다. -> 처음에 의도한 것은 나중에 cotainer border 디자인이 있다면, 어느정도 사이 간격이 있는게 좋지 않을까 싶어 마진을 주었는데 지금 생각해보면 그냥 깔끔하게 마진 없이 갈껄 싶었다. 

5. 상태 on/off는 알잘딱깔센으로 크기, 모양, 색 지정해주고 position: absolute; right: 0; bottom: 0; 을 주어 이미지와 겹치게 했다.
<br/>
<br/>

## [CSS - float 이용]
1. container 
-> margin: 0 auto;
-> 너비, 높이 지정
-> display: flow-root; (아직 이거 이해 안됨)

2. .avatars-setbox
-> position: relative; (부모 역할)
-> float: left; (float 되어 왼쪽에 위치)

3. .on/.off
-> position: absolute; (자식 역할로 avatars-setbox 안에 있게 됨)
-> right: 0;, bottom: 0; (부모 안에서 위치 지정)
<br/>
<br/>

## [CSS - flex 이용]
1. container 
-> margin: 0 auto;
-> 너비, 높이 지정
-> display: flex;
-> flex-flow: row wrap;
-> justify-content: space-evenly;

2. .avatars-setbox
-> position: relative; (부모 역할)
-> display: inline-block; (인라인 블록요소로 옆에 나열될 수 있게 함)

3. .on/.off
-> position: absolute; (자식 역할로 avatars-setbox 안에 있게 됨)
-> right: 0;, bottom: 0; (부모 안에서 위치 지정)

4. .avatars-setbox에서 order로 위치 바꿈! 항상 order을 하려면 부모 요소에 flex 속성이 있어야 함.
<br/>
<br/>

## [avatars2.css]
* avatars2.css는 flex를 사용했을 때의 레이아웃을 따로 만든 것으로, 과제용은 아니고 개인적으로 만든 파일이다. 
<br/>
---
<br/>
<br/>
## [과제 시 궁금점]
1. 아까 [CSS 공통 부분] 4번이 궁금
2. css에서 order 순서 변경 해도 스크린 리더는 css 변경 사항을 반영 안하고 HTML 순서 그대로 읽음. 
<br/>
<br/>

## [과제 시 느낀점]
1. 이거 하나 하기에도 시간이 오래 걸렸다.
2. README.md도 마크업으로 이쁘게 만들고 싶지만 1번의 이유로 지쳤다.
3. 이해 안된 부분은 꼭 확실히 알아두자!
4. README.md를 써보니까 내가 어떤 생각으로 구조를 쌓았고, 놓치고 있는 부분이나 부족한 부분을 알 수 있어서 좋았다. 
