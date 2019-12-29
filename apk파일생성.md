안드로이드 스튜디오 3.5.3
안드로이드 SDK r29
안드로이드 NDK r20
apache ant 1.9.14
JDK 1.8.0_231 설치 후 환경변수 설정

cmd 창에서 cocos compile -p android --android-studio 명령어를 입력해도 apk파일이 생성되지않아
많은 검색을 통해 ndk 버전을 내려보고 SDK 버전도 내려보고 cocos 2d-x를 3.17.1로 내려봐도 안되어 문제를 찾을 수 없어
결국 안드로이드 스튜디오에 proj.android 폴더를 불러와 generate APK로 apk파일을 생성하는데 성공하였습니다.

![image](https://user-images.githubusercontent.com/48848466/71556507-e5ec4780-2a7c-11ea-8b43-f593bf095940.png)


갤럭시 S9+에서 apk파일을 설치하고 실행까지 되는 것을 확인하였습니다.

![image](https://user-images.githubusercontent.com/48848466/71556578-f94be280-2a7d-11ea-88f7-7b927875625c.png)
![image](https://user-images.githubusercontent.com/48848466/71556580-fbae3c80-2a7d-11ea-8886-00aa6a59e7de.png)
