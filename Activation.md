컴포넌트의 활성화 및 비활성화

: 일반적으로 처음 시작되는 메인 액티비티(Activity)는 애플리케이션을
실행할 때 시작되며 다른 액티비티들은 인텐트(Intent)를 통해 시작할
수 있다.
다만 콘텐트 프로바이더는 콘텐트 리졸버(ContentResolver)를 통해서
시작된다.

**콘텐트 리졸버**: <https://developer.android.com/reference/android/content/Intent.html?q=ContentResolver>참고!


    Activity,
    Service,
    Broadcast Receiver: 인텐트(Intent)에 의해 활성화된다.

    Content provider: 콘텐트 리졸버(ContentResolver)에 의해 활성화된다.

**특별 경우**
액티비티(Activity)와 서비스(Service)를 위한 인텐트는 액션과 URI
정보가 필요하다. 또한 브로드캐스트 리시버(BroadCast Receiver)를
위한 인텐트는 액션 정보가 필요하다.

    -Activity-
    : Context.startActivity()나 Activity.startActivityForResult()에 인텐트 객체를 전달해서 활성화 시킴.

    -Service-
    : Context.startService()에 인텐트 객체를 전달해서 활성화 시킴.
    설명이 필요;-> 안드로이드는 인텐트 객체를 Service의 onStart() 메소드에 전달한다.

    -BroadCastReceiver-
    : Context.sendBroadCast(), sendOrderedBroadCast(), sendStickyBroadCast()에 인텐트 객체를 넘겨서 활성화

**단!!**, 브로드캐스트 리시버의 경우에는 인텐트 필터를 AndroidManifest.xml
에 지정해 놓을 시, 조건이 맞을시 명시적으로 호출하지 않아도 알아서
활성화될 수 있다는 것이다.


**비활성화**되는 경우
: 메모리가 부족하거나 기타 여러 이유들로 안드로이드는 Activity를 
비활성화시킨다.

컴포넌트를 직접 비활성화시키고 싶으면 액티비티에서는 **finish()**메소드, 서비스에서는 **stopSelf()**메소드를 호출해야 한다.

또한 브로드캐스트 리시버나 콘텐트 프로바이더 같은 경우에는 메시지나 요청의 **응답 시에만** 활성화 되기 때문에 명시적으로 비활성화시킬
필요가 없다!!!