타이머 기능을 가진 '스케줄'

1. 스케줄
매 프레임마다/지정된 시간마다/딜레이 타임 후 실행
2. 프레임간 시간의 보정
델타 타임: 함수의 현재 호출 시각과 이전 호출 시각의 차이 값을 반환
프레임이 클 수록 작음
3. 스케줄의 정지/재시작
schedule(), unschedule(), pauseTarget(), resumeTarget()
4. 게임의 정지/재시작
Director::getInstance()->pause()/resume()
일시 정지된 상태에서 메뉴를 클릭하면 글자가 확대되는 효과도 정지됩니다.

 


애니메이션을 만들 수 있는 '프로그레스 타이머'

1. 스프라이트 애니메이션
SpriteProgressToRadial/ToHorizontal/ToVertical/ToRadialMidpointChanged/BarVarious/BarTinAndFade
프로그레스 타이머를 사용하여 스프라이트를 생성하거나 다양한 효과를 주었습니다.
2. 진행상황 표시 애니메이션
프로그레스 타이머를 사용하여 스프라이트 생성 비율을 지정하였습니다.

 


이벤트 리스너에 등록하여 사용하는 '터치'

1. 싱글 터치
EventListenerTouchOnebyOne 클래스 사용
onTouchBegan/Moved/Ended/Cancelled
터치 시 위치도 좌표로 알 수 있었습니다.
2. 멀티 터치
EventListenerTouchAllAtOnce 클래스 사용
onTouchesBegan/Moved/Ended/Cancelled
3. 터치 응용 - 드래그 앤 드롭
setSwallowTouches(true)에 의해 블럭이 겹쳐있으면 Zorder가 가장 큰 블럭을 선택하여 드래그 앤 드롭시켜 이동시킵니다.
4. 터치 응용 - 회전
객체를 드래그 앤 드롭으로 회전합니다.
5. 터치 우선 순위
addEventListenerWithSceneGraphPriority(): 객체가 그려진 순서대로 터치의 우선 순위를 가짐
addEventListenerWithFixedPriority(): fixedPriority가 가장 높은 것이 터치의 우선 순위를 가짐

 


스프라이트들간의 '충돌 처리'

1. 충돌 처리
intersectsRect()를 이용하여 스프라이트들간의 충돌 체크
2. 충돌 처리 정리
containsPoint(): 점이 스프라이트에 포함되었는지 판단
intersectsRect(): 스프라이트와 스프라이트가 겹치는지 판단

 


'큰 배경'을 사용하여 배경 이미지를 연속하여 붙이기

1. 큰 배경 스크롤
빈 레이어를 생성해 배경 이미지를 이어서 놓고 레이어를 움직입니다.
2. 배경에 캐릭터 추가하기
배경과 용 캐릭터 생성을 함수로 만들었습니다.
3. 이동 버튼 추가하기
좌우 이동을 위한 화살표 스프라이트를 추가하고 터치이벤트를 추가하였습니다.
4. 이동하기
레이어를 나누어 배경과 드래곤은 움직이지만 이동 버튼은 움직이지 않게 만들었습니다.
Follow 클래스를 이용하여 드래곤을 중심으로 카메라가 따라다닙니다.




----------

노크노크에서 개발환경 설치 후 퍼즐게임 개발을 시작하기 전 cocos 2d-x에 대한 공부를 하고 있습니다.
덕분에 오늘은 cocos 2d-x의 많은 기능들을 다뤄볼 수 있었습니다.
