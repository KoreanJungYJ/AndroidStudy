브로드캐스트 리시버
: 저번에 말했던 것 처럼 시간대 변경, 배터리 부족 등 각종 알림을
띄워주는 역할을 한다. 특정 브로드캐스트에 반응하는 컴포넌트이며,
사용자 인터페이스를 가지고 있진 않다.

작동(?)
1. 브로드캐스트를 받음.
2. 리시버가 이를 처리.
3. 다시 대기 모드 진입.
-> 반복

**처리 방법**
만약 오랜 시간 동작해야 한다면,
1. 별도의 스레드로 처리한다.
2. 서비스에 구현한다.

-예시-
    public class ReceiverEx extends BroadCastReceiver <!-- BroadCastReceiver 상속 받아서 처리함. -->
    {
        @Override
        public void onReceive(Context context, Intent intent){
            <!-- 처리 구문 -->
        }
    }
