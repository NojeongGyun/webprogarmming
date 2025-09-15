서버가 클라이언트가 될 수있음(서버가 다른서버에서 요청하고 받으면)
아이피주소를 이용하여 서버접속
도메인 주소만 이용하면 할당받은 아이피주소를 입력해줌
내가 나한테 접근(로칼로스, 아이피주소) (클라이언트가 되어 자기자신에게 접속)
포트번호(웹서비스 80 - 포트번호(80)이면 생략가능 / index.html생략가능)

로칼로스티(자기자신 ip)(localhost)
127.0.0.1:5500(op주소:포트번호)

-emmet -
Emmet은 HTML, CSS 등의 코드 작성 속도를 빠르게 해주는 도구로써, 지정 되어 있는 문자에 형식을 더하면 완성이 됩니다. 지정 되어 있는 
문자에는 여러개가 있는데 그 중 몇가지만 살펴 보자면 Child: >, Multiplication: *, numbering: $, Climb-up: ^, Grouping: () 가 있습니다.

-emmet chlid : > -
child는 부모/자식 관계로써 A > B라고 하면 A안에 B가 속해 있는걸 뜻합니다. 
예시로 nav>ul>li
<nav>
    <ul>
        <li></li>
    </ul>
</nav>
-emmet Multiplication: *

콘텐츠를 구조화 시킨 코드를 HTML태그
<meta charset="UTF-8"> 
github, git, emmet
meta는 문서 전체를 설명하는 부분
서버에서 받아서 브라우저에서 표현할때 <!DOCTYPE html> 이런식으로 기술함(HTML5 구조를 지킴)
alt가 없으면 태그를 실행 못함
속성에 빈칸없이 작성
<h숫자>는 태그가 없는데 브라우저에서는 <문자> </문자> 가 됨
브라우저는 태그에 맞춰서 화면에 렌더링함
스타트태그 엔드태그 사이에는 콘텐츠라고 부르는 게 있음 (한 문장을 elements라고 부름) (나중에 튜드에 노드가 됨)

wihte characters(balnk, tab, new line)들은 모두 한개의 빈칸으로 표현됨 -> &nbsp;(한칸 띄워쓰기)(엔티티표현)
<pre>태그로 이용하면 있는 그대로 출력이 됨(각자의 특성에 맞게 space, tap, new line)

<br>
  https://www.w3schools.com/

  block태그, 인라인태그 구분

  div끼리의 구분(class(같은 이름의 클래스 중복 가능), ID(중복 불가능: 서로간의 식별을 위해 독보적인 구조를 가짐))
  <div class = "A"> </div>     , <span id = "A"> </span>

  메타데이, 리스트(중첩가능), 
  테이블의 중요(tr안에 동인한 th가 있어야함) , 콜스펜, 로스팬, 하이퍼링크(target), Iframe, 오디어(선택 재생 가능은 재생가능한지 위에 부터 실행)
  
  

