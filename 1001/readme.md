<pre>
https://ko.javascript.info/intro 자바스크립트 설명
모질라 자바스크립트 사이트
브라우져 안에 엔진(인터프리터)가 있음
이벤트가 발생하면 처리할 언어가 필요함 -> 자바 스크립트

-자바스크립트 역할-
캔버스 그래픽, 로컬/세션 스토리지 저장, 위치정보서비스 등

자바스크립트의  사용법은 <script></script> 태그를 이용하고 안에 넣음

자바스크립트 이벤트는 on~가 들어간다  
onmouseout= 마우스가 올려지지 않으면
onmouseover = 마우스가 올려지면

<code>
<script>
function over(obj) {
obj.src="media/banana.png";
}
function out(obj) {
obj.src="media/apple.png";
}
</script>
</code>

p9 주의사항 

자바스크립트를 쓸때 태그, 스크립트 태그, 외부파일에 기술할 수 있음

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
























</pre>
