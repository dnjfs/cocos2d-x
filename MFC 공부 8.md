
- Modeless Dialog를 이용하여 창 전환하기
1. 메인 디알로그 클래스인 mainDlg.cpp에 #include "CTileDlg.h"와 CmainDlg *mainDlg; 선언
2. mainDlg.h에 extern CmainDlg *mainDlg; 선언
3. 마찬가지로 서브 디알로그 클래스인 CTileDlg.cpp와 CTileDlg.h에도 각각 전역 클래스형 변수와 extern 선언
#include "mainDlg.h"도 선언해주는데 헤더 파일이던 소스 파일이던 상관없음
4. 메인 디알로그에서 [Ctrl+Shift+x]로 클래스 마법사를 실행시켜 메시지 탭에서 WM_CREATE 선택
5. 만들어진 OnCreate() 함수에 서브 디알로그 생성 및 메인 윈도우 지정
int CmainDlg::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
 if (CDialogEx::OnCreate(lpCreateStruct) == -1)
  return -1;

 tileDlg = new CTileDlg();
 tileDlg->Create(IDD_DIALOG_TILE, GetDesktopWindow()); //this 대신 GetDesktopWindow()를 넣으면 작업 표시줄에 아이콘이 생김
 tileDlg->ShowWindow(SW_HIDE);

 mainDlg = (CtestDlg *)theApp.m_pMainWnd;
 
 return 0;
}
6. 똑같이 클래스 마법사에서 WM_DESTROY 선택하여 메모리 누수 방지를 위해 delete
void CtestDlg::OnDestroy()
{
 if(tileDlg != NULL)
 {
  tileDlg->DestroyWindow();
  delete tileDlg;
 }
}
7. 버튼을 누르면 메인 디알로그를 숨기고 서브 디알로그 열기
void CtestDlg::OnBnClickedOk()
{
 tileDlg->ShowWindow(SW_SHOW);
 ShowWindow(SW_HIDE);
}
여기까지 모델리스로 메인 디알로그에서 서브 디알로그 여는 방법
반대로 서브 디알로그에서 메인 디알로그로 전환하기 위해
8. CTileDlg.cpp에서 버튼 클릭 시 작업을 설정
void CTileDlg::OnBnClickedOk()
{
 testDlg->ShowWindow(SW_SHOW);
 tileDlg->ShowWindow(SW_HIDE);
}


- 윈도우 창에 자식 디알로그 띄우기
새로운 디알로그를 추가해 클래스를 만들어주고 부모 디알로그의 소스 파일에 자식 디알로그 클래스의 헤더 파일을 포함시킴
부모 디알로그의 소스 파일에서 CPanelDlg panelDlg; 선언
OnInitDialog() 함수에서
 m_clsPanelDlg.Create(IDD_FORMVIEW, this);
 m_clsPanelDlg.ShowWindow(SW_SHOW);
추가하여 초기화 시키면 부모 디알로그에 자식 디알로그가 그대로 올라옴


- 최소화 버튼
프로젝트 생성 시 사용자 인터페이스 기능 탭에서 최소화 상자 선택
혹은 디알로그 속성-모양에서 Minimize Box 값을 True로 설정


- 윈도우 창 크기 변경 가능/금지
디알로그 속성-모양에서 Border 값을 Resizing/Dialog Frame으로 설정


- Accelerator를 이용한 단축키 설정
Accelerato 리소스 추가
보조키와 키 설정
메인 클래스에 HACCEL m_hAccel; 선언
OnInitDialog() 함수에 m_hAccel = ::LoadAccelerators(AfxGetInstanceHandle(), MAKEINTRESOURCE(IDR_ACCELERATOR1)); 추가
클래스에서 해당 단축키의 ID 처리기 추가하여 동작 정의하면 완료 
