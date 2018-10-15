## Callback 함수

콜백 함수는 주로 함수 내부의 처리 결과값을 함수 외부로 내보낼 때 사용한다.(일종의 return문과 비슷)

<br>

콜백 함수는 특정 함수의 매개 변수 값으로 콜백 함수를 넘긴 후 처리 결과를 콜백 함수의 매개변수에 담아 콜백 함수를 호출하는 구조를 가진다.

- callback 함수의 기본구조
```
function foo (callback) {
    ...

    callback(result);
}
```
<br>

이 구조를 사용하면 **로직 구현 부분과 로직 처리 부분을 나눠 코딩할 수 있게 된다.**  이에 따라 로직 구현 부분은 동일하고 로직 처리 부분을 다양하게 처리해야 하는 경우 유용하게 사용할 수 있다.

```
function foo (var param1, var param2, callback) {

    //함수 로직 구현 부분
    var result = param1 + param2;

    //함수 로직 처리 부분
    callback(result);
}

function print1 (result) {
    document.write("print1 result = " + result);
}

function print2 (result) {
    document.write("print2 result = " + result);
}

foo(10, 20, print1);    //print1의 결과로 처리됨
foo(10, 20, print2);    //print2의 결과로 처리됨
```