# php 메모
echo, print로 출력 가능.
'.'으로 문자열 연결 가능. '+'는 안됨.
```
<?php
$txt1 = "Learn PHP";
echo "<h2>" . $txt1 . "</h2>";
print "<h2>" . $txt1 . "</h2>";
?>
```
- 함수 밖에 선언한 변수는 함수 밖에서만 접근할 수 있음. 함수 안에 선언한 변수는 함수 안에서만 접근 가능.(자바스크립트는 함수 밖에서 선언한 변수를 함수 안에서도 접근할 수 있었는데 php는 안됨).
- 이것을 해결하기 위해 **global** 키워드를 사용함. global 키워드를 사용하면 함수 안에서도 전역 변수에 접근할 수 있음.
- **$GLOBALS[index]** 사용해서 접근할 수도 있음. 예) $GLOBALS['x']
- 변수 앞에 **static** 쓰면 함수가 끝나도 변수 값이 사라지지 않음.
# URL 규칙(php뿐만 아니라 모든 url에 해당됨)
- ? 뒤에 오는 값들은 parameter라고 함. &로 구분.
```
http://127.0.0.1/parameter.php?name=hello&address=서울
안녕하세요 <?php echo $_GET['address'];?>에 사시는 <?php echo $_GET['name'];?>님
```
# 함수
- strlen() 글자 수 세기.
- nl2br() 내가 입력한 대로 출력됨(줄바꿈 됨).
- file_get_contents() 파일 읽는 함수.
- var_dump() 괄호 안의 데이터를 출력하고 그 데이터의 타입도 알려줌.
- isset() 괄호 안의 데이터의 참,거짓 판별.
- scandir('./directory') directory의 하위 문서들을 스캔해서 배열로 가져옴.
- **require보다는 require_once 쓰는 것이 정신건강에 이롭다.** 왜냐? php는 같은 함수 재선언을 못하기 때문에
- 함수 작성방법
```
function sum($left, $right) { // $left, $right는 parameter(매개변수)라고 불림
    print($left+$right);
    print("<br>");
  }
  sum(2,4); // 결과: 6
  // sum 안의 2와 4는 arguments(인자) 라고 불림
```
매개변수에 $를 붙여서 변수로 만들어줘야 함. 그냥 left, right만 쓰면 에러남.
- echo htmlspecialchars(); XSS 방지(괄호 안에 방지할 것 써야함)
- basename(); 파일 경로는 안보이게 하고 파일명만 보이게 할 수 있음.
## php는 API를 잘 활용해야 한다.
