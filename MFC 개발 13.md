- 재택 개발환경 구축

Visual Studio 2019 Community 설치 및 MFC 추가

cocos 2d-x 개발환경 설정


- stage[ID].xml

블록 확률 입력하는 칸 생성

최소 확률(10%), 최대 확률, 모든 확률의 합이 100%를 만족하지 않는 경우 에러

xml 파일로 저장/불러오기 확인

확률을 입력하지 않은 칸 자동으로 채우기

블럭의 생성확률과 드랍확률을 나눠서 설정할 수 있게 변경


- missionList[ID].xml과 tileInfo[ID].xml 편집 창에서도 바뀐 stage[ID].xml 파일 구조 불러오게 설정


- tileInfo[ID].xml 창에서 초기화(New) 시 발생하는 오류 수정

블럭 뿐만 아니라 패널의 CDC도 delete


- tileInfo[ID].xml

불러오기, 저장, 타일 복구 버튼 추가

저장하고 수정하지 않으면 창을 닫을 때 저장 여부 묻지않게 수정(저장 여부 물을 시 창에 *표시)


- TransparentBlt() 함수를 이용하여 비트맵 배경을 투명 처리

블럭 비트맵을 투명하게 하여 블럭과 패널이 한 번에 보이게 수정


- xml 제작 툴 매뉴얼 ppt 작성


- 프로그램 주석 달기



메인 화면

![image](https://user-images.githubusercontent.com/48848466/75870254-18843900-5e4e-11ea-814d-a49ca223ade5.png)


puzzleConfig.xml

![image](https://user-images.githubusercontent.com/48848466/75870284-21750a80-5e4e-11ea-81fb-c232ed21f767.png)


stage[ID].xml

![image](https://user-images.githubusercontent.com/48848466/75870352-35207100-5e4e-11ea-946c-93c8f58bff3d.png)


missionInfo[ID].xml

![image](https://user-images.githubusercontent.com/48848466/75870399-423d6000-5e4e-11ea-938b-68bb6eb9f38c.png)


tileInfo[ID].xml

![image](https://user-images.githubusercontent.com/48848466/75870491-60a35b80-5e4e-11ea-9e4e-d8c48d6efbf7.png)
