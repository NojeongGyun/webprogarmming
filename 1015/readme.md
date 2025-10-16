<pre>- <mark> 자바 스크립트 객체 </mark> -
객체란 만들어진 틀 안에서 프로퍼티의 속성과 메소드를 정하는 것을 활용하는 매체를 말합니다. 사용 할때 마다 틀 안에서 다르게 속성, 메소드를 활용할 수 있는 장점이 있습니다. 
몇가지 여기서 쓰는 용어를 알아보자면 class의 변수를 프로퍼티 라고 하고, class 변수를 다루는 함수를 메소드라고 하고, 객체 생성 연산자를 추가 할떄 new 객체를 사용합니다.
객체를 만들려면 let 선언을 하여 만들어도 되고, class 정의로 하여 만들어도 되고, 또한 이미 구현되어 있는 코어 객체로 사용하여도 됩니다.

<b>let선언 객체</b> -
let 선언 객체는 let 변수 {..} 중괄호안에는 각종 메소드, 속성을 포함 할 수 있습니다.
ex)   - let 선언 객체 예시 -
 <code> let account = {
            owner: "홍길동", // account객체의 owner 프로퍼티에 "홍길동" 저장
            balance: 35000, // account객체의 balance 프로퍼티에 "35000" 저장
            deposit: function(amount) { // deposit 메소드에 amount 파라미터의 값을 위에서 받음
                this.balance += amount; // 객체 속성 balance의 값을 파라미터 amout와 더함
            },
            inquiry: function() {
                return this.balance; // inquiry 메소드는 현재 객체 속성에 저장 되어있는 balance의 값을 리턴함
            }
        };
    account.balance = 50000 // account라는 객체에서 객체의 속성 balance의 value를 50000으로 변경함
    account.deposit(5000); // account라는 객체의 객체 속성 balance에 5000을 더함
    console.log(account.inquiry()); // account 객체 속성 balance의 현재 값을 출력함
 </code>

- 사용하기 위해서는 위에 있던 코드처럼   객체.메소드(파라미터) or 객체.메소드() or 객체.프로퍼티 = value 로 사용할 수 있고, 사용함으로써 객체 속성을 설정하거나 메소드를 실행 시킬 수 있습니다.

 
ex)   - class 선언 객체 예시 -
<code> class Account {
         constructor(owner, balance) { //  constructor는 객체가 생성되었을 떄 자동 호출개념임.
             this.owner = owner;
             this.balance = balance;
       }
 
         deposit(amount) { 
             this.balance += amount; 
       }
    } </code>
   
let acc = new Account("홍길동", 35000); // acc는 class Account의 객체가 되고  constructor으로 인해 값을 입력 받게 됩니다. -> (owner = "홍길동", balance = 35000)
acc.deposit(3000); //acc라는 class Account의 객체이므로 객체 안의 메소드인 deposit(amout)를 사용하여 이미 입력받은 balance값에 3000을 더하였습니다.

 
ex)    - 코어 객체 예시 -
<code> let today = new Date(); // 시간 정보를 다루는 Date 타입의 객체인 today 생성
       let msg = new String(“Hello”); // “Hello” 문자열을 담은 String 타입의 객체인 msg 생성
</code>
 
 - <mark> 자바 스크립트 배열 </mark> -
배열은 여러 개의 원소들을 연속적으로 저장하는 저장 공간입니다. 보통은 인덱스 0번 부터 순서대로 채워지는데, 원치 않는다면 인덱스를 지정하여 건너 띄어서 사용자가 마음대로 지정할 수도 있습니다. 자바 스크립트에서 배열 선언 방법은 대괄호([])를 쓰거나, Array객체를 사용하여 만드는 방법이 있습니다. 자바 스크립트에서 배열의 특징은 다른 언어와 다르게 여러타입 값을 섞어서 저장 할 수 있다는 점입니다. 그리고 배열은 순서를 역순으로 하거나, 추가, 일부 영역 출력, 정렬 등의 기능을 구현 할 수도 있습니다.

<b>대괄호 배열 선언 방법</b> -
let week = [“월”, “화”, “수”, “목”, “금”, “토”, “일”];
document.write(week[0]); // week배열 인덱스 0인 "월"을 출력합니다.

- 배열의 시작 인덱스는 인덱스 0부터입니다.
 
