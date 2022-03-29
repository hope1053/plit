# plit
`Storyboard` `MVC` `Alamofire` `SwiftyXMLParser` `Realm` `Firebase(Analytics, Crashlytics) `

#### ✨ 그 날의 공연을 잊지 않게, plit
> 공연(연극/뮤지컬)을 다관람하는 관객들을 위한 어플

<img src = "https://user-images.githubusercontent.com/22907483/158542477-b5b08971-b9d7-4546-95cf-49ec359876f0.png" width= "30%"><img src = "https://user-images.githubusercontent.com/22907483/158542505-8e21629b-4825-42de-9dc2-03de3b071ff3.png" width= "30%">

> - 프로젝트 기간: 2021.11 ~ 2021.12  
> - Released: 2021.12.04
> - 개인 프로젝트

[<img src = "https://user-images.githubusercontent.com/22907483/158495296-80b90b26-9fb3-4933-96b5-a5953b30fb6c.png" width= "18%">](https://apps.apple.com/kr/app/plit/id1597847235)

## Service
- **관극 일정 저장**: 제목, 캐스팅, 좌석 정보, 가격, 할인 정보, 후기 등 관람 일정 관련 정보들을 저장할 수 있고 캘린더 형식으로 일정을 한 눈에 확인할 수 있습니다.
- **정산 데이터 제공**: 1년 단위로 관극 횟수, 금액을 기준으로 통계 자료를 제공합니다. 또한 극, 극장별로 정산 데이터도 제공합니다.

## Workflow
<img width="80%" alt="image" src="https://user-images.githubusercontent.com/22907483/158543781-29789c4a-e80c-4c13-b40d-431d7ff102a1.png">

## Skill
- View
```swift
'Storyboard'
'XIB'
'FSCalendar'                      // 커스텀 캘린더 구현 
'Parchment'
'IQKeyboardManager'
'Charts'                          // 차트로 데이터 시각화
'JGProgressHUD'
```
- Network
```swift
'Alamofire'                       // 서버 통신
'SWXMLHash'                       // XML 데이터 Hashing
'Kingfisher'                      // 이미지 캐싱
```
- Data & User
```swift
'Realm'                     // 데이터 저장
'Firebase/Analytics, Crashlytics' // 사용자 앱 사용 정보 및 충돌 정보 수집 
```
## View
### 1. 캘린더
<img src = "https://user-images.githubusercontent.com/22907483/158496412-c6b0632a-0710-4ba6-9cc9-c2297e9397a7.PNG" width= "25%"> <img src = "https://user-images.githubusercontent.com/22907483/158548878-73e57575-17ed-4d54-a03d-389aa67c532f.jpeg" width= "25%">

- 캘린더 날짜별 Cell 각 하단의 이벤트 유무 표시로 일정의 유무를 확인할 수 있습니다.  
- 하루에 최대 2개의 일정을 저장할 수 있으며 날짜 선택 후 일정을 클릭하여 상세 정보 화면으로 진입할 수 있습니다.  
- 해당 화면의 우측 상단 '+' 버튼을 클릭하여 공연을 검색하고 기록을 추가할 수 있습니다.

### 2. 공연 검색 및 기록
<img src = "https://user-images.githubusercontent.com/22907483/158547709-16be9d13-7faf-4da6-83c3-825a726feb46.jpeg" width= "25%">  <img src = "https://user-images.githubusercontent.com/22907483/158496421-8891dbf2-1228-4deb-ad96-4e66dd5f058f.PNG" width= "25%">

- 원하는 공연을 검색 후 선택하여 자세한 정보를 입력 후 저장할 수 있습니다.  
- 이때 저장 가능한 정보는 날짜, 시간, 캐스팅, 좌석, 금액, 할인 정보 그리고 후기 입니다.
- 추후 수정 및 삭제 가능합니다.

### 3. 1년 단위로 제공되는 관극 리포트 확인
<img src = "https://user-images.githubusercontent.com/22907483/158496429-3507063d-0241-4d8a-92ab-68b1553ac266.PNG" width= "25%">  <img src = "https://user-images.githubusercontent.com/22907483/158548136-d8c7c3f0-ee2b-45cb-a6fc-0be34a424002.jpeg" width= "25%"> 

- 저장한 데이터를 기반으로 각 년도별 통계 데이터를 확인할 수 있습니다.  
- 총 몇 번의 관극을 했는지 label로 표시하고 있으며 월 별로 몇 번 관람하였는지 차트를 통해 확인할 수 있습니다.  
- 동일하게 총 소비 금액을 label로 표시하고 있으며 월 별로 소비 금액을 차트를 통해 확인할 수 있습니다.  
- 화면 수평 스크롤을 통해 다른 년도 데이터를 확인할 수 있습니다.  
- 화면 하단의 극 별 정산 보러가기, 극장 별 정산 보러가기 버튼을 통해 극, 극장 별 정산 페이지로 진입할 수 있습니다.

### 4. 극/극장 별 정산 확인
<img src = "https://user-images.githubusercontent.com/22907483/158496458-f7c43ca6-2886-4212-86c7-b4f32d18fbea.PNG" width= "22%">  <img src = "https://user-images.githubusercontent.com/22907483/158496477-c60f84ed-ab95-4d0d-911d-2fcb61c5bb15.PNG" width= "22%">  <img src = "https://user-images.githubusercontent.com/22907483/158548276-c2bfe4de-25df-4c99-8403-70064c5769f6.PNG" width= "22%">  <img src = "https://user-images.githubusercontent.com/22907483/158548290-4cff40b0-33b4-499c-ab8d-ca197b90e0f0.PNG" width= "22%">

- 극 별 정산 페이지에서는 해당 년도에 관람한 극들에 대한 정보를 확인할 수 있습니다.  
- 기본적으로 관람 횟수 순으로 정렬이 돼있으며 가나다 순, 관극 횟수 순, 관극 비용 순으로 정렬도 가능합니다.  
- 그 중 원하는 극을 선택하면 상세 페이지로 진입할 수 있습니다.  
- 극 별 정산 상세페이지에서는 해당 극에 대한 기본 정보들(공연 일정, 전체 캐스팅, 극장, 런타임, 가격)과 사용자 맞춤 정보(첫 관람 날짜 및 캐스팅, 마지막 관람 날짜 및 캐스팅, 총 관람 횟수, 총 소비 비용, 좌석 정보)를 확인할 수 있습니다.  
- 극장별 정산 페이지는 방문 횟수 순으로 정렬돼있습니다.  
 원하는 극장을 선택하면 상세 페이지로 진입할 수 있고 월 별 방문 횟수와 해당 년도, 해당 극장에서 관람한 극의 리스트를 확인할 수 있습니다.

## Update
- **ver 1.1**
 - 코드 안정성 및 리포트 탭 UI 개선
- **ver 1.2**
 - 삭제 기능 추가
 - UI 업데이트

## Extra Detail
<details>
<summary>기획서</summary>
<div markdown="1">   
  
## 기획 배경
- 기존에 관극 일정 관리를 위해 사용하는 어플이 있지만 UI가 더 보기 좋고 인터랙션이 조금 더 부드러웠으면 좋겠다는 의견이 다수 있었음  
- 평소에 분기별로 관극 일정을 정산하여 친구들과 그 결과를 공유하기도 하는데 기존에 사용하는 어플은 통계가 관극 횟수, 금액에 대해서 대략적으로만 제공되고 있어서 직접 일일히 기록을 찾아보며 계산해야되는 불편함이 있었음
- 티켓팅이 자주 진행되다보니 일정을 잊어버리는 경우가 발생하는데 이를 대비하여 일정 리스트업 및 알림까지 해주는 기능이 있었으면 함

## 기능 정의
1. 캘린더 형식으로 일정을 한 눈에 볼 수 있도록 제공
2. 1년 단위로 관극 횟수, 금액을 기준으로 통계자료 제공 & 극, 극장별로 정산 데이터도 제공

### 기능 명세서
[📱 스프레드시트 링크](https://docs.google.com/spreadsheets/d/1mbSi8enOS0kr1sQolvYPqGSjQUuz6io5vxsx7Y3UdoM/edit?usp=sharing)</br></br>
<img width="953" alt="image" src="https://user-images.githubusercontent.com/22907483/142127363-1a7d4c73-2eb9-4728-8a1a-a8c3ce77b4cb.png">  
  
## 고민중인 부분
- 친구들과 일정 공유기능을 만들고 싶은데 서버를 다뤄본 적이 없어서 어려울 것 같아서 고민 중  
- 추후에 위젯도 추가하고 싶음!
  
</div>
</details>

<details>
<summary>와이어프레임</summary>
<div markdown="1">   
  
## 와이어프레임
[📱 피그마 링크](https://www.figma.com/file/bR1Djyrgi7igk5pAZig4aJ/SeSAC_PLIT?node-id=0%3A1)  
### 캘린더
<img width="959" alt="image" src="https://user-images.githubusercontent.com/22907483/142127892-ea63be35-ffe4-447b-96d9-87166896f0b1.png">

### 관극리포트
<img width="830" alt="image" src="https://user-images.githubusercontent.com/22907483/142128136-56c6fcec-f327-46de-819d-071aa7fc6174.png">

### 티켓팅 알림
<img width="912" alt="image" src="https://user-images.githubusercontent.com/22907483/142128303-745ebd8b-1a14-48bd-b38b-e293246c1297.png">

### 설정
<img width="370" alt="image" src="https://user-images.githubusercontent.com/22907483/142128358-35e6d736-5b59-400a-bbb6-4d82c095703c.png">
  
</div>
</details>

<details>
<summary>진행 과정</summary>
<div markdown="1">   
  
## 진행상황
no. | Date | Task | 팀 빌딩  
------ | ------ | ------ | ------ | 
1 | 21.11.15(월) | 서비스 주제 확정 및 와이어프레임 구성 | 기획 중인 아이디어 및 의견 공유
2 | 21.11.16(화) | 기획서 내용 보강, 기능 명세서 작성 시작, UI 수정사항 반영  
3 | 21.11.17(수) | 와이어프레임 마무리, 기능 명세서 작성 | 현재 기획단에서 고민 중인 부분에 대해 의견 나눔(View 구성, 기능 추가 여부 등)
4 | 21.11.18(목) | UI 디자인 마무리, 데이터베이스 스키마 구성 | 기획 발표 내용 중 서로 궁금한 부분 질의, 하루치 계획 공유
5 | 21.11.19(금) | 스키마 재구성, 티켓 오프 알림 View UI 구성 | 서로 궁금한 부분 질의, 하루치 계획 공유, Bug Bash Day 일정 픽스
6 | 21.11.20(토) | Detail Input View UI 구성, 저장 기능 구현
7 | 21.11.21(일) | FSCalendar custom, Detail Input View 정산 테이블과 연결
8 | 21.11.22(월) | - Calendar View에 등록된 일정 반영 구현</br>- Calendar PopUp View에 데이터 전달</br>- Calendar PopUp View의 TableViewCell과 DetailView 연결</br>- Detail View에서 저장/수정 기능 및 일일 저장 갯수 제한 구현</br>- Detail View의 DatePicker View 구현</br>- 관극리포트 View 라이브러리 서치 및 테스트(Parchment)| 주말동안 진행한 부분 공유
9 | 21.11.23(화) | - 차트 라이브러리 서치 및 테스트</br>- 정산 테이블 스키마 수정</br>- 관극리포트 View UI구현(Parchment)</br>- 관극리포트 View 데이터 반영 | 진행 과정 & 일일 Todo List 공유
10 | 21.11.24(수) | - 극 별 정산 TableView UI 구현</br>- 데이터 반영 및 정렬 기능 구현</br>- 극 별 정산 상세페이지 구현 | 어제 진행했던 부분 중 공유하고 싶은 정보 공유(스크롤뷰 업데이트 타이미, charts library, hierarchy)
11 | 21.11.25(목) | 발표준비하느라 ,,, 진행을 못한,,, | 
12 | 21.11.26(금) |
13 | 21.11.27(토) | - | -
14 | 21.11.28(일) | - | -
15 | 21.11.29(월) | - 앱 아이콘 일단 간단한 로고로 넣음 → 추후에 디자인 수정 후 업데이트 예정</br>- 일단 다크모드 막음(info.plist → Appearance → Light 추가) → 추후 업데이트 시 다크모드 대응 고려중</br>- 최소 버전  13.0으로 설정, 아이패드 해제, Portrait 설정</br>- KOPISAPIMangaer 코드 정리 → completion Handler에 struct를 만들어서 보냄 → view controller에서 훨씬 코드가 짧아짐!</br>- Detail View DatePicker 오류 개선(ButtonTitle에 Current Date 표시, 오늘 날짜 + 오후 8시로 Button Title Default 설정, Button 눌렀을 때 DatePicker Default Time도 똑같이 설정하기</br>- 저장된 데이터가 없을 때 → 관극 리포트에 "관극 데이터가 없어요 :(" label 추가 → 추후에 삭제 기능 추가한 뒤 삭제 후에도 잘 작동하는지 확인해야함(현재는 삭제 기능이 없어서 확인 불가)</br>- Search View에서 원하는 극 서치할 때 End Date를 현재로부터 1년뒤로 수정하여 아직 올라오지 않은 극도 서치가능하도록 수정</br>- Detail View UI 업데이트</br>- ImageView Shadow 추가 → 추가했는데 새로 추가할 때랑 calendarPopUp으로 진입할때랑 그림자 위치가 다르게보임.. 일단 그림자 삭제....</br>- dataview icon 수정</br>1. 새로 데이터를 추가하는 View 수정</br>- 저장하는 경우 Alert 띄우고 dismiss</br>- 캐스팅 작성할 때 TextView로 변경해서 작성하는 만큼 칸이 늘어나도록 설정</br>2. 이미 저장된 데이터 보는 View 수정</br>- 수정된 경우 Alert 띄우기</br>- SearchView UI 업데이트</br>- ReportView UI 업데이트</br>- ReportTableView UI 업데이트</br>- ReportDetailTableView UI 업데이트</br>- 관극 리포트 subview 동일년도 여러번 추가되는 오류 수정</br>- Detail 리뷰 및 캐스팅 textview placeholder 적용하기</br>- 데이터 수정하는 경우 Realm에 반영하기 | 주말동안 진행한 부분 공유 & Todo List 공유

## Iteration (11/18(목) ~ 11/21(일))

check | Task | 예상 시간 | 소요 시간 | 이유 |  
------ | ------ | ------ | ------ | ------ |   
✔️ | API Key 파일 구성 | 0.5h | 0.5h
✔️ | 네트워크 매니저 class 구현 | 1h | 0.5h
✔️ | Search View 구현 | 2h | 2h
✔️ | Detail Input View 구현 | 4h | 4h | Scroll View를 본격적으로 사용해본 것이 처음인데다가 내부에 Table View를 넣고 이를 구성하는 과정을 처음 겪어봐서 예상만큼 시간이 오래 걸렸다.
✔️ | Calendar View 구현 | 2h | 4h | 의도했던 디자인대로 라이브러리를 Custom하는 과정이 쉽지 않았다.
✔️ | Calendar Popup View 구현 | 2h | 1.5h
✔️ | 티켓오픈 알림 View 구현 | 1h | 2h | 티켓 오픈 시간이 지났을 때 Disable 처리해주는 부분을 추가하다보니 시간이 더 오래걸렸다.
✔️ | 정산용 테이블 스키마 짜기 | 0.5h | 0.5h

## Iteration (11/22(월) ~ 11/24(수))

check | Task | 예상 시간 | 소요 시간 | 이유 |  
------ | ------ | ------ | ------ | ------ |   
✔️ | DetailDatePicker View 구현 | 1h | DatePicker에서 Date를 받아올 때 데이터에 대한 이해가 부족해서 오류가 났다고 생각하여 시간을 더 투자하였다.
✔️ | 관극 리포트 구현 전 Charts 라이브러리 Test 및 정산 테이블 스키마 수정 | 1h | 2h | charts 라이브러리 자체의 오류가 발생해서 해결방법을 찾는데 시간이 오래 걸림 -> version을 예전 버전으로 확 낮춰서 설치하는걸로 해결했다.
✔️ | 관극리포트 View UI 구현(Parchment 활용) | 4h | 2h | Parchment 테스트를 미리 따로 진행하면서 라이브러리에 익숙해졌고 스크롤뷰를 여러 번 사용하다보니 사용하는 법을 확실하게 익혀서 생각보다 시간이 적게 걸렸다.
✔️ | 관극리포트 View Data 반영 | 1h | 1h
✔️ | 극 별 정산 View UI구현 | 2h
✔️ | 극 별 정산 DetailView 구현 | 2h
  
</div>
</details>
