## Mobile Programming Team Project 

**: Clothes My God (옷마이갓 )**



#### 20175161 소프트웨어학과 김현서 @Chord.West

> - 데이터베이스 ( Firebase 연동 )
> - 로그인, 회원가입, 내 옷장, 나의 코디 



### 목차

| 내용             |
| ---------------- |
| 프로젝트 소개    |
| 내가 구현한 기능 |



### 프로젝트 소개

---

- #### 개발 동기 및 목적

  > 사람들은 매일 아침마다 스타일 코디를 위해 착의하고 탈의하는 과정을 수없이 반복한다. 또한 어떤 사람들은 옷이 많아서 자신의 옷장에 어떤 옷들이 있는지 알 수 없고, 어떤 사람들은 일주일에 세네번 같은 옷을 입기도 한다. 우리는 사용자 개인 맞춤에 중점을 두어 사용자가 가지고 있는 옷들을 바탕으로 "오늘 뭐 입지?”, “저번에 이 친구 만날 때 뭐 입었지?” 라는 고민을 덜어주고자 한다.

  

- ####  개요

  > 옷장에 있는 옷들을 카메라로 촬영한뒤 핸드폰 어플 속에 저장해서  현재 보유하고 있는 옷들을 한눈에 
  >
  > 살펴볼 수 있고, 옷들의 조합을 코디리스트로 저장해서 관리할 수 있다.
  >
  > 그리고 캘린더를 통해 언제 옷을 입을지 정할 수 있고, 게시판을 통해 코디에 대한 질문도 할 수 있다. 
  
  
  
- #### 개발 환경

  > Compile Sdk Vesrion : 30 ( API 30 : Android 10.0 + (R))
  >
  > 언어 : Java 사용
  >
  > Build Tools Version : 30.0.2
  >
  > Android Gradle Plugin Vesrion : 4.0.1
  >
  > Gradle Version : 6.1.1
  >
  > AVD : Pixel 2 API 30
  >
  > 데이터 베이스 : Firebase 

  

- #### 프로젝트 구조

  ```
  📦main
   ┣ 📂java
   ┃ ┗ 📂com
   ┃ ┃ ┗ 📂example
   ┃ ┃ ┃ ┗ 📂clothesmygod
   ┃ ┃ ┃ ┃ ┣ 📂Model
   ┃ ┃ ┃ ┃ ┃ ┣ 📜CodyItem.java
   ┃ ┃ ┃ ┃ ┃ ┣ 📜PostData.java
   ┃ ┃ ┃ ┃ ┃ 
   ┃ ┃ ┃ ┃ ┣ 📂ui
   ┃ ┃ ┃ ┃ ┃ ┣ 📂board
   ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜BoardFragment.java
   ┃ ┃ ┃ ┃ ┃ ┃ 
   ┃ ┃ ┃ ┃ ┃ ┣ 📂calendar
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CalendarFragment.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MyCodyListActivity.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜MyCodyListAdpater.java
   ┃ ┃ ┃ ┃ ┃ ┃
   ┃ ┃ ┃ ┃ ┃ ┣ 📂mycloset
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MyClosetAdapter.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MyClosetFragment.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜PostClothesActivity.java
   ┃ ┃ ┃ ┃ ┃ ┃
   ┃ ┃ ┃ ┃ ┃ ┗ 📂mycody
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MyCodyAdapter.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MyCodyFragment.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostCodyActivity.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜SelectAdpater.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SelectCategory.java
   ┃ ┃ ┃ ┃ ┃ 
   ┃ ┃ ┃ ┃ ┣ 📜LoginActivity.java
   ┃ ┃ ┃ ┃ ┣ 📜MainActivity.java
   ┃ ┃ ┃ ┃ ┣ 📜SignUpActivitiy.java
   ┃ ┃ ┃ ┃ ┗ 📜SplashActivity.java
   ┣ 📂res
   ┃ ┣ 📂layout
   ┃ ┃ ┣ 📜activity_login.xml
   ┃ ┃ ┣ 📜activity_main.xml
   ┃ ┃ ┣ 📜activity_mycodylist.xml
   ┃ ┃ ┣ 📜activity_signup.xml
   ┃ ┃ ┣ 📜fragment_board.xml
   ┃ ┃ ┣ 📜fragment_calendar.xml
   ┃ ┃ ┣ 📜fragment_mycloset.xml
   ┃ ┃ ┣ 📜fragment_mycody.xml
   ┃ ┃ ┣ 📜mycloset_card_item.xml
   ┃ ┃ ┣ 📜mycloset_post_clothes.xml
   ┃ ┃ ┣ 📜mycody_item.xml
   ┃ ┃ ┣ 📜mycody_postcody.xml
   ┃ ┃ ┣ 📜mycody_select_category.xml
   ┃ ┃ ┗ 📜mycody_select_item.xml
   ┃ 
   ┗ 📜AndroidManifest.xml
   
   
  
  ```
  

### 내가 구현한 기능

---

#### 1. 로그인, 회원가입 

<div style="display:flex; justify-content : space-evenly;">
    <img src="https://user-images.githubusercontent.com/50789483/99502579-9b3f2b00-29c0-11eb-8097-9f9f60bda919.png" style="width:300px; height:400px;" />
	<img src="https://user-images.githubusercontent.com/50789483/99502215-1ce28900-29c0-11eb-8bbd-8069ebe2a83a.png" style="width:300px; height:400px;" />
