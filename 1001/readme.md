<pre>
-<mark> 자바 스크립트 </mark>-
자바스크립트는 웹 개발에서 가장 중요한 프로그래밍 언어 중 하나로, 캔버스를 이용한 그래픽 처리, 로컬/세션 스토리지에 데이터 저장, 
위치 정보 서비스 제공 등 다양한 기능을 수행할 수 있습니다 일반적으로 HTML 요소에 이벤트(클릭, 입력 등) 를 발생시켜 동적인 웹 페이지를 구현하며, 
인터프리터 방식으로 코드가 한 줄씩 즉시 해석되어 실행됩니다. 자바스크립트는 HTML 태그 안에 직접 작성하거나 script 태그 안에 작성할 수 있으며, 
또는 외부 .js 파일을 만들어 불러오는 방법도 있습니다. 이때 외부 파일을 불러올 경우, (script src="파일명.js")(/script) 안에 자바스크립트 
코드를 작성하면 안 됩니다. 또한, 자바스크립트에서 이벤트 이름은 반드시 "on"으로 시작하며, 함수를 정의할 때는 function 키워드를 사용하고, 
그 뒤에 함수 이름과 매개변수를 선언합니다.

<b>HTML태그안에 직접 기술</b> -
<code>
        &lt;button onclick=&quot;alert('클릭!')&quot;&gt;눌러보세요&lt;/button&gt; /* 클릭하면이라는 이벤트를 시행(이벤트기에 on이 붙음) */
</code>
      
<b>script 태그 작성</b> -
<code>
    &lt;body&gt;
    &lt;h3&gt;document.write() 활용&lt;/h3&gt;
        &lt;hr&gt;
        &lt;script&gt; /* <- 여기 */
        document.write("&lt;h3&gt;Welcome!&lt;/h3&gt;");
        document.write("2 + 5 는 &lt;br&gt;");
        document.write("&lt;mark&gt;7 입니다.&lt;/mark&gt;");
        &lt;/script&gt; /* <- */
        &lt;/body&gt;
</code>
 
<b>.js파일 불러오기</b> -
          - lib.js파일 -
<code> function over(obj) { /* function으로 매게변수 "obj", 함수 이름인 "over" 생성 */
       obj.src="media/banana.png"; 
       }
       function out(obj) { /* fuction으로 매게변수 "obj", 함수 이름인 "out" 생성 */
       obj.src="media/apple.png";
       }
       
        - lib.js 사용파일 -
<code>
        &lt;!DOCTYPE html&gt;
        &lt;html&gt;
        &lt;head&gt;
            &lt;meta charset="utf-8"&gt;
            &lt;title&gt;외부 파일에 자바스크립트 작성&lt;/title&gt;
            &lt;script src="lib.js"&gt;&lt;/script&gt; 
            &lt;!-- 외부 파일을 불러왔기 때문에 이 script 안에는 JS 코드 작성 금지 --&gt;
        &lt;/head&gt;
        &lt;body&gt;
            &lt;h3&gt;마우스 올려 보세요&lt;/h3&gt;
        
            &lt;img src="media/apple.png" alt="이미지"
                onmouseover="over(this)"  &lt;!-- 마우스 커서가 이미지 위로 올라가면 이벤트 실행 --&gt;
                onmouseout="out(this)"    &lt;!-- 마우스 커서가 이미지에서 벗어나면 이벤트 실행 --&gt;&gt;
        &lt;/body&gt;
        &lt;/html&gt;
</code>

- <mark> 자바 스크립트 코드 </mark> -
<b>document.write() </b>-



 document.write는 HTML5의 Body의 속성과 같다

 let ret = prompt("이름을 입력하세요", "황기태");  
 

C언어의 개념과 비슷합 하지만 데이터 타입은 값에 의해서 결정됨(파이썬처럼)


p21
자바스크립트에서 var, let으로 변수 생성(두개는 다름)


p22
전역변수, 지역변수, block변수
block안에서 유효
지역 안에서 유효
모든 곳에서 유효
             - 구분 가능해야함

단항   - ++, --, +, =, ~, !등
산술   - *, /, %, +, -
시프트 - <<, >>, >>>
비교 - <, <=, =, >, >=, !=
비트 - &, ^, |
논리 - ! &&, ||
삼항 - (조건식)? (True):(false)
할당 - =, a = a + b

++a +  ++a   +   ++a   (원래는 왼쪽에서 오른쪽인데, 이거는 오른쪽부터 왼쪽까지임)

a = 1
b = ++a + ++a + ++a

| a = 4, b = 9 |

a = 1
b = a++ + a++ + a++

| a = 4, b= 9 |


p63 eval() - 숫자 묶기
isNaN()는 숫자면 false, 다른건 true
parseInt() 숫자로 바꿔줌























</pre>
