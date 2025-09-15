-emmet정의 -                                                                                                                                            
Emmet은 HTML, CSS 등의 코드 작성 속도를 빠르게 해주는 도구로써, 지정 되어 있는 문자에 형식을 더하면 자동으로 문장이 완성됩니다. 지정 되어 있는                                         
문자에는 여러개가 있는데 그 중 몇가지만 살펴 보자면 Child: >, Multiplication: *, Sibling: +, numbering: $, Climb-up: ^, Grouping: () 가 있습니다.                                 
                                                                                                                                                                                            
1) emmet chlid : >                                                                                                                                                         
child는 부모/자식 관계로써 A > B라고 하면 A안에 B가 속해 있는걸 뜻합니다.                                                                                                                                                                                                                      
```html
<nav>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
    </ul>
</nav>
```
예시로 emmet 코드를 활용하여 nav>ul>li 쓰면 부모 자식관계로 나타나 지는걸 볼 수 있습니다.                                                          
                                                                                                                                   
2) emmet Multiplication: *                                                                                                        
 Multiplication은 곱셈으로써 A * n (n은 자연수)라고 하면 A가 n개 만들어 지는것을 뜻합니다.                                                                              
```html
<li> </il> 
<li> </il> 
<li> </il>
```    
예시로 emmet 코드를 활용해 li * 3 쓰면 보이는 것과 같이 li가 3개가 만들어 집니다.                          

3) emmet Sibling: + 
Sibling은 형제관계로써 같은 위치에 만들어 지는걸 뜻합니다.
예시로 emmet 코드를 활용해 div+p+bq을 쓰면
```html
<div></div>
    <p></p>
    <blockquote></blockquote>
```
앞에 보이는 것과 같이 부모도 아니고, 자식도 아닌 형제관계가 만들어집니다. 

4) emmet Climb-up: ^ 
Climb-up은 한 단계 부모로 올라가서 그 부모 안에 형제 추가입니다.
예시로 nav>ul^li 쓰면
```html
<nav> 
<ul> </ul> 
<li> </li>
<nav>
```
nl ^ li에서 li는 nl보다 1레벨이 낮아 부모쪽으로 올라오니 li와 nl은 형제가 됩니다.
만약에 nl^^li을 쓰게 되면 li은 nl의 부모자식관계는 아니지만, nl의 부모인 nav와 li는 형제관계가 됩니다.

5) emmet numbering: $ 
numbering은 반복되는 요소 안에서 번호를 붙을수 있는 기능입니다.
```html
<li class="item1"></li>
<li class="item2"></li>
<li class="item3"></li>
```
예시로 li.item$*3를 쓰면 자동으로 1~3까지가 출력이 됩니다.

6) emmet Grouping: () - 
Grouping은 여러 개체를 하나로 묶고, 반복 작업이나 부모자식관계를 설정할때 활용됩니다.
```html
<div>
<p></p>
</div>
    
<div>
<p></p>
</div>
```
예시로 (div>p)*2 있으면 div와 p는 부모 자식관계인데 그룹으로 지정해서 두번 반복하게 설정이 되어 있습니다.                                                                       
                                                                                                             
- HTML(!DOCTYPE html)-                                                                                                                                                                                     
(!DOCTYPE html)는 HTML5 문서임을 선언하는 선언문입니다. 반드시 첫 문장에 있어야하고, 이 선언을 통해 브라우저는 표준 모드 해석 할 수 있습니다.                                                     

- HTML meta-                                                                                                                                 
meta는 문서 전체를 설명하는 부분으로써 주로 <meta charset="UTF-8">(문서를 UTF-8로 해석), 문서 정보, 반응형 화면 설정으로 사용됩니다.                                                           
                                                                                                                                                                     
- HTML img-                                                                                                                                                 
이미지를 삽입하는 HTML태그로써 (img src="이미지경로.png/jpg" alt="이미지 설명") 이미지를 화면에 출력하고 싶을 때 사용되며 예시에 나오는 alt는 이미지를 출력하는 화면에 불러오지 못 했을시 나타나는 문구으로써 alt가 없으면 태그를 실행하지 못합니다. 
                                                                                                                                                                       
- HTML (pre) -  
white characters라고 하는 balnk, tab, new line들은 모두 한개의 빈칸으로 표현되어 집니다. 원본 그대로의 문자를 출력하고 싶다고 하면 pre태그 안에 문자, 문자열을 넣어주면 각자의 특성에 맞게 그대로 출력이 됩니다. 

- HTML list-                                                                                                                               
HTML list는 순서있는 리스트(ol), 순서 없는 리스트(ul), 정의 리스트(dl) 총 3가지 있습니다.                                                                    
먼저 ol은 (ol type="문자"), (ol type =숫자)를 사용하며 그 기준에 맞게 내림차순으로 list가 생성이 됩니다.                                                                                                                   
ul은 순서가 없으므로 (li)만 있으면 형제의 개수에 맞게 그 앞에 마커를 생성합니다.
dl은 (dl)안에 (dt), (dd)가 있으며, dt는 머리글, dd는 머리글에 대한 내용을 뜻합니다. dt와 dd는 여러개 지정 할수 있고, 무조권 dl이 부모자식 관계여야 사용 가능합니다.                                           
                                                                                                                                                             
- HTML 하이퍼링크 -                                                                                                                                       
하이퍼링크는 다른 페이지나, url로 이동할수 있는 링크입니다. (a href="url")링크 텍스트(/a) 구조로 되어있습니다. 링크 택스트는 그 자리에 문자를 입력하면 url클릭부분이 입력된 문자로 바뀌고, 클릭 시 해당 url로 이동하게 되는 방식입니다.
만약 링크택스트를 넣지않는다면 화면에 아무것도 보이지 않아, 해당 url로 이동이 불가합니다. 

- HTML block태그 -
div, p, li등이 있으며, 자식 요소를 포함할 수 있는 특성을 가지고 있고, 문서 구조를 나누거나 구획할 때 주로 사용합니다.                                     
                  
- HTML inline태그 -                                                                                                                                                                                           
span, a등이 있으며 줄을 나누지 않고, 내용과 같은 줄에 이어서 표시하고, 자식 요소로 블록 태그를 포함할 수 없기에 주로 텍스트 꾸미기, 링크, 이미지 등에 사용합니다. 

-HTML class, ID -                                                                                                                 
class와 ID는 (p), (span), (a), (img), (ul), (div) 등 여러 태그에 붙여서 사용 가능합니다. class는 식별이 필요 없을 때 사용하고, ID는 서로간의 식별이 필요 있을 때 사용합니다. 그렇기에 class는 같은 이름의 클래스 중복 가능한데, 반대로 ID는 독보적인 구조를 가집니다. 

  메타데이, 리스트(중첩가능), 
  테이블의 중요(tr안에 동인한 th가 있어야함) , 콜스펜, 로스팬, 하이퍼링크(target), Iframe, 오디어(선택 재생 가능은 재생가능한지 위에 부터 실행)
  
  