</div>



- ##### 회원가입 ( Firebase Auth 사용 )

  <div>
  	<img src="https://i.imgur.com/Bf97WeF.png" style="width:800px; height:400px;" />
      <img src="https://user-images.githubusercontent.com/50789483/99500383-a6448c00-29bd-11eb-94a2-481c20d8becc.PNG" style="width:800px; height:400px;" />
  </div>

  


  - 회원가입 버튼 클릭시 Edittext가 null 값인 경우 "아이디와 비밀번호를 모두 입력해주세요." 라는 Toast 메세지 출력.

  - 회원가입 완료후 Firebase Authenctication에 UID와 함께 e-mail 형식으로 저장됨.

    

- ##### 로그인

  - 로그인 성공시 FirebaseUser 메소드를 통해 CurrentUser의 UID를 통해 자동 로그인이 활성화 되고,  User의 정보를 불러옴.

  

#### 2. 내 옷장


- Firebase RealTimeDatabase, Storage 사용
  
  - User의 데이터베이스에 저장된 카테고리 별로 저장된 옷의 이름을 Storage와 연동시켜 화면에 출력
  

<div style="display:flex; justify-content : space-evenly;">
    <img src="https://user-images.githubusercontent.com/50789483/99527109-9b9aee80-29df-11eb-905c-6af0be7e40dd.PNG" style="width:300px; height:400px;" />
	<img src="https://user-images.githubusercontent.com/50789483/99527159-af465500-29df-11eb-9628-58396ac78243.PNG" style="width:300px; height:400px;" />
    <img src="https://user-images.githubusercontent.com/50789483/99527203-c5ecac00-29df-11eb-8193-dd4d985bc2c3.PNG" style="width:300px; height:400px;" />
</div>



- 메인
  
  - GridView 의 Adapter에서 Glide API를 통해서 Firebase Storage의 저장된 파일들을 URI로 불러와서 User가 가진 카테고리의 옷이름과 일치하면 ViewHolder를 통해 ImageView에 고정시켜 화면에 출력시킴.  
  
  - <div>
    	<img src="https://i.imgur.com/t2uSs1v.png" style="width:600px; height:300px; margin-bottom : 50px" />
        	<img src="https://i.imgur.com/6nUutXo.png" style="width:600px; height:200px;" />
    </div>
  
- 옷 등록
  
  <div>
  	<img src="https://user-images.githubusercontent.com/50789483/99636903-71047080-2a87-11eb-97da-9602ca6222ec.png" style="width:700px; height:200px; margin-bottom : 50px" />
      <img src="https://user-images.githubusercontent.com/50789483/99638031-03f1da80-2a89-11eb-8e58-bbbbe8d66280.PNG" style="width:400px; height:200px;" />	
      <img src="https://user-images.githubusercontent.com/50789483/99637980-ee7cb080-2a88-11eb-8dc5-23866fae9c14.PNG" style="width:400px; height:200px;" />
  </div>
  
  
  - 옷등록을 하기전에  ImageView에 핸드폰 갤러리에서 가져온 이미지를 고정 하기 위해서 
    
    먼저  유저에게 갤러리에 접근할 수 있게하는 권한 요청하는 READ_EXTERNAL_STORAGE을 실시
    
  - Allow 클릭시, 갤러리에 접근 가능하고, 이미지 클릭시 onActivityResult를 통해서 REQUSET_CODE
    
    일치 시  
    
    
    
  - Radix Group을 통해 카테고리 선택가능.
  
    
  
  - 옷의 이름과 카테고리가 User 정보의 저장됨.
  
    
  
- 옷 삭제
  
  - GridView 메소드인 setOnItemLongClickListener를 통해서  길게 클릭시 AlertDialogBuilder 객체를 생성해서 삭제할 것인지 물어보고, 삭제 클릭 시 StorageReference와 DatabaseReference 메소드를 통해서 유저의 정보와 파일을 동시에 삭제한다.
  
    

#### 3. 나의 코디



<div style="display:flex; justify-content : space-evenly;">
    <img src="https://user-images.githubusercontent.com/50789483/99635942-11599580-2a86-11eb-9b2f-fef07b2a4681.PNG" style="width:300px; height:400px;" />
	<img src="https://user-images.githubusercontent.com/50789483/99635968-1f0f1b00-2a86-11eb-99c2-070e41d0eee6.PNG" style="width:300px; height:400px;" />
    <img src="https://user-images.githubusercontent.com/50789483/99636011-2df5cd80-2a86-11eb-910f-f210f1f06dc0.PNG" style="width:300px; height:400px;" />

- 메인

  - Firebase의 User의 UID에서 Child("codylist")에 CodyItem들을 객체를 불러와 Glide 객체를 통해서 카테고리별로 일치하는 이름을 Storage와 일치하면 Imageview와 TextView에 각각 고정 후 출력.

- 코디 저장

  - 카테고리별로 ImageView를 클릭하면 나의 옷장에서 아이템을 선택해 ImageView에  저장.
  - 코디 등록시 코디명과 함게 Firebase의 User의 UID에서 Child("codylist")에 Object형식으로 저장.

- 코디 삭제

  - 삭제 버튼 클릭시  AlertDialogBuilder 객체를 생성해서 삭제할 것인지 물어보고, 삭제 클릭 시  User의 "codylist"에서 코디명과 일치하는 데이터 삭제.

    


