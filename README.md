<div align='center'>

# css 공부

</div>

<h4> 2022년도 CSS 업데이트 기술 정리</h4>

color-mix()

#

color-mix() 를 사용하면 브라우저에서 색상을 혼합할 수 있다.

▼▼▼

    .container {
      background-color : color-mix(red 30%, blue 70%);
    }
    
이렇게 사용할 수 있다.

아니면 
:root를 사용하여 변수로 색상을 저장한다음 ' color-mix' 내부에서 사용해도 된다.

#

<h4>accent-color</h4>

#

accent-color 를 사용하면 커스터마이징이 넘나 어려웠던 HTML 요소의 색상을 변경 할 수 있다.
예를들어 Radio버튼, 체크박스, 프로그래스바, 범위 슬라이더 등 수정이 가능하다.

이전엔 이 색상을 바꾸려면 수동으로 다 했었어야했다.
배경색, 테두리 색상 hover 색상 을 하나하나 다 바꿔야 해서 다 기억하기도 힘듬;
그러나 'accent-color' 를 사용하면

▼▼▼

    <style>
       :root{
          accent-color : red;   
       }
    </style>

    <input type="checkbox"></input>
     <input type="radio"></input>
    <input type="range"></input>
    <progress max='100' value='50'>50%</progress>
    

각 요소의 'accent-color'가 어떻게 될 것인지 알려주기만 하면
브라우저는 우리를 위해 모든 색을 바꿔준다.


#

<h4>color-centrast</h4>

#

텍스트를 읽시 쉽도록 하려면 배경색과 텍스트 색 사이의 대비가 좋아야한다.
배경색 대비하여 잘 보이는 색을 우리가 직접 고르는 대신에 color-contrast를 사용하면 된다.

예를 들어보자

▼▼▼

    .box{
       background-color : red;
    }


여기 배경색이 빨간색인 상자가 있다. 이젠 텍스트의 색상을 골라야 하는데.


    .box{
      background-color : red;
      color: color-contrast(red);
    }

