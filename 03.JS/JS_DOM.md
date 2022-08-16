# JS_DOM 정리, Part03
* DOM : documnet object model
* HTML 문서의 모든 요소를 객체로 만들어 사용하도록 여러 기능을 제공하는 모델

## 기본 규칙? getElementBy ~
* const A = document.B('C');
 * A = 변수명 지정
 * B = C타입에 따라 getElement[Id, Class, Tag, Name]
 * C = HTML의 속성 이름 또는 태그이름

## querySelector
* document.querySelector('A').B
 * A = HTML의 아이디,클래스,태그이다.  앞에 각각의 기호를 붙여서 사용한다.
 * B = 아벤트 옵션

## addEventListener
* 같은 기능 등록 가능
* A.addEventListener('B', (C) => {D})
 * A = getElementBy~ 의 변수명
 * B = 사용할 이벤트
 * C = ?
 * D = 코드

## document 객체
* title1.style.color = "gold";
* titles[2].style.color = "tomato";
* title1 관 titles는 const 로 지정해주고 사용

## 요소(element) 생성/추가/삭제/...
* HTML <div id="aTag"></div>
* const A = document.getElementById('B');
* aTag.innerHTML = '<a href="#">링크</a>'
 * A = 생성할 document 객체
 * B = HTML 에서 지정할 id
 * 설명 : div aTag에 해당되는 HTML코드에 a~ 링크/a 코드가 추가된다.
 
* const A = document.createElemnet('B');
 * A = 생성할 document 객체
 * B = HTML 에서 지정할 곳(태그?)
* h3.innerHTML = 'createElement h3';
* document.body.appendChild(h3);
 * 설명 : HTML 에서 없는 요소를 생성, body의 자식요소에 h3 위치시킴

## 속성(Attribute)
* set 추가 = h3에 data-id="test" 라는 속성을 추가
 * h3.setAttribute('A', "B");
  * 설명 : h3는 const로 만들어주었음, A=data-id, B=test => HTML의 h3 태그에 추가된다.
* get
* has
 * 도 있음

## 텍스트
* 프로퍼티 = innerHTML, innerText, textContent
 * innerHTML : 자주 사용, HTML에 해당 내용을 추가
 * innerText : 단순 텍스트 추가이나 보안문제로 HTML로 사용
 * textContent : 내용 추가, 그 외 별건 없으므로 HTML로 사용

## Child
* appendChild(추가) / removeChild(삭제) / replaceChild(A, B)(B를 A로 변경)
 *  removeChild()는 노드를 삭제하는 것이 아니라 메모리에 해당 노드는 그대로 존재하며, 부모 노드와의 부모-자식관계를 끊어 DOM 트리에서 해제하는 것입니다

## Node
* DOM 표준에 나와있는 HTML의 모든 요소
 * 문서노드 : document
 * 요소노드 : HTML 태그 각각의 요소
 * 텍스트노드 : HTML 요소 내부의 텍스트
 * 속성노드 : HTML 속성
 * 주석노드 : 주석
 * 루트노드 : HTML 태그
* Node 선택
 * A.previousSibling
  * A = document 객체, A 이전 선택
 * A.nextSibling
  * A = document 객체, A 이후 선택

## mouse 및 기본 이벤트 사용
* step01 인라인 방식        : function 함수이름() {}
* step02 프로퍼티 방식      : A.onclick = function 함수이름() {}   A=document 객체, 같은 이벤트 중복 등록 불가능
* step03 addEventListener  : A.addEventListener('click', ()=>{}); A=document 객체, 같은 이벤트 중복 등록 가능

## Mouse 이벤트
* click, dblclick, mouseover, mouseup, mousedown... 많음
* addEventListener 형식으로 옵션 선택해서 사용하자

## classList
* A.classList.B('C');
 * A = document 객체, B=옵션(remove, add), C= HTML 지정0
* checkService.classList.remove('hide');

## Focus
* 마우스 초점 클릭시 이벤트 발생
## contains
* 해당 이름(id, class, tag) 포함되어 있는지 확인
## includes
* 값에 포함되어 있는지 확인

## this, target
* 일반함수 : function(e) {}   : e.target = 이벤트, this = 자신을 가르킴
* 화살표함수 :  (e) => {}     : e.target = 이벤트, this = window(브라우저)를 가르킴

##  e는 event의 약자
* DOM과 관련되어 발생한 이벤트 정보를 저장하는 객체
* menu.addEventListener('click', (e) => {}

## 흐름
* preventDefault : 
* stopPropagation : 다른요소로 이벤트 전파 방지

## 모바일인지 PC인지 구분함
* navigator.userAgent.match(moblie_keys[i]

## 예시
* const btn_plus = document.querySelector('#btn-plus');
* const btn_minus = document.querySelector('#btn-minus');
* const result_val = document.getElementById('result');
* coupon.value = coupon.value.toUpperCase();
* check.addEventListener('click', () => {
            document.querySelector('#content').innerHTML = "조회 서비스";
        });
* 