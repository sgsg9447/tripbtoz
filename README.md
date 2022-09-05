# 1. 프로젝트 설치 및 실행

```
git clone https://github.com/Wanted-Pre-Onboarding-FE-Team5/tripbtoz

npm i

npm start

//windows 운영체제에서 npm start 명령어로 json-server 실행이 안될 경우 추가로 아래 명령어 사용
npm run server

//json-server port 설정 = "json-server --watch ./database/database.json --port 8000" 

```

## 2. 프로젝트 목표
- 예약 페이지 개발
- 체크 인/아웃 날짜를 선택할 수 있는 캘린더 구현
- 투숙객 수를 입력할 수 있는 인풋 폼 구현
- 제공되는 hotels.json 파일의 데이터 중 체크 인/아웃 기간과 인원수에 해당하는 호텔들을 조회
- 조회 된 호텔을 무한 스크롤로 노출
- 호텔 하나를 선택하게 되면 선택한 (체크 인/아웃 - 투숙객 수 - 호텔명) 정보를 가지는 데이터를 로컬 스토리지에 json타입으로 저장. 

## 3. 역할 분담

| 팀원 이름                               | 기능                                                                                                     |
| --------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| [김슬기](https://github.com/sgsg9447)   | 캘린더 구현 |
| [이유미](https://github.com/ymStudyLog) | 호텔 정보 렌더링 담당 |
| [김연진](https://github.com/yunjink)    | 전체 레이아웃,스타일 담당 |


## 4. 기술스택

typescript 
react-router-dom
styled-components 
styled-reset 
json-server
react-query
date-fns
uuid

## 5. 캘린더 제작

- [x] 체크 인/아웃 날짜를 선택할 수 있는 **캘린더 구현**
- [x] 투숙객 수를 입력할 수 있는 인풋 폼 구현
- [x] 오늘 날짜부터 12개월까지 보여지는 캘린더를 반응형으로 구현
- [x] 이번달의 지난날은 모두 선택되지 않아야 함
- [x] 처음 캘린더를 선택할 때 default로 일주일 뒤 1박으로 체크인 되도록 함
- [x] 처음 선택한 날이 체크인이 되며 두 번째 선택한 날이 체크아웃으로 설정됨
- [x] 처음 선택한 날보다 이전 날짜를 선택한 경우 처음 선택한 날짜가 초기화 되고 두 번째 선택한 날짜가 체크인으로 됨
- [x] 시작일(체크인)과 종료일(체크아웃) 날짜는 highlighting 되며 체크인과 체크아웃 사이의 날짜도 동일하게 highlighting 됨
- [x] 시작일(체크인)과 종료일(체크아웃)을 선택한 상태에서 다른 날짜를 선택하면 기존 선택값은 초기화 되며, 선택한 다른 날짜가 시작일(체크인)이 됨


## 6. 구현 화면
<img width="797" alt="스크린샷 2022-09-06 오전 4 34 41" src="https://user-images.githubusercontent.com/87474789/188505765-e4211b8b-dec8-49bb-a263-6f3b722eef08.png">

<img width="792" alt="스크린샷 2022-09-06 오전 4 37 15" src="https://user-images.githubusercontent.com/87474789/188505922-4f95a970-7730-49a7-b2e8-a93f8706a65f.png">


## 7. 구현과정 
- [자세히 보기](https://velog.io/@sgsg9447/React-TS-Calendar-Without-Library)

## 8. 디렉토리구조
```
src
 ┣ api
 ┃ ┗ api.ts
 ┣ components
 ┃ ┣ calendar
 ┃ ┃ ┣ Body.tsx
 ┃ ┃ ┣ Calendar.tsx
 ┃ ┃ ┣ Dates.tsx
 ┃ ┃ ┗ Head.tsx
 ┃ ┣ common
 ┃ ┃ ┣ Loading.tsx
 ┃ ┃ ┣ NavigationBar.tsx
 ┃ ┃ ┗ SearchBar.tsx
 ┃ ┣ hotelList
 ┃ ┃ ┣ HotelItem.tsx
 ┃ ┃ ┗ HotelList.tsx
 ┃ ┗ modal
 ┃ ┃ ┣ CalendarModal.tsx
 ┃ ┃ ┗ CountModal.tsx
 ┣ hooks
 ┃ ┣ useDatabase.ts
 ┃ ┣ useFilter.tsx
 ┃ ┣ useInfiniteScroll.tsx
 ┃ ┗ useLocalStorage.ts
 ┣ pages
 ┃ ┣ Hotel.tsx
 ┃ ┣ Landing.tsx
 ┃ ┗ Reservation.tsx
 ┣ router
 ┃ ┗ Router.tsx
 ┣ styles
 ┃ ┣ GlobalStyles.tsx
 ┃ ┣ Hotel.style.tsx
 ┃ ┣ HotelItem.style.tsx
 ┃ ┗ HotelList.style.tsx
 ┣ types
 ┃ ┣ databaseType.ts
 ┃ ┣ localStorageType.ts
 ┃ ┗ queryType.ts
 ┣ utils
 ┃ ┣ dateUtils.ts
 ┃ ┗ infiniteScroll.ts
 ┣ App.tsx
 ┣ index.tsx
 ┣ react-app-env.d.ts
 ┗ setupTests.ts
```


