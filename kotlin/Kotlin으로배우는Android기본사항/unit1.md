### [Kotlin Playground](https://developer.android.com/training/kotlinplayground?hl=ko)

- Java와 마찬가지로 main 함수가 있어야 Kotlin도 실행이 된다.

- `val` : 선언된 변수는 한 번만 설정할 수 있다. 프로그램 후반부에 값을 변경할 수 없다.
- `var` : 변경 가능한 변수를 선언할 수 있다.
변수의 값을 사용할 때는 `${variable}` 형식으로 사용




### [함수명 작명 규칙](https://developer.android.com/kotlin/style-guide)
- 소문자 동사로 시작. 이름은 함수가 하는 작업을 설명해야 한다. `ex) printBorder()`
- 카멜표기법으로 작성 `ex) drawReallyCoolFancyBorder()`

- Top-down Development : 큰 그림에서부터 세부적으로 개발해나가는 방식
- 리팩터링 : 출력을 변경하지 않고 더 효율적으로 또는 더 쉽게 작업할 수 있도록 코드를 변경하는 것


### 반복문(loop)
- 중첩 루프를 만들 수도 있다.
```
repeat(반복횟수) {
  
}
```


### 함수 파라미터 정의 방식
- 괄호 안에 `인수명 : 인수종류`
- 여러개 인수를 정의할 때에도 쉼표로 구분
```
fun printBorder(repeatTime : Int, border : String){
  ...
}
```

요약
- `${}`를 사용하여 print 문 텍스트의 변수와 계산 값을 둘러쌉니다. 예를 들어 `${age}`에서 `age`가 변수입니다.
- `val` 키워드와 이름을 사용하여 변수를 만듭니다. 설정이 완료되면 변경할 수 없습니다. 등호를 사용하여 변수에 값을 할당합니다. 값의 예로는 텍스트와 숫자가 있습니다.
- `String`은 `"Hello"`와 같이 따옴표로 묶인 텍스트입니다.
- `Int`는 양의 정수 또는 음의 정수(예: 0, 23, -1024)입니다.
- 함수에서 사용할 인수 한 개 이상을 함수에 전달할 수 있습니다. 예:`fun printCakeBottom(age:Int, layers:Int) {}`
- `repeat() {}` 문을 사용하여 일련의 명령어를 여러 번 반복합니다. 예를 들면 `repeat (23) { print("%") }` 또는 `repeat (layers) { print("@@@@@@@@@@") }`이 있습니다.
- 루프는 명령어를 여러 번 반복하는 명령어입니다. `repeat()` 문은 루프의 예입니다.
- 루프를 중첩할 수 있습니다. 즉, 루프 내에 루프를 배치할 수 있습니다. 예를 들어 `repeat()` 문 내에 `repeat()` 문을 만들어 케이크 층을 만들 때처럼 여러 행에 걸쳐 기호를 여러 번 출력할 수 있습니다.

함수 인수 사용 요약: 함수에 인수를 사용하려면 다음 세 가지 작업을 실행해야 합니다.
- 함수 정의에 인수와 유형을 추가합니다. `printBorder(border: String)`
- 함수 내에서 인수를 사용합니다. `println(border)`
- 함수 호출 시 인수를 제공합니다. `printBorder(border)`




[Kotlin에서 사용되는 Android 기초 용어](https://developer.android.com/courses/android-basics-kotlin/android-basics-kotlin-vocab?hl=ko)
[변수정의](https://kotlinlang.org/docs/reference/basic-syntax.html#defining-variables)
[주석](https://kotlinlang.org/docs/reference/basic-syntax.html#comments)
[함수정의](https://kotlinlang.org/docs/reference/basic-syntax.html#defining-functions)
[repeat](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/repeat.html)

