<pre>
-<mark> 자바 스크립트 </mark>-
자바스크립트는 웹 개발에서 가장 중요한 프로그래밍 언어 중 하나로, 캔버스를 이용한 그래픽 처리, 로컬/세션 스토리지에 데이터 저장, 
위치 정보 서비스 제공 등 다양한 기능을 수행할 수 있습니다 일반적으로 HTML 요소에 이벤트(클릭, 입력 등) 를 발생시켜 동적인 웹 페이지를 구현하며, 
인터프리터 방식으로 코드가 한 줄씩 즉시 해석되어 실행됩니다. 자바스크립트는 HTML 태그 안에 직접 작성하거나 script 태그 안에 작성할 수 있으며, 
또는 외부 .js 파일을 만들어 불러오는 방법도 있습니다. 이때 외부 파일을 불러올 경우, (script src="파일명.js")(/script) 안에 자바스크립트 
코드를 작성하면 안 됩니다. 또한, 자바스크립트에서 이벤트 이름은 반드시 "on"으로 시작하며, 함수를 정의할 때는 function 키워드를 사용하고, 
그 뒤에 함수 이름과 매개변수를 선언합니다.

<b>HTML태그안에 직접 기술</b> -
ex) <code>
        &lt;button onclick=&quot;alert('클릭!')&quot;&gt;눌러보세요&lt;/button&gt; /* 클릭하면이라는 이벤트를 시행(이벤트기에 on이 붙음) */
</code>
      
<b>script 태그 작성</b> -
ex) <code>
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
ex)         - lib.js파일 -
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
                onmouseout="out(this)"    &lt;!-- 마우스 커서가 이미지에서 벗어나면 이벤트 실행 --&gt;
        &lt;/body&gt;
        &lt;/html&gt;
</code>

- <mark> 자바 스크립트 코드 </mark> -
<b>document.write() </b>-
자바스크립트로 HTML 콘텐츠를 웹 페이지에 직접 삽입하는 코드로 ()안의 내용이 화면에 출력됩니다.
그리고 document.writeln()는 문자를 출력하고 한칸 들여쓰기가 됩니다.
ex) <code>
    document.write("&lt;h3&gt;Welcome!&lt;/h3&gt;"); /* 화면에 Welcome! 출력 */
</code>

<b>prompt()</b> -
사용자로부터 문자열을 입력 받아 리턴 코드로 보통은 function함수 정의랑 같이 쓰이고,  사용법은 prompt("메시지", "디폴트 입력값") 입니다.
ex) <code>
        let ret = prompt("이름을 입력하세요", "홍길동"); /* 입력칸의 제목은 "이름을 입력하세요" 이고, 기본값은 "홍길동" 으로 설정 */
        if(ret == null) {
        
        }
        else if(ret == "") {
        
        }
        else {
        
        } /* ret에는 아무것도 입력 받지 못했을 때, 취소 버튼을 누르면(null), 입력 했을 때의 경우가 있음. */ 
</code>
 
-<mark> 변수 </mark>-
변수란 자바스크립트 프로그램이 실행 중에 데이터를 저장하는 공간을 말하고, 변수 선언 할떄, var, let, const 변수 선언 키워드가 있고, 변수 선언이 적용되는 범위의 종류에는 전역 변수, 지역 변수, 블록 변수가 있습니다.

-<mark> 변수 선언 키워드 </mark>-
변수 선언 키워드에는 var, let, const가 있습니다.

<b>var </b>-
var은 같은 이름으로 중복 선언이 가능하며, 변수 선언 전에도 사용가능하긴 하나 undefined로 초기화되고, 블록 밖에서도 접근 가능합니다. 그리고 값은 바꿀수 있습니다.
ex)    -  같은 이름으로 중복 선언 가능  -
        <code> 
        var n = 1;
        var n = 2;
        </code>
        
        - 변수 선언 전 사용 가능 -
        <code>
        console.log(a); // undefined
        var a = 5;
        </code>
        
        - 블록 밖에서 접근 가능 -
        <code> 
        if (true) {
        var x = 10;
        }
        
        console.log(x); /* 10의 값이 출력됨 */

        - 변수의 값 바꾸기 -
        <code>
                var n = 1
                n = 2
        </code>
</code>
        
<b>let </b>-
let은 var과 다르게 같은 이름으로 변수 사용이 불가능 하며, 변수 선언 전에 사용 불가능 하고, 블록 밖에서도 접근 불가능합니다. 하지만 값은 바꿀수 있습니다.

<b>const </b>-
const는 같은 이름으로 중복 선언 불가능 하며, 블록 밖에서는 접근 불가능하고, 한번 선언한 변수의 값 또한 바꿀 수 없는 상수의 특징을 가집니다.

<b>전역 변수 </b>-
함수 선언 전 선언된 변수로 모든 함수에 전역변수를 사용 할 수 있습니다. 전역 변수는 블록 안에 있어도 앞에 키워드를 붙이지 않으면 전역 변수의 의미를 갖습니다. 
        
