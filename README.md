# 🗂️ 시간표 추천 프로그램

## 1. 프로젝트 소개  
본 프로젝트는 알고리즘 강의의 일환으로, 시간표를 자동으로 추천해주는 프로그램을 개발하고 개선하는 데 목적이 있습니다.  
사용자 입력에 따라 필수 과목을 자동으로 배치하고, 선택 과목은 시간표 충돌 없이 추천 알고리즘을 통해 제안합니다.


## 1-1. 📁 디렉터리 구조

- README.md
- data/
  - data.csv
- src/
  - code


## 1-2. 🗓️ 프로젝트 개발 일정
- 상세 일정 및 주차별 계획: [**Notion 팀 스페이스**](https://destiny-goat-114.notion.site/1c9c7c6ac4d9808eba1df79cecd53954) 참고


## 2. 📌 프로그램 전체 흐름

### 프로그램 시작

1. **CSV 파일 읽기**
   - 수업 데이터를 `data.csv`에서 불러옴
   - C: 직접 파싱하여 구조체로 저장
   - Java: 라이브러리 활용, List 객체에 저장  
   - 저장 필드: `과목명`, `과목코드`, `과목 유형`, `학점`, `강의 시간`, `개설 학과` 등

2. **사용자 입력 받기**
   - C: 콘솔 입력  
   - Java: GUI 입력 (Java Swing 활용)
   - 입력 항목:
     - 학과 및 학년
     - 수강 희망 학점/과목 수
     - 이미 수강한 과목
     - 선호 시간대 / 피하고 싶은 시간대
     - 선호 교수 / 피하고 싶은 요일 등

3. **필수 과목 우선 배치**
   - 학과 및 학년에 따라 전공 필수 / 교양 필수 과목을 `검색 알고리즘`으로 검색
   - 시간표에 추가하고, 시간 충돌 여부 검사 후 충돌 시 예외 처리
   - 시간표 객체 또는 구조체에 저장

4. **선택 과목 배치**
   - 필수 과목과 시간이 겹치지 않게 `검색 알고리즘`으로 검색
   - `추천 알고리즘` 적용:
     - 전공 > 교양 > 일반 순으로 우선순위 적용
     - 무작위 조합 생성으로 다양한 후보 시간표 구성
     - 사용자 조건 기반으로 점수화하여 최적 시간표 선택

5. **결과 출력**
   - 최종 추천 시간표를 출력
   - 콘솔, GUI 또는 파일 저장 형태 제공

### 프로그램 종료


## 3. 👥 역할 분담

| 역할 | 담당자 |
|------|--------|
| 데이터 불러오기 | 강현식 |
| 사용자 입력 처리 | 천예준 |
| 검색 알고리즘 | 김인규 |
| 추천 알고리즘 | 박신원 |
| 코드 통합 및 프로젝트 관리 | 전하준(팀장) |

## 4. 🤔 현재 고민 사항

- **사용 언어 선정**
  - 후보: C 또는 Java
  - Java는 GUI 개발이 쉬우며, 객체 지향적 구조에 유리
  - C는 구조적으로 단순하지만, 메모리 관리와 문자열 처리에서 복잡도 존재
  - 프로젝트 특성과 팀원의 역할 분담에 따라 결정 예정

- **개선 예정 알고리즘**
  - **검색 알고리즘**: 필수 과목 및 시간 겹침 없는 과목 추출
  - **추천 알고리즘**: 사용자 선호 기반 + 과목 우선순위 기반 점수화 로직 도입 고려


