#### 티켓랭킹 자동화 프로그램
---
REFramework 기반으로 YES24 티켓 랭킹 데이터를 자동 수집하고, 정리된 결과를 메일로 전송하는 자동화 프로그램입니다.

## 기술 환경

- UiPath Studio
- Robotic Enterprise Framework(REFramework)
- Excel, Web Automation
- HTML Email, DataTable, Dictionary 등 활용

## 자동화 흐름 요약

1. 수신 메일에서 항목 목록 추출
2. 템플릿 복사 및 초기 Excel 시트 생성
3. YES 24 티켓 랭킹 페이지 접속 및 항목 별 데이터 수집
4. 시작일, 종료일, 장소 항목 분리 및 날짜 포맷 가공
5. 항목별 1위 데이터를 본문 용 테이블로 정리
6. 성공/실패 항목 구분 및 처리 결과 적용
7. 전체 결과를 Excel 파일로 저장
8. 메일 본문 작성 및 Excel 첨부 후 자동 발송

## 워크플로우 구성

- **Initialization**
    01_Output 폴더 초기화.xaml
    02_초기 변수 선언.xaml
    03_결과 파일 생성.xaml
    04_메일수신및항목추출.xaml
    05_초기 DT 생성.xaml
    06_엑셀 템플릿 리스트 복사.xaml

- **Process Transaction**
    07_티켓 랭킹 DT 추출 및 가공.xaml
    08_티켓 랭킹 DT 저장.xaml
    09_1위 DT 추출.xaml

- **End Process**
    10_처리 결과 분류.xaml
    11_메일 발송.xaml