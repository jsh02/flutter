## 시작하기


lib 폴더 속 main.dart 파일이 플러터 메인 파일
(lib 이 안보일 경우 android 로 설정되어있음 project 로 변경)


## 다트 언어의 특징

1.다트는 main 함수로 시작한다 
2.다트는 어디에서나 변수 선언과 사용 가능


문자열 안에서 \n 사용가능

## 위젯설명

Container 위젯 : 자식을 담는 컨테이너 역할 **배경색, 너비와 높이, 테두리 등의 디자인**을 지정할 수 있다
GestureDetector 위젯 : 탭이나 드래그 그리고 더블 클릭 같은 제스처 기능이 자식 위젯에 인식됐을 때 함수를 실행할 수 있습니다.
SizedBox 위젯 : 높이와 너비를 지정하는 위젯 Container 위젯과는 다르게 디자인 적 요소는 **적용할 수 없고** const 생성자로 선언할 수 있어서 퍼포먼스 측면에서 더 효율적

Column 위젯 : children 매개변수에 입력된 모든 위젯들을 **세로**로 배치
Row 위젯 : children 매개변수에 입력된 모든 위젯들을 **가로**로 배치
ListView 위젯 : 리스트를 구현 할 때 사용, 입력된 위젯이 **화면을 벗어나게 되면 스크롤이 가능**


## StatelessWidget vs StatefulWidget

***StatelessWidget
필수적으로 build()함수 실행
위젯값은 불변 이므로 만약 변경된 값이 필요하다면 build 함수 자체를 재 실행

*** StatefulWidget

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
   
클릭 시 실행 -> onPressed: (){}
버튼 스타일 -> style: TextButton.styleFrom()      주색상 지정 -> foregroundColor: Colors.(입력)
버튼 스타일 -> style: OutlinedButton.styleFrom()  주색상 지정 -> foregroundColor: Colors.(입력)
버튼 스타일 -> style: ElevatedButton.styleFrom()  주색상 지정 -> backgroundColor: Colors.(입력)

버튼에 넣을 위젯 -> child: Text(입력)

***Container

스타일 작용 -> decoration : BoxDecoration ()
배경색 작용 -> color.Colors.(입력)
테두리 작용 -> border: Border.all()
모서리 둥글게 만들기 -> borderRadius : BorderRadius.circular(입력)

***배치
Column 세로 배치 -> 위젯을 세로로 배치
Row  가로 배치 -> 위젯을 가로로 배치

mainAxisAlignment: MainAxisAlignment.start  ->  시작에 정렬
mainAxisAlignment: MainAxisAlignment.center ->  중앙에 정렬
mainAxisAlignment: MainAxisAlignment.end    ->  끝에 정렬

***이미지
자신이 만든 상위 폴더에서 New 를 누르고 Directory 에다가 assets 폴더 만들기
이후 이 assets 폴더를 pubspec.yaml 파일에 지정하기 이 파일 안에 assets : 주석처리되어있는거 해제 후
assets:
  - assets/

이후 위젯을 Image.assets( 이 안에 asset/'이미지이름') 





