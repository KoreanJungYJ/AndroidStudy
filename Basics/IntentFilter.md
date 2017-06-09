인텐트 필터란?

: 인텐트 필터는 특정 인텐트를 받을지 말지를 정의하는 역할을 수행하는 요소이다. 
이를 통해 컴포넌트의 특징이 정해진다고 한다.

-예시-

    1. android.intent.action.MAIN 선언
    2. android.intent.category.HOME 선언
    -> 해당 컴포넌트는 HOME 어플리케이션이 된다.
    -> 즉, 디바이스가 시작될 때 자동으로 시작될 수 있는 것!

**인텐트 필터는 AndroidManifest.xml에 다양하게 정의 가능!**

-구성 요소-
-> 인텐트와 동일!

-예시-

    <activity class=".NotesList" android:label="@String/title_notes_list">
        <intent-filter>
            <action android:name="android.intent.action.MAIN">
            <category android:name="android.intent.category.LAUNCHER">
        </intent-filter>
    </activity>