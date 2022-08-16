# JavaScript

## 외부로부터 불러옴 
* script src="~" script

## 변수
* let
* var
* const

## 타입
* number
 * 0b... (2진수)
 * 0o... (8진수)
 * 0x... (16진수)
* string
* boolean
* symbol

## write
* ` `  ${ }
* ' '  +
* " "  +

## 연산자
* 증감연산자 ++, --
* 대입연산자 =, +=, -=, *=, /=
* 비교연산자 >, >=, !==, ===
* 논리연산자 ||, &&, !

## 조건문
* if
* switch

## 반복문
* while
* for
* for ~ of      (let i of nums)

## 배열
* let array = [1,2,"aa", ...];
* pop
* shift
* splice(inx, no, n)    : 지정 인덱스 포함한 이후 값 지정한 곳 까지 삭제 후 (n 값 대입) 
* indexof   : 해당 요소의 인덱스 값 출력
* join      : 내부 요소를 하나의 문자열 값으로 출력하고자 할 때
* find      : 테스트 함수의 조건에 맞는 첫 번째 요소 값으로 반환
* filter    : 조건에 맞는 요소들을 추려 새로운 배열 객체로 반환
* forEach   : 배열 내부의 요소를 하나하나 반복을 통해 접근
* map       : 배열 내부의 요소를 하나하나 반복을 통해 접근 + 새로운 배열을 만들어 반환
* reduce    : 배열의 합을 출력함

* let result = array.옵션(function(x,y) {});
* let result = array.옵션((x, y) => {})
## 스코프
* 변수에 접근 할 수 있는 범위 (전역, 지역)
* 함수(var), 블록(let, const)

## 호이스팅
* 코드에 선언된 변수를 상단으로 끌어 올리는 것
* 가능한 선언
 * var (undefined), 선언식 함수 : f a() {}
* 불가능한 선언
 * let, 표현식 함수 : var a = f() {}

## 오브젝트
* 객체 = 키:값 으로 구성된 프로퍼티의 집합
* 프로퍼티 키 : 프로퍼티 값
* JS내에서 기본타입(원시타입)을 제외한 모든 것
* let obj1 = {name : "tt", age:24};
* let obj2 = {};
* let obj3 = new Object();
* typeof
* valueOf
* 생성자 함수   : 대문자로 시작
* this         : 함수 내부에서 안쓰면 객체로 인식하지 못한다.
* for ~ in      : 객체의 프로퍼티키를 출력 (for of 은 불가능)
* delete

## 값에 의한 전달 / 참조에 의한 전달
## Call By Value / Call By Reference
* 얕은 복사     : 값이 변경됨
* 깊은 복사     : 값이 변경이 안됨 (array, JSON, filter, Object)
* JSON          : 내부(하위)객체 까지 깊은 복사를 함, 확인하면 false
* Object        : let dev2 = Object.assign({}, dev); 새로운 객체 만들어짐  Object.is(dev.car, dev2.car); 확인 ture

## Number
* 발트인 규칙에 의해 문자열 0이 자동 형변환 됨
* isFinite      : 들어온 값이 유한수일 때 ture 출력
* isInteger     : 정수이면 true
* isNaN         : NaN 이면 true
* tofixed       : 숫자를 반올림
* toString      : 숫자를 문자열로 반환
* Math          : 수학적인 상수와 함수를 위한 내장 객체
* round         : 반올림 정수
* ceil          : 특정 소수점 자리에서 올림
* floor         : 특정 소수점 자리에서 내림
* random
* max

## Date
* new Date(년 월 일 시 분 초 밀리초);
* getFullYear() :
* getMonth
* getDay
* toDateString  : 날짜만 반환
* toTimeString  : 시간만 반환
* parse         : 문자열을 data 객체로 표현

## String
* indexOf       : 지정 문자열을 검색하여 첫번째 결과값의 인덱스를 반환
* includes      : 지정 문자열을 검색하여 존재하는 경우 true 반환
* startsWidth / endsWith : 지정문자열로 시작/끝 여부를 반환
* substring     : 지정한 범위만큼 문자열 반환
* charAt        : 지정 인덱스의 문자열 반환
* slice         : substring 같음(단, slice는 음수 사용가능)
* toUpperCase / toLowerCase : 대상 문자열을 모두 대/소 문자로 변경
* replace : 지정한 문자열을 원하는 문자열로 변경
* split : 지정 문자열을 기준으로 모두 분리하여 배열로 반환

## 암묵적 타입 변환
* 문자열 타입으로 변환 (string)
 * 숫자 -> 문자열   : 120 + ''
 * 객체 -> 문자열   : NaN + ''
 * true/false      : true + ''
* 숫자 타입으로 변환 (number)
 * 문자열 -> 숫자    : +'1' 
 * null & undefined -> 숫자 : +null, +undefined
 * 객체 -> 숫자 : +{}, +[], +false

 ## Boolean
* 거짓 판별 : 공백, 0 , null, undefined, NaN 만 false 로 판별한다.
* 1 : true

## 단축 평가 결과
* ture && value --> value
* ture || value --> true
* false && value --> false
* flase || value --> value
* true > value > false  ??
 * 예시 viewMessage = isLogin || "로그인 실패"; 조건문의 !isLogin 과 같음

## 실행 컨텍스트
* step08_context.html 참조...

## 삼항 연산자
* num > 30 ? '참' : '거짓'
* num > 30 ? function(){} : function(){}

## this 가르키는 곳
* Window    : 일반함수, 화살표 함수
* 객체 자기자신 : new 객체 함수, 객체 함수

## 함수
* fn 이름(params) {
    코드
}
* (params) => {}

## fetch
* https://axios-http.com/kr/docs/intro
## axios
* https://axios-http.com/kr/docs/intro