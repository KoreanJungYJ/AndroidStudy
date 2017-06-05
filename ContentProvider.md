콘텐트 프로바이더란?
: 애플리케이션 간의 데이터 공유를 위해 표준화된 인터페이스를 제공하는
컴포넌트이다. (브로드캐스트 리시버는 사용자 인터페이스를 가지지 않는다!)

이것이 제공하는 실제 데이터는 파일 시스템에 있을 수 있고
데이터베이스에도 있을 수 있다. (그 외에도 다양하다!)

**기능 작성**
1. 읽기
2. 쓰기
3. 수정하기
4. 삭제하기

만약 콘텐트 프로바이더가 구현되어 있으면 다른 애플리케이션은
구현된 메소드를 호출하기만 하면 된다는 특징이 있다.

    public class ProviderEx extends ContentProvider{
        public int delete(Uri uri, String selection, String[] selectionArgs){
            return 0;
        }
        public String getType(Uri uri){
            return null;
        }
        public Uri insert(Uri uri, ContentValues values){
            return null;
        }
        public boolean onCreate(){
            return false;
        }
        public Cursor query(Uri uri, String[] projection, String[] selectionArgs, String sortOrider){
            return null;
        }
        public int update(Uri uri, ContentValues values, String[] selectionArgs){
            return 0;
        }
    }