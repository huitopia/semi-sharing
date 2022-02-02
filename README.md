# JSP, Servlet을 활용한 MVC 패턴 미니 프로젝트
### 여행을 통해 방문한 특정 장소나 상황에 대한 사진을 기록으로 남기고 공유하는 소셜 네트워킹 기반 서비스

## 📅 제작 기간
#### 2021.08.17 ~ 2021.08.20

## 📝 요구사항
### 회원가입
- 가입하기 버튼을 입력 시 : 아이디&비밀번호가 입력되지 않았을 경우 -> 아이디&비밀번호를 입력하지 않았다는 알림창 출력
- 아이디, 이메일, 전화번호 중복 불가
- 아이디, 이메일, 전화번호 Not null
- 비밀번호 확인 시 이전에 입력한 값과 같은지 확인
- 생년월일 캘린더 API 사용
- 이메일 유효 체크
- 아이디 중복 버튼을 토해 기존 값이 존재하는지 확인
- 휴대전화 맨 앞 자리를 선택할 수 있는 드롭박스 구성
- 가입하기 버튼 클릭시 필수 입력 항목들이 모두 체크되어있는지 체크 후 만족한다면 회원가입 완료 페이지로 이동, 불만족시 알림 호출
- 회원 가입 시 회원 고유 번호 생성
- 가입 완료시, 가입 완료 알림 호출
- 텍스트 하단에 로그인 버튼과 메인 페이지로 돌아가는 home 버튼 생성
### 회원정보
- 회원정보에서 현재 본인의 정보 확인 가능
- 정보 수정으로 본인 정보 중 휴대폰 번호, 주소, 비밀번호 변경 가능
- 비밀번호 변경 시 비밀번호 재확인
- 회원 탈퇴 가능
- 비밀번호 확인 불가능
- 아이디, 이름, 생년월일은 수정 불가
- 닉네임 변경 버튼 클릭시 중복 확인 결과 알림 호출
- 가입일자 표기되며, 탈퇴 버튼 클릭 시 탈퇴 요청 알림 호출
### 로그인
- 로그인 버튼 클릭시 아이디, 비밀번호 일치 확인
- 아이디, 비밀번호 다른 경우 알림 호출
- 아이디, 비밀번호 입력창에 입력된 값이 없을 경우 입력하라는 알림 호출
- 가입하기 버튼 클릭 시 회원가입 페이지 이동
- 카카오톡 로그인 버튼 클릭시 카카오톡 로그인 연동 팝업 호출
### 메인페이지
- 대표 이미지 랜덤 출력
- 이미지 클릭시 해당 게시물 이동
- 로그인하지 않았을 경우 상단에 로그인 메뉴 존재함
- 로그인시 회원의 프로필 사진, 닉네임, 로그아웃 존재함
- 가입된 회원 수, 업로드된 이미지 수 등의 통계 정보를 실시간 반영하여 업로드
#### 메인페이지 - 검색기능
- '#' 태그 형태로 검색 기능 지원 및 여러 개의 태그를 이용하여 해당 태그에 맞는 검색 가능
- 검색 결과에서 좋아요, 최근, 조회 순서로 보기 지원
- 검색창에 텍스트 입력시 아래에 검색 가이드라인이 출력(ex. #pa 검색 시 #paris, #paradise 등 출력)
- 태그를 정확히 인지하여 검색되어야함
#### 메인페이지 - 검색결과
- 검색 결과는 이미지만 그리드 형태로 출력
- 검색 버튼을 누르면 해당 검색 태그에 해당되는 이미지를 하단에 1열에 3개씩 출력
- 이미지에 마우스 커서가 들어올 시 이미지 110% 확대
- 검색 전에는 검색창 하단에 좋아요 수가 많은 순서로 특정 게시글을 출력
- 이미지 클릭시 상세 게시물 보기 이동
### 게시물 작성
- 불러오기 버튼으로 사진 업로드 가능(jpg, png 등)
- 불러오기 버튼을 입력 시 업로드 창 출력
- 글을 적는 중 페이지를 벗어나려 할 경우 경고 알림 출력
- 국가, 날짜 버튼은 필수 항목으로 누락시 업로드 버튼 비활성화
- 도시, 랜드마크는 선택사항
### 상세페이지
- 이미지, 게시글, 글쓴이, 좋아요, 신고, 태그 형태로 출력
- 본인 게시물이면 수정, 삭제 버튼 활성화
- 관리자 접근 시 삭제 버튼 활성화
- 하단에 이미지 그리드 혀태로 목록 출력
### 관리자
- 관리자 페이지에서 전체 글 확인 가능
- 검색을 통하여 특정 키워드 글 검색 및 체크하여 글 삭제 가능
- 회원 정보 확인 가능
- 지역별, 키워드별 게시물 수 통계로 확인 가능
- 좋아요, 싫어요 해당하는 게시글 목록 확인 가능
- 신고, 문의 게시판 활성화
### QnA
- 자주 묻는 질문 목록으로 화면 표시
- 신고, 문의 버튼으로 해당 게시판 이동
- 신고, 문의는 자신이 작성한 것만 확인 가능(관리자는 전체 글 확인 가능)
- 상단에 개발자 정보 업로드(문의 안내)
