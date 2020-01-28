- 노크노크의 CDN 주소로 filezilla FTP 설정


- Dialog 새로 만들어 새 창 띄우기

Dialog 하나를 추가하여 클래스 생성 후 메인 클래스에서 선언

newDlg.DoModal()로 새 창 띄움


- MFC로 만들어진 FTP 오픈소스를 이용하여 FTP 통신으로 CDN에 xml 파일 저장/불러오기

저장을 하면 Login()으로 FTP에 접속 후 UploadFile()로 PC에 있는 xml 파일을 CDN에 저장

불러오기를 하면 새 창을 띄워 스테이지 번호를 입력받고 Login() 후 해당 스테이지 xml 파일을 찾아 DownloadFile()로 PC에 저장하여 불러옴
