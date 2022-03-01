본 프로그램은 DVSwitch 서버에 여러 사용자의 서버를 함께 구성할 수 있도록 만드는 보조 프로그램이다.

즉, DVSwitch 서버와 함께 사용하여야 한다.
#
### 설치 방법:
  - sudo wget https://github.com/hl5ky/dvsmu/raw/main/setup
  - sudo chmod +x setup
  - sudo ./setup
#
### 추가 설정:
  - 로칼 시간 설정 (자동리부팅을 위하여 설정 필요) https://blog.buffashe.com/2020/02/changing-ubuntu-timezone
  - 디스크 SWAP 설정 (오라클 클라우드에 설치시 필요) https://yeon-kr.tistory.com/174
  - 포트 개방 (오라클 클라우드에서 포트 개방 방법) https://kibua20.tistory.com/124
#
### 특징:
  - 하나의 서버에 최고 40 명의 사용자를 추가할 수 있다.
  - 전체 사용자의 호출부호, DMR ID, USRP Port 현황을 한 화면에서 볼 수 있다.
  - 별도의 설치방법을 제공하므로 여러 가지 목적으로 사용이 가능하다.
  - 각 사용자가 각자의 매크로를 사용할 수 있다.
  - 각 사용자가 각자의 즐겨찾기를 관리할 수 있다.
  - 추가사용자는 DMR만 가능하다.
  - DVSwitch의 업그레이드를 반영할 수 있다.
  - 업그레이드시 각 사용자의 정보는 자동으로 재설정된다.
  - dvsMU의 업그레이드도 메뉴에서 가능하다.
  - 시스템 최적화를 통해서 보다 안정된 시스템을 만들 수 있다.
#
### 실행방법:
  - 터미널모드에서 dvsmu를 입력하고 엔터를 누르면 실행된다.
#
### 사용방법:
  - dvs에서 메인사용자의 설정을 한 후에 dvsmu를 사용하도록 한다.  
  - User번호에서 엔터를 누르면 추가 사용자설정이 가능하다.  
  - 추가 사용자의 설정을 한 후, 다시 User번호에서 엔터를 누르면 사용자 관리 메뉴가 보인다.
#
### History:

  v.2.0 (배포 예정)
  - 스크립트 형태로 배포 시작
  - 추가사용자수 최대 40명까지 가능. 하드웨어 및 상황에 따라 다름 3B(10명) 3B+(15명) 4B(20~40명)
  - 메뉴 구성 변경 및 다양한 ini 파일 관리 기능 추가
  - DVSM용 매크로의 언어선택(한글,영어) 가능
  - 추가사용자 입력시 위도,경도,위치는 빈 내용으로 표시하여 입력을 편리하게 변경
  
  v.1.92 (2021. 11. 22.)
  - 추가사용자의 설정시 주파수 입력난 추가
  - 기존 사용자의 주파수 설정에 문제가 있으면 자동으로 해결하는 루틴 추가
  - BM 마스터서버의 주소를 주사용자의 설정에 따르도록 수정
    (주사용자의 설정이 호주의 BM서버이면, 추가사용자도 호주로 설정됨)
  - 주사용자의 기본모드설정에 상관없이 추가사용자의 모드는 DMR로 설정되도록 수정
  - DMRId 데이타의 에러로 상대방의 호출부호가 보이지 않는 문제 보완
  - 브랜드마이스터 비밀번호에 특수문자 사용시 에러 수정
  - 주요한 내용을 로그에 기록하여 차후에 참조할수 있도록 함

  v.1.8 (2020. 12. 22.)
  - 1일1회 리부팅 기능: 사용하지 않는 시간에 실행하도록 개선

  v.1.7 (2020. 12. 18.)
  - 메뉴 구성 변경
  - 1일1회 리부팅 설정 기능 추가

  v.1.6 (2020. 12. 10.)
  - BM 및 클라이언트 연결상태 확인 기능 추가
  
  v.1.5 (2020. 11. 27.)
  - 공개 버전
  
  v.1.4.9 (2020. 11. 25.)
  - 메인 메뉴 내용 변경 : talkerAlias의 내용이 공백이 아니면, 메인 메뉴에 표시
    
  v.1.4.8 (2020. 11. 23.)
  - 추가사용자의 talkerAlias 내용 변경 기능 추가
  
  v.1.4.7 (2020. 11. 22.)
  - 시스템 최적화 메뉴 추가

  v.1.4.6 (2020. 11. 21.)
  - 브랜드마이스터 비밀번호 입력항목 추가
  
  v.1.4.5 (2020. 11. 20.)
  - Description을 dvsMU로 처리 (talkerAlias에 반영)
  - 로그파일 처리루틴 개선
  - 업그레이드 처리루틴 개선

  v.1.4.4 (2020. 11. 19.)
  - 입력시 위도,경도,위치는 최종 입력내용을 디폴트로 저장
  
  v.1.4.3 (2020. 11. 19.)
  - 주파수 등을 입력항목에서 제외
  - 진행상태 표시 개선
  
  v.1.4.2 (2020. 11. 19.)
  - 로그파일이 utc 기준으로 작성되기 때문에 발생하는 문제 해결 
  - 설정시 진행상태 표시
  - 업그레이드시 버전 확인후 업그레이드 진행
  
  v.1.4 (2020. 11. 17.)
  - 업그레이드 메뉴 추가
  
  v.1.3 (2020. 11. 16.)
  - 입력시 포트 중복 확인 기능 추가
  - 시스템 모니터 기능 추가
  - 사용자별 로그 확인 기능 추가
  - 4일 이상 지난 로그 삭제 기능 추가
  
  v.1.2 (2020. 11. 15.)
  - 사용자별로 기본매크로와 수정매크로로 변경하는 기능 추가
  
  v.1.1 (2020. 11. 13.)
  - 메인사용자의 DSTAR 활성/비활성화 기능 추가
  
  v.1.0 (2020. 11. 12.)
  - 프로그램 작성 및 테스트 시작
    
