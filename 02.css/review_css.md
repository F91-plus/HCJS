#CSS

## <link rel="" href="">

## id = "#"     class = .

* tag 요소
    * p, h, div, li, ul, ...

* ### 선택자
    * 복합선택자
    * li.berry
    
    * 하위선택자
    * .fuits li

    * 인접 형제선택자
    * .berry + li

    * 일반 형제 선택자
    * .berry ~ li

* ### 가상 클래스
    * 방문했을 때
    * a:visited

    * 마우스 올렸을 때
    * a:hover

    * 마우스 눌렀을 때
    * a:active

* ### 텍스트 입력 상태
    * input:focus

* ### li 활용
    * .fruits li:first-child
    * .fruits li:nth-child(1)
    * .fruits li:last-child
    * .fruits p:nth-of-type(1)
    * .fruits li:not(.berry)

* ### 가상요소 선택자 ::
    * .before li::before

* ### 속성 선택자 []
    * [class^="btn-"]
    * [class$="success"]
    * [class$="danger"]

* ### 간편기능
   * 자식 노드 생성 : a>b
   * 형제 노드 생성 : a+b
   * 반복 생성      : a*10
   * id, class 적용 : div.name  /   div#name
   * 넘버 순차 적용 : $
   * 태그안 내용설정: {}

* ### margin, padding... 순서
 * 위 우 아래 좌
 * 위 [좌 우] 아래
 * [위 아래] [좌 우]
 * [위 아래 좌 우]

 * ### 중앙정렬
    * 텍스트    : text-align : center
    * img      : vertical-align: middle
    * 블록      : margin-left,right : auto
    * 아이템?   : align-items : center


* ## 사용했음
font-family         : 글꼴 전체 설정
font-style          : 글꼴 변경
color               : 텍스트 색상 변경
background-color    :
background-size     : 
background-image    :
background-repeat   :
background-position : 
background-attachment
list-style-type     : li에서 list 특성 설정
list-style
max-width           : 최대 너비 설정 이상 안커짐
min-width           : 최소 너비 설정 이하 안작아짐
max-height
min-height
margin          
text-decoration     : a 태그에서 특성 설정
box-sizing          : 
display             : 화면 설정    flex, block, inline-bloc, ...
flex=justify-content=align-items
block=margin-left/right
inline-block=vertical-align
position            : 요소의 위치 지정의 기준 설정
float               : 가로 정렬 (ul::after= content:'', display:block,clear:both)
overflow            : 현재 창보다 내용이 많을 때 스크롤 바 만듬
opacity             : 투명도 설정 0~1 위치는 그대로 있음
flex-direction      : 주축, 교차축
flex-wrap           : 줄넘김 처리
flex-grow           : 증가 너비 비율 설정
flex-shrink         : 감소 너비 비율 설정
flex-basis          : 공간 배분전 기본 너비 설정
transition          : css로 시작과 끝으로 동적인 효과 적용 ? 시간 특성
transform           : 원근법 이동 크기 회전 기울임       x, y
@keyframes [name]   : 애니메이션 스타일 지정 0 ~ 100%
animation           : [name] n초만에 n초마다 n번 반복
@media screen and (max/min-width : npx) : 미디어 설정

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.2/css/all.min.css" integrity="sha512-1sCRPdkRXhBV2PBLUdRb4tMg1w2YPf37qatUFeS7zlBy7jJI8Lf4VHwWfZZfpXtYSLy85pkm9GaYVYMfw5BC1A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
i                   : 인터넷에서 아이콘 사용, 링크 연결 필수, class로 불러옴
scroll-snap-align   : 스크롤 움직인 후 지정한 값으로 이동
z-index             : 화면 출력 순서 지정, 숫자가 클수록 순서가 뒤로감
:root {}            :커스텀 함수 설정, --이름 :값
