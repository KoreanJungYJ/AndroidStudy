**액티비티란?**
: 액티비티(Activity)는 사용자 인터페이스 화면을 관리하는 컴포넌트이다.
액티비티의 역할을 하기 위해서는 Activity 클래스를 상속해야 하며,
액티비티가 기본적으로 가지고 있는 **생명주기** 메소드를 재정의해서
원하는 기능을 구현해야 한다.

    public class ActivityEx extends Activity{
        @Override
        public void onCreate(Bundle savedInstanceState){
            super.onCreate(savedInstanceState);
            setContentView(R.layout.main);
        }
    }

    알 수 있는 것
    1. onCreate()메소드는 setContentView의 메소드를 호출한다.
    2. setContentView()메소드는 R.layout.main을 가지고 화면 구상을 한다.
    3. R.layout.main은 실제로 /res/layout/main.xml을 가리킨다.

기본적으로 xml파일은 화면에 보이는 **레이아웃**을 정의하는 역할을 한다.

LinearLayout: 내부에 정의된 뷰(View)들을 수직 혹은 수평으로
나열하는 역할을 한다.
-> 만약 android:orientation="vertical"로 정의되어 있으면  뷰들이
수직 방향으로 보여지게 되며,
android:orientation="horizontal"이면 수평방향으로
보여지게 된다.

**액티비티의 특징**
1. 액티비티의 크기는 상태바(Status Bar)영역을 제외한 화면 전체로 고정한다.
즉, 원하는 위치에 원하는 크기로 변경할 수 없다는 의미!

2. 두 개의 액티비티를 동시에 보여주는 것은 불가능!

3. 다른 애플리케이션의 액티비티를 불러올 순 없다.

4. 액티비티 내에서 프래그먼트(Fragment-UI Component)를
추가하여 화면을 분할하거나 별도로 조작할 수 있다.


**About R.layout.main**
위의 예제에서  R.layout.main으로 화면 구성을 한다는 것을
알 수 있는데 이 때 R은 R 클래스(R.java)내에 작성되어 있는
정적 클래스의 정적 변수를 가리킨다.
R 클래스는 빌드 시 자동으로 생성되며, 이 클래스는
리소스를 int값으로 관리하는 역할을 한다.(**리소스의 효율적 접근!**)
R.java 파일은 수정하면 안되며, 수정한다 하더라도
그 내용이 적용되지 않는다!