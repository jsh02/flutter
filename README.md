***시작하기
lib 폴더 속 main.dart 파일이 플러터 메인 파



***다트 언어의 특징

1.다트는 main 함수로 시작한다
2.다트는 어디에서나 변수 선언과 사용 가능


문자열 안에서 \n 사용가능


문자열의 위치를 바꾸고 싶을 때는 Center() 함수 / 

child 옵션은 어떤 위젯을 넣겠다.
childern 여러 옵션을 넣고 싶을 때 

// 글자를 화면 가운데 맞춤
home : Center(
  child: Text('넣고 싶은 문자열' , textAlign: TextAlign.center // 글자 가운데 맞춤)
));

Text('넣고 싶은 문자열' , textAlign: TextAlign.center // 글자 가운데 맞춤)


Container 로 화면 구성 설정 
home: Container(
  color: Colors.white, // 배경색 바꾸기 
  child: Center(
    child: Text('hello\nFlutter', textAlign: TextAlign.center),
  ))


// Text 안에 style 태그를 넣어서 그 안에 fontSisze나 color 를 정해줌 
child: Text(
    'hello\nFlutter',
    textAlign: TextAlign.center,
    style: TextStyle(color:  Colors.blue, fontSize: 20),
),

***Text
글자 크기 -> fontSize : (입력)
글자 굵기 -> fontWeight : FontWeight.w(입력)
글자 색상 -> color : Colors.(입력)

***Button 
버튼의 종류 
1) TextButton 텍스트만 있는 버튼
2) OutlinedButton 테두리가 있는 버튼
3) ElevatedButton 입체적으로 튀어나온 느낌의 버튼
   
