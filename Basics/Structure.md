안드로이드 애플리케이션의 구조

1. 뷰(View) : 말 그대로 화면 구성을 담당하는 영역이며, 이 영역은
 View 클래스를 상속하는 클래스를 사용해서 구성할 수 있다.

2. 모델(Model): 애플리케이션이 데이터를 저장하는 역할을 담당하며,
안드로이드에 내장된 데이터베이스와 파일, 콘텐트 프로바이더(Content Provider)가 이 영역에 속한다.

3. 컨트롤(Control): View와 Model 사이에서 둘을 서로 연결하고 제어할 수 있고,
 이 영역에서는 액티비티, 서비스, 브로드캐스트 리시버가 포함되며,
 버전 3.0(허니콤 : HoneyComb)부터 프래그먼트가 포함이 되었다.


 <img src="https://github.com/KoreanJungYJ/AndroidStudy/blob/master/Structure.PNG"> 