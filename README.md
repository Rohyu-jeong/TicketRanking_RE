# 티켓랭킹 자동화 프로그램

> **REFramework 기반으로 YES24 티켓 랭킹 데이터를 수집하고, 정리된 결과를 메일로 자동 전송하는 RPA 프로그램입니다.**

---

## 기술 환경

- UiPath Studio
- Robotic Enterprise Framework (REFramework)
- Excel, Web Automation
- HTML Email, DataTable, Dictionary 등 활용

<br>

## 자동화 흐름 요약

1. 수신 메일에서 항목 목록 추출
2. 템플릿 복사 및 초기 Excel 시트 생성
3. YES24 티켓 랭킹 페이지 접속 및 항목별 데이터 수집
4. 시작일, 종료일, 장소 항목 분리 및 날짜 포맷 가공
5. 항목별 1위 데이터를 본문용 테이블로 정리
6. 성공/실패 항목 구분 및 처리 결과 적용
7. 전체 결과를 Excel 파일로 저장
8. 메일 본문 작성 및 Excel 첨부 후 자동 발송

<br>

## Workflow 구성

- **Initialization** <br>
  01_Output 폴더 초기화.xaml <br>
  02\_초기 변수 선언.xaml <br>
  03\_결과 파일 생성.xaml <br>
  04\_메일 수신 및 항목 추출.xaml <br>
  05\_초기 DT 생성.xaml <br>
  06\_엑셀 템플릿 리스트 복사.xaml <br>

- **Process Transaction** <br>
  07\_티켓 랭킹 DT 추출 및 가공.xaml <br>
  08\_티켓 랭킹 DT 저장.xaml <br>
  09_1위 DT 추출.xaml <br>

- **End Process** <br>
  10\_처리 결과 분류.xaml <br>
  11\_메일 발송.xaml <br>
