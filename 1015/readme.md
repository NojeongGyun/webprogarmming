<pre>- <mark> 자바 스크립트 객체 </mark> -
객체란 만들어진 틀 안에서 프로퍼티의 속성과 메소드를 정하는 것을 활용하는 매체를 말합니다. 사용 할때 마다 틀 안에서 다르게 속성, 메소드를 활용할 수 있는 장점이 있습니다. 
몇가지 여기서 쓰는 용어를 알아보자면 class의 변수를 프로퍼티 라고 하고, class 변수를 다루는 함수를 메소드라고 하고, 객체 생성 연산자를 추가 할떄 new 객체를 사용합니다.
객체를 만들려면 let 선언을 하여 만들어도 되고, class 정의로 하여 만들어도 되고, 또한 이미 구현되어 있는 코어 객체로 사용하여도 됩니다.

- let선언 객체 -
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
배열은 여러 개의 원소들을 연속적으로 저장하는 저장 공간입니다. 보통은 인덱스 0번 부터 순서대로 채워지는데, 원치 않는다면 인덱스를 지정하여 건너 띄어서 사용자가 마음대로 지정할 수 도 있습니다. 자바 스크립트에서 배열 선언 방법은 




자바 스크립트는 배열을 대괄호를 이용함( [ ] )
다른언어는 한 배열에 똑같은 데이터 타입을 써야하는데, 자바 스크립트 한정으로 배열에 여러 타입의 데이터 섞여 저장이 가능합니다.
 c = a.toString(); -> a의 배열을 c에 넣음 (a, b, c..)
 string 객체는 절대 바뀌지 않음(파이썬에서 sorted 하는거랑 같음) p19
 string 객체에서 .charAt(A) 를 쓰면 string 객체에서 A인덱스 문자를 출력합니다.
 string 객체에서 .indexOf("s") 를 쓰면 string 객체에서 "s"의 문자 위치를 출력합니다.
 string 객체에서 slice(5,8)를 쓰면 인덱스 5~8을 
 
7장 p10, p13, p18, p23 다른 예제문제도 풀어보기


교재 이론문제 실습문제, 인의예지신과 중도(각각 인의예지신)에 대해서 서술하시오.
</pre>
