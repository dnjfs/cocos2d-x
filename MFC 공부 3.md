- Check Box가 체크되면 Edit Control 활성화
클래스 마법사로 체크박스의 변수를 추가 후 체크박스 클릭 시 변수.GetCheck()로 체크박스의 상태를 가져옴
에딧컨트롤의 ID로 객체를 가져와 활성화
GetDlgItem(IDC_EDIT_RED)->EnableWindow(TRUE);


- 윈도우창 이름 바꾸기
CtestDlg::OnInitDialog() 함수에서
AfxGetMainWnd()->SetWindowText(L"Puzzle Stage Tool");
추가
혹은 Dialog에서 Caption 값을 직접 변경


- Menu 선택 시 Archive형 파일 입출력
New:  입력상자에 입력된 정보들 초기화
Load: 디렉토리에서 파일선택 후 파일에서 입력받아 각각 입력상자에 저장
Save: 입력상자에 입력된 정보들을 파일로 출력


- xml 파일 입출력
CMarkup 사이트에서 코드를 받아 Markup.h, Markup.cpp 파일 프로젝트에 추가
Markup.cpp에 #include "pch.h" 추가
CMarkup 클래스 사용


퍼즐게임 스테이지 제작도구 프로토타입 개발중
![image](https://user-images.githubusercontent.com/48848466/72626423-09c0f000-398e-11ea-8703-061510729b3b.png)
