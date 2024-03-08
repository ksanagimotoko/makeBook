# flex 태그를 사용하여 신호등 만들기
***
flex 태그를 사용하고자 한다면  
title태그 밑에 style 태그를 넣어주고 그 안에서 flex 태그를 사용해준다  
나는 신호등을 만들 것이기 때문에 이름을 traffic_light 으로 했다  
style 태그에서 이름 앞에 .을 붙이는 이유는 이게 class 요소를 불러오는 방법이기 때문이다
***
## traffic_light  
* display: flex;
flex 태그를 사용하겠다    
* background-color: #333; 
배경색을 검정으로  
* flex-direction: row;
배치 방향을 가로로  
justify-content: center;
중앙에 정렬되게  
* justify-content: space-around;
사이에 간격을 주게  
* border-radius: 10px;
테두리 모서리를 둥굴게  
* padding: 45px; 
내부 여백을 모든 방향으로 45  
* width: 300px;
요소의 너비를 300으로
***
## light  
* width: 100px; 
요소의 너비를 100으로  
* height: 100px; 
요소의 높이를 100으로  
* border-radius: 50%; 
요소의 모서리를 반지름이 50인 원형으로 설정해 요소의 모양을 원으로 만듦  
* margin: 10px 0;
요소의 위쪽과 아래쪾 여백을 10픽셀로, 좌우 여백은 0  
* display: flex;
flex 태그를 사용하겠다  
* align-items: center;
flex 아이템을 수직, 중앙으로 정렬  
* justify-content: center;
flex 아이템을 수평, 중앙으로 정렬
***
***
## 본문(body 태그)
* class="traffic_light"  
 이 태그는 내가 만들 신호등을 전체로 감싸는 컨테이너와 같은 태그이다  
* class="light red"  
 이 태그는 위에서 만들었던 style에서 .light와 .red 클래스를 나타낸다  
* img src="./image/left.png" class="light green"  
green에 있는 이 img 태그  
우선 "./image/left.png"에서 맨 앞에 있는 .은  
내가 만든 html과 같은 폴더 안에 있다 라는 것을 의미한다  
그래서 그 이후의 경로를 지정해주면 된다  
그리고 class를 지정해준 이유는 이 원형 안에 넣기 위해서이다
***
***
## script
* window.addEventListener('load', function() {  
스크립트가 로드 될 때 실행 될 이벤트 리스너이다  
모든 html 요소가 로드되었을 때 스크립트가 실행 될 수 있도록 함  
* var greenleft = document.querySelector('.light.green img');  
var 뒤에있는 greenleft는 내가 임의로 지정한 이벤트 이름이다  
document.querySelector는 css의 요소인 light와 다른 요소인 green의 img 이미지를 불러온다는 의미이다
* setInterval(function() { ... }, 1000);  
주기적으로 실행되는 함수를 정의한다  
{} 안에 ... 부분에 주기적으로 실행할 코드를 작성해준다  
, 뒤 1000부분에는 몇 초 마다 반복할지를 나타내는데 1000은 1초이다  
* if (orangeLight.style.display === 'none')  
주황색 신호등의 display 즉, 노출이 none이라면~
* {orangeLight.style.display = 'block';  
block 즉, 주황색 신호등을 보이게 한다
* greenleft.style.display = 'block'; }  
또한 초록색 신호등 안에 있는 화살표 이미지를 보이도록 한다
* else {orangeLight.style.display = 'none';  
그렇지 않으면 주황색 신호등을 보이지 않게 한다
* greenleft.style.display = 'none';}  
또한 초록색 신호등 안에 있는 화살표 이미지를 보이지 않게 한다