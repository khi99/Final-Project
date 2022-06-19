# Final-Project

<h3>Django를 이용한 Web Server구축</h3><br>
19_32181267_김형인<br><br><br><br>

window powershell에서 pip명령어를 통해 Django를 설치해준다.
<img src="https://user-images.githubusercontent.com/103643538/174446385-063256cf-72af-43a6-9fe7-8a52246a62c3.png"><br><br><br>


Django파일이 생성된것을 볼수있고 새로운 프로젝트를 추가해준다.
<img src="https://user-images.githubusercontent.com/103643538/174446391-d16604ee-2ae5-476e-add2-05c3099652e7.png"><br><br><br>


바로 서버를 실행해보면 다음과같이 주소와함께 서버가 시작됬다는 문구가 뜨게된다.
<img src="https://user-images.githubusercontent.com/103643538/174446392-8a46d9ac-06fd-49dd-a888-5cea698e52bb.png"><br><br><br>


나와있는 주소 127.0.0.1:8000 주소로 들어가보면 아무것도 안뜨는 상태
<img src="https://user-images.githubusercontent.com/103643538/174446394-12c64125-eda6-4ddb-8fb6-ecbece4fff47.png"><br><br><br>


지금 이 서버로 운영되는 페이지에, 내가 직접 작성한 HTML웹페이지를 넣어서 활용해보려한다.<br><br>

그러기위해서 먼저 Django에서의 "Views.py"라는 파일과 "템플릿"이라는 요소를 알아야하는데<br> Django에서의 View가 다른 MVC Framework에서의 Controller와 유사한 역할을 한다면, Django에서의 템플릿 (Template)은 MVC Framework에서의 View와 비슷한 역활을 한다. <br>템플릿 (Template)은 View로부터 전달된 데이터를 템플릿에 적용하여 Dynamic 한 웹페이지를 만드는데 사용된다.
Template은 HTML 파일로서 Django App 폴더 밑에 "templates" 라는 서브폴더를 만들고 그 안에 템플릿 파일(*.html)을 생성한다. 이는 단일 App이거나 동일 템플릿명이 없는 경우 사용할 수 있다.<br><br><br><br>



그런데 여기서 Django 개발 가이드라인은 "App폴더/templates/App명/템플릿파일" 처럼,  App 폴더 밑에 templates 서브폴더를 만들고 다시 그 안에 App명을 사용하여 서브폴더를 만든 후 템플릿 파일을 그 안에 넣기를 권장한다고 한다.<br><br>
이는 템플릿(templates)이라는 폴더를 생성한 후 관리를 쉽게하기위해서인데, 이를위해 프로젝트명과 똑같은 폴더를 다시 만들어주고 거기에 이 주소에 작동시킬 html소스를 넣는다.<br><br>

구체적인 이유는 만약 복수의 App들이 동일한 이름의 템플릿을 가진 경우, View에서 잘못된 템플릿을 가져올 수 있기 때문인데, 예를 들어, App1에 create.html이 있고, App2에 동일한 create.html 템플릿이 있는 경우, App2의 View에서 create.html를 지정하면, 처음 App1의 create.html을 사용하게 된다.<br>
이는 템플릿을 찾을 때 자신의 App 내의 템플릿을 먼저 찾는 것이 아니라, 전체 App들의 템플릿 폴더들을 처음부터 순서대로 찾기 때문이다. View에서 "App2/create.html" 과 같이 템플릿명을 지정하면 이런 혼동은 없어진다.<br>
쉽게말해 다른 앱의 templates 내의 html 파일과 헷갈리지 않게 하기 위함이라고 생각하면 된다.<br><br>

그래서 여기서는 firstapp/templates/firstapp/introduce.html 이렇게 경로를 구성하여 내가 작성한 HTML인 introduce.html을 넣어주었다.<br>
<img src="https://user-images.githubusercontent.com/103643538/174447979-e9591e7d-73eb-4950-b559-5ebc4aa72001.png"><br><br><br>