<b>Array 배열 선언 방법</b> -
 let num = Array[2] // 크기 2인 배열의 객체인 num을 만듭니다.
 num[1] = 1; // 배열에서 인덱스 1 자리에 정수타입인 1을 넣습니다.  
 num[0] = "zero"; // 배열에서 인덱스 0자리에 문자열타입인 "zero"를 넣습니다. -> num["zero", 1] 

 - 이런식으로 배열에 다른 언어와 달리, 자바스크립트는 여러 타입을 섞어서 배열을 만들 수 있습니다.

<b>배열 객체의 메소드</b> -
배열 객체의 메소드란 배열에 내장되어 있는 함수를 객체에 적용 시키는 것입니다. 이를 사용하여 배치의 순서, 추가, 일부 영역 가져오기 등의 기능을 구현할 수 있습니다. 
함수에는  객체.sort (정렬), 객체.reverse (역순), 객체1.concat(value1, value2...) (배열의 추가), 객체.slice(num1, num2) (배열 일부 영역 가져오기) 등이 있습니다.    
 
<b>코어 객체 Date</b> -
Date는 자바스크립트의 코어 객체 중 하나로, 날짜와 시간을 처리하기 위한 객체입니다. new Date()를 사용해 객체를 생성하면 현재 날짜와 시간을 알 수 있습니다.
그리고 구하고자 하는 형식도 지정하여 구할 수 있습니다. 만약 시간만 따로 알고 싶으면 "객체.getHours", 달을 알고 싶다면 "객체.getMonth" 을 사용하여 따로 구할 수 
있고, 다른 날짜관련, 혹은 시간 관련에서 따로 구할 수 도 있습니다. 방금 적은건 사용할 수 있는 코드의 극히 일부입니다. 

 <b>코어 객체 Math</b> -
수학 계산을 위한 프로퍼티와 메소드 제공하고, new Math()로 객체 생성하지 않고 사용할 수 있습니다.
ex) let sq = Math.sqrt(4); // 제곱근 구하는 Math객체
    let area = Math.PI; // PI를 활용한 Math객체 생성
    document.write(Math.Pi) // 객체 생성 없이 PI값만 출력함
 
- <mark>문자열 객체</mark> -
문자열 객체는 지정한 문자열을 객체에 담는 것 입니다. 문자열 객체를 만드는 방법은 총 2가지가 있습니다. 한가지는 new String을 선언하여 그 안에 문자열을 넣는 방식이고, 아니면 바로 변수에 문자열을 넣는 방법이 있습니다.

 ex)  - new String 선언 문자열 객체 -
     let S = new String("안녕") // String 객체인 S가 "안녕" 이라는 문자열을 저장합니다"

     - 변수에 문자열 바로 넣기 -
     let A = "All" // 변수 A에 "All"이라는 문자열을 저장합니다.

 
자바 스크립트와 다른 언어에서 차이점이 문자열 객체에서 도드라지는데, 다른 언어는 문자열을 변수에 선언 하였어도, 똑같은 변수에 다른 문자열이 선언되게 되면, 후에 들어온 문자열이 해당 변수에 저장되게 됩니다. 하지만 자바 스크립트는 문자열을 객체에 저장하면 절대 바뀌지 않는 특징을 가지고 있습니다. 

ex)   - 자바 스크립트 문자열 변경 확인 예시(1) - 
      let str = new String("Hello"); 
      str[0] = "Y";      // 문자열 첫번째 문자를 Y로 변경 시도
      document.write(str + "<br>"); // 출력 할떄 변경이 되지 않고, 문자열 그대로 "Hello"가 출력 됨

      - 자바 스크립트 문자열 변경 확인 예시(2) -
     let A = new String(“Hello”); // 문자열 객체 A에 "Hello" 저장
     let B = A.concat(“Javascript”); // 문자열 객체 A에서 문자 "Javascript"를 뒤에 추가하고 객체 B에 저장
     document.write(A) // A에 있는 "Hello" 출력 

 - "자바 스크립트 문자열 변경 확인 예시(2)" 에서 쉽게 이해 하는 방법은 파이썬에서 sorted를 써서 기존에 있던 배열은 그대로 두고, 정렬된 배열만 다른 배열에 넣습니다. 이 예시랑 비슷한 원리라고 보시면 됩니다.
 

 
7장 p10, p13, p18, p23 다른 예제문제도 풀어보기


교재 이론문제 실습문제, 인의예지신과 중도(각각 인의예지신)에 대해서 서술하시오.
</pre>
