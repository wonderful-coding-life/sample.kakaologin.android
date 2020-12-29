# 카카오 로그인 API 예제

카카오 로그인 API를 사용하여 로그인/로그아웃을 구현한 샘플 프로젝트입니다.
MainActivity.java는 자바로 구성된 예제이며 LoginActivity는 동일한 내용의 코틀린 예제입니다.
카카오 개발자 사이트에서 애플리케이션 등록을 한 후에 네이티브 앱 키를 아래 부분에 수정을 한 후 실행하면 됩니다.

KakaoApplication.java
```
KakaoSdk.init(this, "94b1f974c57cec1e31d33f8a4acc4829");
```
AndroidManifest.xml
```
<data android:host="oauth" android:scheme="kakao94b1f974c57cec1e31d33f8a4acc4829" />
```

소스코드에 대한 설명은 [유튜브](https://youtu.be/8hKczn0-Hkw)를 참조하세요.

간혹 카카오 로그인 한 후에도 계속 로그인 버큰이 보인다는 분들이 계십니다. 터미널에서 생성한 해시키 대신 아래와 같이 MainActivity의 onCreate에서 직접 코드로 해시키를 생성하여 사용해 보시기 바랍니다.
```
Log.i(TAG, "debug keyhash is " + Utility.INSTANCE.getKeyHash(this));
```