다른 이용자들에게 이 페이지에서 보여줄 화면을 추가하기위해선 프로젝트파일 내의 views.py에서 introduce.html 파일을 렌더링 할 함수를 만들어야 한다.<br>
다음과같이 템플릿폴더 내에 introduce.html가 위치하는 경로를 적어준다.<br>
<img src="https://user-images.githubusercontent.com/103643538/174447980-01b96726-c480-4774-a5be-dcda5d7ddcbd.png"><br><br><br>


이제 html 화면을 보여줄 수 있도록 url 설정을 한다.<br>
url로 보여줄 화면은 urls.py에다가 방금 views.py에서 적었던 함수를 사용하면 된다.<br>
때문에 import firstapp.views를 시켜주면서 127.0.0.1/추가할경로명 을 적고, 함수를 적어주면 된다.<br>
다음과 같이 적을경우 127.0.0.1/first 라는 주소에 나의 introduce.html이 띄워질것이다.<br>
<img src="https://user-images.githubusercontent.com/103643538/174447976-b7a97078-f67d-4cb6-81ff-8761b5c78c6f.png"><br><br><br>


http://127.0.0.1:8000/first/ 이라는 주소에 다음과같이 자기소개 페이지가 올라간 상태<br>
<img src="https://user-images.githubusercontent.com/103643538/174446402-0b86344d-2aa9-4eb7-be8d-2cac1d59bd57.png"><br><br><br>


이제 이 주소를 외부접속에서도 가능하도록 내 pc의 ip주소를 allowed_host에 추가하여 사이트를 오픈해볼것이다.<br>
settings.py 내에서 allowed_host에 ip주소를 추가해준다.<br>
<img src="https://user-images.githubusercontent.com/103643538/174446404-fe81103d-2ecb-4faa-9016-634dcab0a242.png"><br><br><br>

열린 주소가 바뀐것을 볼수있다.(컴퓨터 접속시 화면)<br>
<img src="https://user-images.githubusercontent.com/103643538/174446406-8f3cd4ff-c279-401b-9cd4-2e70e2ebd749.png"><br><br><br>

다른기기(데이터로 사용중인 내 핸드폰) 접속화면<br>
<img src="https://user-images.githubusercontent.com/103643538/174446411-b25b8686-26e0-42b1-ae9f-09cd55e515c9.jpg"><br><br><br>

<br><br><br>
여기서 클라우드 서버를 이용하여 여는 방법을 찾아봤는데 클라우스 서비스중 구름ide와 네이버 클라우드에 가입을 해보았다.<br>
구름 ide는 클라우드와 개발환경까지 같이 제공하는 서비스를 제공한다고 하는데 컨테이너를 하나 생성해서 실행을 해보면 하나의 가상공간이 나온다.<br>
아예 새로운 환경이라 그런지 여기서 장고설치를 아예 처음부터 다시해야되는듯 보였다.
<img src="https://user-images.githubusercontent.com/103643538/174478171-aa9935c9-5d21-47f4-9acb-17d9311e4143.PNG"><br><br><br>


네이버 클라우드는 클라우드서비스를 제공하는데 결제수단을 먼저 등록해야 서버시스템을 사용할수있고, 서버 사양에따라, 공인ip를 추가할때마다 요금이 자동으로 빠져나가 조금 겁이나서 시도를 해보진 못했다...<br>
여기서 결제를 하여 공인ip를 할당받으면 그 공인ip를 내 윈도우 visual studio code에서 작업한 장고에 allow host로 추가하여 그 주소로 서버를 열어서 작동시키는게 가능할것같았다.
<img src="https://user-images.githubusercontent.com/103643538/174478062-2d4b7294-5a22-4849-a083-5f64e20767f9.PNG"><br>
<img src="https://user-images.githubusercontent.com/103643538/174478063-b089dcc0-cebd-4aa2-8c87-0817e773e69a.PNG"><br>
