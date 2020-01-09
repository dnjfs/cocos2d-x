AudioEngine 클래스를 이용하여 '사운드' 출력

게임 안에서 배경음이나 효과음을 출력
preload(), play2d(), pause(), resume(), stop(), setVolume()




장면을 전환하는 '씬 트랜지션'

1. 장면 전환
createScene(), pushScene(), popScene(), replaceScene()
2. 장면 전환 효과
TransitionScene 클래스
3. 장면의 생성 및 소멸 순서
새로운 장면이 먼저 불러지고 이전 장면이 사라집니다.




작은 그래픽 입자들로 효과를 주는 '파티클 시스템'

1. 파티클 시스템 사용
텍스쳐 파일을 불러와 다양한 효과 사용
2. plist를 사용한 파티클 시스템
plist 파일을 불러옴




'데이터 저장'

UserDefault 클래스 이용
get/set[자료형]ForKey()로 데이터 불러오기/저장하기




'사용자 입력'

EditBox 클래스를 이용하여 키보드로 입력




'스크롤'

ScrollView 클래스를 이용하여 페이지 스크롤




'테이블'

TableViewDataSource, TableViewDeleate 추상 클래스를 상속받아 함수들을 오버라이드해서 사용
테이블을 스크롤할 수 있고, 터치 시 테이블의 태그와 인덱스 출력




'리소스 데이터'

1. XML 사용
tinyxml2 프레임워크 사용하여 XML 데이터 읽음
2. JSON 사용
rapidjson 프레임워크 사용하여 JSON 데이터 읽음




서버에 접속하기 위한 'HTTP 통신'

1. HTTP 기본 사용법
HttpRequest() 클래스 사용, get/post 테스트
2. 웹에서 이미지 가져와서 출력하기
HttpRequest Type을 GET으로 설정하여 웹페이지를 경로로 이미지 파일을 다운로드
