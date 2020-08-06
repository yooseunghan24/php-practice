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
### URL 규칙(php뿐만 아니라 모든 url에 해당됨)
- ? 뒤에 오는 값들은 parameter라고 함. &로 구분.
```
http://127.0.0.1/parameter.php?name=hello&address=서울
안녕하세요 <?php echo $_GET['address'];?>에 사시는 <?php echo $_GET['name'];?>님
```
