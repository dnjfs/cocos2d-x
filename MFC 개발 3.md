- puzzleConfig.xml, stage[ID].xml, missionList[ID].xml 파일을 관리하는 프로그램 개발

CDN 서버와 연동되어 파일 저장과 불러오기를 CDN에 할 수 있음


- puzzleConfig.xml

버튼을 누르면 바로 CDN과 연결되어 xml 파일을 불러옴


- stage[ID].xml

스테이지의 ID로 불러오는 기능 추가

사용할 블럭의 종류 수가 3개 미만인 경우 확인

저장 시 현재 스테이지의 ID가 연속되지 않는 경우 해당 ID를 알려줌


- missionList[ID].xml

ID로 불러오는 기능

미션으로 블럭을 선택할 때 stage[ID].xml 파일에서 존재하지 않는 블럭인 경우 알림
