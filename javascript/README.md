# 21.03.02

# 메모

* '1' + 1 = '11' (예외)
"2" > 3 -> false
더하기는 문자로 나머지는 숫자로
ex) '5' - 3 = 2

1. 자동형변환에 의지하지 않기
2. 다른 타입간의 연산시 형변환 함수 사용(string(), Number(), Boolean())


* let:변수, const:상수


* 기본형 boolean, number, string, null, undefined + symbol
파생형 function, object


* dom : html그리면서 tree구성 document object model


* outerHTML, innerHTML
document.body.innerHTML -> body태그 안에 innderhtml에 넣는다.


* !!는 피연산자를 boolean으로 변환 거짓으로 평가되는 값이 무엇인지 알아야함 (ex 0, null, "", undefined)


* dir(객체) 객체속성보여줌console에서

* Number vs pareseInt
Number("123px") -> 에러 NaN
parseInt("123px") -> 해석할수있는데까지만 123


* 피연산자 타입을 수동으로 일치시킬것
가능하면 === 또는 !== 사용
(==는 값만비교, ===는 값과타입같이비교)


* y = y||0 --> 기본값
flag && {} -->  if문대신에


* function add(a, b) {
return a+b;
}

const add = function(a,b) {return a+b;}
- function 보다는 const 함수이름 권고함


*  Array(10) - 10개짜리배열
Array(273, 12, 13, 14) - [273, 12, 13, 14]


* 함수마다 유사배열 sum(arguments)있다 arguments는 배열은 아님
```
const sumAll = function(){
    let sum = 0;
    for(let i=0; i<arguments.length; i++) {
        sum += arguments[i];
        dir(arguements);
    }
    return sum;
}
```



* 
```
(function(a,b) { return a+b;})(3, 5);    -> 8

const add = function(a, b) {return a+b;};
add(3, 5);
(add)(3, 5);
(function(a,b){return a+b;})(3,5);
```


* scope - 지역 / 전역 변수가 전부 (나중에 block레벨 추가)


* [11,1,2,3,5].sort()
하면 [1, 11, 2, 3, 5]로나옴
그래서 sort((a, b)=> a-b))해야함
섞을때는 sort((a, b) => Math.random()-0.5)) -0.5 <= x <= 0.5


* this -> 웬만하면 객체자신, window객체도 가능하긴함


* 배열 앞 shift, unshift 뒤 push, pop 가운데 splice()


* let p5 = Person('bbbbb', 1000);
-> undefined (new가 없다.)
js함수는 항상 값을 반환 반환값이 없으면 undefined


* new로 객체를 만들지 않으면 (생성된 객체가 없으면) this는 window를 가리켜서 window.age, window.name값에 들어간다


* Person객체에 Person.prototype이 존재(각 Person마다 공유됨)


* Person.prototype.toString = function(name, age) {
    return "name=" + this.name + ", age" + this.age;;
}


* typeof new String('asdf")

instanceof로 판별가능

기본형도 ()치면 객체처럼 쓸수있음 (273).toFixed(2)


* ;생략은 return 문은 조심해서쓰자


* h1.setAttribute('class', '');
h1.setAttribute('data-prop', 'first')

attribute와 property구분 잘해야함


* 형변환함수 
1, boolean(), !!
2. Number(), *1, -, parseInt(), parseFloat()
3. String(), +'' , toString()


* 배열에서 문자열사용할떄 validation안되서
enum같은역할하는 symbol씀(찾아보기)


* prototype 공통 속성이지만 static메서드는아니다 -> 인스턴스메서드(자바식), static으로 하고싶으면 선언식에 추가(다른점 다시 생각해보기 this.사용할수있는차이가있네요)


