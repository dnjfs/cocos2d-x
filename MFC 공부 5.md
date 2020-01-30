- xml파일 저장/불러오기시 디렉토리가 존재하지 않으면 생성하기

CreateDirectory(디렉토리 경로, NULL);


- 8x8 격자 생성, 격자에 사각형 채우기

CPaintDC 클래스를 이용하여 dc.Rectangle()로 사각형 생성

CBrush 클래스로 사각형의 색깔 설정

왼쪽클릭시 좌표값을 받아 반올림하여 격자 위치에 맞게 생성
