인텐트란?
: 컴포넌트에 액션, 데이터 등을 전달하는 메시지 객체이다.

**구성 요소**
액션(Action): 수행할 액션의 이름(ACTION_DIAL)
데이터(Data): 수행할 데이터의 URI(tel: )
카테고리(Category): 수헹할 액션에 대한 추가적인 정보
타입(Type): 수행할 인텐트 데이터의 명시적인 타입(MIME 타입, video/mpeg)
컴포넌트 이름(Component Name): 대상 컴포넌트의 완전한 클래스 이름
추가 정보(Extras): 인텐트를 다루는 컴포넌트에 추가적으로 전달할
**한 쌍**의 키 혹은 값

->이들을 활용하면 다른 App의 액티비티를 실행하거나 데이터를
전달해줄 수 있음.

**주요 액티비티 액션**
    <https://developer.android.com/reference/android/content/Intent.html#ACTION_EDIT>

    ACTION_MAIN: 시작 액티비티를 지정하기 위한 액션
    ACTION_VIEW: 데이터의 URL로 가장 적절한 액티비티를 호출하는 액션
    ACTION_DEFAULT: ACTION_VIEW와 동일하다.
    ACTION_EDIT: 어떠한 데이터를 수정하기 위해 호출하는 액션이다.
    ACTION_DELETE: 어떠한 데이터를 삭제하기 위해 호출하는 액션이다.
    ACTION_DIAL: 전화 다이얼 액티비티를 호출하는 액션이다.
    ACTION_CALL: 전화 액티비티를 호출하는 액션이다.
    ACTION_WEB_SEARCH: 웹 검색 액티비티를 호출하는 액션이다.
    ACTION_SEARCH: (전체적) 검색 액티비티를 호출하는 액션이다.
    ACTION_SENDTO: 이메일 등의 **메시지 전송**을 지정하는 액션이다.
    ACTION_ANSWER: 전화 착신을 위한 액션이다.

    -전달 시-

        Intent intent=new Intent(this, IntentCallee.class);
        intent.putExtra("name","Caden");
        intent.putExtra("age",18);
        startActivity(intent);

    -수신 시-

        Intent intent=getIntent();
        String name=intent.getStringExtra("name");
        int age=intent.getIntExtra("age",18);