<b>지역 변수 </b>-
함수 선언 후 그 안에 선언된 변수로 함수 안에만 사용 할 수 있습니다.
        
<b>블록 변수 </b> -
블록 안에 선언 된 변수로 해당 블록 안에서만 사용 가능 합니다.
        
ex)
        -전역 변수, 지역 변수, 블록 변수 -
<code>
        let x; /* 전역 변수 x 선언 */
        function f() {
        let y; /* 지역 변수 y 선언 */
        x = 10; /* 전역 변수 x에 10 저장 */
        y = 20; /* 지역 변수 y에 20 저장 */ 
        z = 30; // 새로운 전역 변수 z가 선언 후 30 저장(let 키워드 선언을 하지 않았기에 전역 변수) */
         if(y == 20) {
                let b = 40; // if 블록에서만 사용되는 블록 변수 b 선언 */
                 b++;
                } 
                
/* 이곳에서는 변수 x, y, z에 모두 접근 가능(블록 변수인 b는 블록에서 나왔기에 b라는 함수이름만 남아있고, 40이라는 값은 없어집니다.) */
}
/* 전역변수인 x는 10을 저장 했고, z는 30을 저장했기에 함수 밖에 나와서도 10, 30의 값이 유지가 되고, 지역 변수인 y는 함수 안에서만 사용 가능하므로 함수이름만 남아있고, 값은 없어집니다. */

</code>

<b>this </b>-
전역변수와 지역변수의 이름이 같을 떄 구분해서 값을 지정하는 방법은 해당 이름에 아무것도 건들지 않고 값을 넣으면 지역 변수에 값을 넣는 방법이고, this.전역변수 를 하여 값을 넣으면 전역변수에 값을 넣는 방법입니다.
하지만 let으로 선언된 전역 변수는 this로 접근할 수 없고, let 전역변수와 let 지역변수가 같은 이름으로 선언되었다고 가정하고 변수에 값을 넣는다고 하면 지역 변수에 선언이 되고,
지역변수가 선언이 되지 않고, 값을 넣는다면 let전역 변수에 값이 저장이 됩니다.
ex)     - this 사용 예시 -
        <code>
        var x; /* 전역변수 x선언 */
        function f() {
        var x; /* 지역변수 x선언 */
        x = 1; /* 지역변수 x에 1 저장 */
        this.x = 100; /* 전역변수 x에 100 저장 */
        }
        </code>
        
        - let 동작 원리(1) -
         <code>
        let x; /* 전역변수 x선언 */
        function f() {
        let x; /* 지역변수 x선언 */
        x = 1; /* 지역변수 x에 1 저장 */
        }
        </code>
        
         - let 동작 원리(2) -
         <code>
        let x; /* 전역변수 x선언 */
        function f() {
        x = 1; /* 전역변수 x에 1 저장 */
        }
        </code>

-<mark> 자바 스크립트 문자 리터럴 </mark>-
정수, 실수, 문자열, 그리고 이 외 나머지가 있습니다.

<b>정수 </b>-
정수 표현은 8진수는 숫자 앞에 0을, 16진수는 숫자 앞에 0x를, 2진수는 숫자 앞에 0b를 붙이고, 10진수는 숫자 그대로 사용하면 값이 설정 됩니다.
ex)     
        <code>
        let A = 0b1001 // (2진수)
        let B = 012 // (8진수)
        let C = 0xAB //(16진수)
        let D = 13 // (10진수)
        </code>

<b>소수 </b>-
소수는 소수점을 붙여 소수형으로 나타내거나, E를 써서 지수형으로 나타냅니다.
ex) 
        <code>
        let h = 0.3214 // 소수형
        let g = 1234E-4 // 지수형
        </code>

<b>문자열 </b>-
문자열을 만들때는 ' 또는 " 중 하나를 반드시 선택하여 시작하고, 문자열의 시작과 끝 따옴표가 반드시 같아야 합니다.
문자열에서 특정 문자를 그대로 사용하고 싶을 때에는 \로 열고 \로 닫으면 해당 문자를 문자열 안에서 그대로 사용할 수 있습니다.
ex)     <code>
        &lt;!DOCTYPE html&gt;
        &lt;html&gt;
        &lt;head&gt;
        &lt;meta charset="utf-8"&gt;
        &lt;title&gt;리터럴&lt;/title&gt;
        &lt;/head&gt;
        &lt;body&gt;
        &lt;h3&gt;리터럴&lt;/h3&gt;
        &lt;hr&gt;
        &lt;script&gt;
        let oct = 015;  
        let hex = 0x15; 
        document.write("8진수 015는 십진수로 " + oct + "&lt;br&gt;"); 
        document.write("16진수 0x15는 십진수로 " + hex + "&lt;br&gt;");
        document.write('문자열 : 단일인용부호로도 표현' + "&lt;br&gt;"); 
        document.write("그녀는 \"누구세요\"라고 했습니다."); /* "그녀는 누구세요" 라고 큰 따움표도 그대로 출력됨 */
        &lt;/script&gt;
        &lt;/body&gt;
        &lt;/html&gt;
        </code>











        
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
