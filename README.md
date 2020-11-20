# Mobile Programmin Team Project



## ClothesMyGod (옷마이 갓) / 20175167 정현구 

@jhg3522

### 목차

| 내용          |
| ------------- |
| 프로젝트 소개 |
| 역할분담      |
| 기능          |



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
   ┃ ┃ ┃ ┃ ┃ ┣ 📜Board.java (20175167 정현구)
   ┃ ┃ ┃ ┃ ┃ ┣ 📜CodyItem.java
   ┃ ┃ ┃ ┃ ┃ ┣ 📜Comment.java (20175167 정현구)
   ┃ ┃ ┃ ┃ ┃ ┗ 📜PostData.java
   ┃ ┃ ┃ ┃ ┃ 
   ┃ ┃ ┃ ┃ ┣ 📂ui
   ┃ ┃ ┃ ┃ ┃ ┣ 📂board	 (20175167 정현구)
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜BoardActivity.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜BoardAdapter.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜BoardFragment.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentAdapter.java
   ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜PostBoardActivity.java
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
   ┃ ┃ ┃ ┃ ┃ ┣ 📜LoginActivity.java
   ┃ ┃ ┃ ┃ ┃ ┣ 📜MainActivity.java
   ┃ ┃ ┃ ┃ ┃ ┣ 📜SignUpActivitiy.java
   ┃ ┃ ┃ ┃ ┃ ┗ 📜SplashActivity.java
   ┣ 📂res
   ┃ ┣ 📂drawable	 	(20175167 정현구)
   ┃ ┃ ┣ 📜board_wrap.xml
   ┃ ┃ ┣ 📜cody_wrap.xml
   ┃ ┃ ┣ 📜comment_wrap.xml
   ┃ ┃ ┣ 📜edittext_border.xml
   ┃ ┃ ┣ 📜login_button.xml
   ┃ ┃ ┣ 📜menu_button.xml
   ┃ ┃ ┣ 📜nabvar_wrap.xml
   ┃ ┃ ┣ 📜register_button.xml
   ┃ ┃ ┣ 📜register_eidt.xml
   ┃ ┃ ┗ 📜splash.xml
   ┃ ┃ 
   ┃ ┣ 📂layout		 (20175167 정현구)
   ┃ ┃ ┣ 📜activity_board.xml
   ┃ ┃ ┣ 📜activity_login.xml
   ┃ ┃ ┣ 📜activity_main.xml
   ┃ ┃ ┣ 📜activity_mycodylist.xml
   ┃ ┃ ┣ 📜activity_signup.xml
   ┃ ┃
   ┃ ┃ ┣ 📜board_list.xml
   ┃ ┃ ┣ 📜board_post.xml
   ┃ ┃
   ┃ ┃ ┣ 📜comment_list.xml
   ┃ ┃
   ┃ ┃ ┣ 📜fragment_board.xml
   ┃ ┃ ┣ 📜fragment_calendar.xml
   ┃ ┃ ┣ 📜fragment_mycloset.xml
   ┃ ┃ ┣ 📜fragment_mycody.xml
   ┃ ┃
   ┃ ┃ ┣ 📜mycloset_card_item.xml
   ┃ ┃ ┣ 📜mycloset_post_clothes.xml
   ┃ ┃
   ┃ ┃ ┣ 📜mycody_item.xml
   ┃ ┃ ┣ 📜mycody_postcody.xml
   ┃ ┃ ┣ 📜mycody_select_category.xml
   ┃ ┃ ┗ 📜mycody_select_item.xml
   ┗ 📜AndroidManifest.xml
   
   
  
  ```



### 역할분담

---

#### 2017 소프트웨어학과 정현구 @jhg3522

> - front-end
> - splash 화면
> - 질문게시판, logout_btn





### 주요 기능

---

#### 1. Front-end 

 1. splash 화면

    <div><img src="https://user-images.githubusercontent.com/50823103/99775266-5945ee80-2b52-11eb-87e3-f9288bb093f7.JPG" alt="mp8" style="zoom:50%;" />


    **-AndroidManifest.xml**

     ```xml
    <activity
        android:name=".SplashActivity"
        android:theme="@style/SplashTheme">
        <intent-filter>
              <action android:name="android.intent.action.MAIN" />
              <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>
    </activity>
     ```

    **-res/values/styles.xml**

    ```xml
    <style name="SplashTheme" parent="Theme.AppCompat.NoActionBar">
        <item name="android:windowBackground">@drawable/splash</item>
    </style>
    ```

    **-res/drawable/spalsh.xml**

    ```xml
    <layer-list xmlns:android="http://schemas.android.com/apk/res/android"
        android:opacity="opaque">
        <item android:drawable="@drawable/main" />
        <item
            android:drawable="@drawable/logotext2"
            android:gravity="center"
            android:bottom="250dp"
            />
    </layer-list>
    ```

    처음에는 splash layout을 만들어서 SplashActivity에서 handler를 사용하여 splash layout을 먼저 실행한 후 login layout으로 넘어가게 구현하였다.

    하지만 자원 낭비가 심하다는것을 알게 되었고 styles을 통해 Theme을 만들어서 Manifest에 SplashActivity를 선언할때 Theme을 지정해주는 방법으로 개선하였다.

    

 2. layout에 사용되는 component xml

    ```
    ┣ 📂res
     ┃ ┣ 📂drawable	 	(20175167 정현구)
     ┃ ┃ ┣ 📜board_wrap.xml
     ┃ ┃ ┣ 📜cody_wrap.xml
     ┃ ┃ ┣ 📜comment_wrap.xml
     ┃ ┃ ┣ 📜edittext_border.xml
     ┃ ┃ ┣ 📜login_button.xml
     ┃ ┃ ┣ 📜menu_button.xml
     ┃ ┃ ┣ 📜nabvar_wrap.xml
     ┃ ┃ ┣ 📜register_button.xml
     ┃ ┃ ┣ 📜register_eidt.xml
    ```

     layout 디자인을 할 때 편리하게 제작할 수 있게 컴포넌트 별로 xml을 작성하였다.

    - image

      <div>
          <img src="https://user-images.githubusercontent.com/50823103/99777802-2b62a900-2b56-11eb-8bdb-020109670459.JPG" alt="mp10" style="zoom: 100%;" />
          <img src="https://user-images.githubusercontent.com/50823103/99777808-2bfb3f80-2b56-11eb-8f71-49a6867a2b44.JPG" alt="mp11" style="zoom:150%;" />
          <img src="https://user-images.githubusercontent.com/50823103/99777809-2bfb3f80-2b56-11eb-972d-0fde8e6918ce.JPG" alt="mp12" style="zoom:80%;" />
          <img src="https://user-images.githubusercontent.com/50823103/99777811-2c93d600-2b56-11eb-85ab-4dcf89dc4557.JPG" alt="mp13" style="zoom:67%;" />
          <img src="https://user-images.githubusercontent.com/50823103/99777814-2d2c6c80-2b56-11eb-94fa-a2d709f5992f.JPG" alt="mp14" style="zoom:50%;" />
      </div>

      

 3. 전반적인 layout 구조 설계

    <img src="https://user-images.githubusercontent.com/50823103/99778875-9eb8ea80-2b57-11eb-919d-2e2a7da82c6b.JPG" alt="m1" style="zoom:33%;" /><img src="https://user-images.githubusercontent.com/50823103/99778881-9fea1780-2b57-11eb-96d3-b9caa4fd5191.JPG" alt="m2" style="zoom:33%;" /><img src="https://user-images.githubusercontent.com/50823103/99778888-a11b4480-2b57-11eb-92c5-344cf3e157e3.JPG" alt="m3" style="zoom:33%;" /><img src="https://user-images.githubusercontent.com/50823103/99778883-a082ae00-2b57-11eb-96c6-9ab94bd215af.JPG" alt="m7" style="zoom:33%;" /><img src="https://user-images.githubusercontent.com/50823103/99778885-a082ae00-2b57-11eb-8f08-e54a844ba2c3.JPG" alt="m8" style="zoom:33%;" />

    <img src="https://user-images.githubusercontent.com/50823103/99778892-a24c7180-2b57-11eb-8c89-d76f83a1c8f0.JPG" alt="m6" style="zoom:33%;" /><img src="https://user-images.githubusercontent.com/50823103/99778891-a1b3db00-2b57-11eb-922f-5540ed1fa8a6.JPG" alt="m5" style="zoom:33%;" /><img src="https://user-images.githubusercontent.com/50823103/99778889-a11b4480-2b57-11eb-950e-18a19b962ec7.JPG" alt="m4" style="zoom:33%;" />

    수업시간에 배운 LinearLayout, RelativeLayout, FrameLayout, GridLayout등을 디자인에 맞게 적절하게 사용해서 작성하였다.

#### 2. 질문게시판

> 1. Board
>
>    - BoardActivity.class
>    - BoardFragment.class
>
>    - PostBoardActivity.class



**-BoardFragment.class**

```java
public class BoardFragment extends Fragment {
    private View view;

    public View onCreateView(@NonNull LayoutInflater inflater,
                             ViewGroup container, Bundle savedInstanceState) {
        //fragment를 위한 view     (정현구)
        view = inflater.inflate(R.layout.fragment_board,container,false);
        view.findViewById(R.id.board_post_btn).setOnClickListener(onClickListener);
        //firebase에 있는 데이터를 출력할 ListView     (정현구)
        //이벤트 리스너 안에서 사용하기위해서 final로 선언     (정현구)
        final ListView listView = (ListView)view.findViewById(R.id.board_listView);
        final ArrayList<Board> boardData = new ArrayList<>();
        //firebase 읽기를 위한 db
        DatabaseReference db = FirebaseDatabase.getInstance().getReference();
        DatabaseReference boardDBRef = db.child("board");

        //firebase Realtime Database의 정보를 얻기위한 이벤트 리스너      (정현구)
       ValueEventListener mValueEventListener = new ValueEventListener() {
           @Override
           public void onDataChange(@NonNull DataSnapshot snapshot) {
               //중복 데이터 출력 제거를 위하여 clear     (정현구)
               boardData.clear();
               //Board의 모델 객체를 생성하여 db에서 데이터를 객체에 저장후 boardData에 add      (정현구)
               for (DataSnapshot datasnapshot : snapshot.getChildren()) {
                   Board board = datasnapshot.getValue(Board.class);
                   board.setKey(datasnapshot.getKey());
                   boardData.add(board);
               }
               //데이터를 BoardAdapter를 사용하여 ListView에 담기      (정현구)
               BoardAdapter adapter = new BoardAdapter(boardData);
               listView.setAdapter(adapter);
               //리스트뷰 item 클릭 리스너, 클릭시 item의 키값을 intent로 넘겨서 게시판 출력      (정현구)
               listView.setOnItemClickListener(new AdapterView.OnItemClickListener() {
                   @Override
                   public void onItemClick(AdapterView<?> adapterView, View view, int i, long l) {
                       String data=boardData.get(i).getKey();
                       Intent intent = new Intent(getActivity(),BoardActivity.class);
                       intent.putExtra("key",data);
                       startActivity(intent);
                   }
               });
           }
           @Override
           public void onCancelled(@NonNull DatabaseError error) {

           }
       };
       boardDBRef.addValueEventListener(mValueEventListener);
        return view;
    }
    //클릭 이벤트리스너 (정현구)
    View.OnClickListener onClickListener = new View.OnClickListener(){
        @Override
        public void onClick(View v) {
            //게시판 포스트 페이지로 이동
            if (v.getId() == R.id.board_post_btn) {
                Intent intent = new Intent(getActivity(), PostBoardActivity.class);
                startActivity(intent);
            }
        }
    };
}
```

- BoardFragment.class 에서는 board_post_btn을 통해서 PostBoardActivity.class로 액티비티 전환 기능과 Firebase Realtime Database의 "board" child에 있는 Board 객체를 가져와 Listview형태로 출력해주는 기능을 한다.

- 또한 Listview item Click Listener를 통해서 게시판을 선택시에 선택한 포지션의 key를 BoardActivity.class로 넘겨주면서 액티비티 전환 기능을 한다.

  

**-BoardActivity.class**

```java
public class BoardActivity extends AppCompatActivity {
    private FirebaseAuth mAuth = FirebaseAuth.getInstance(); //현재 유저정보 가져오기 (정현구)
    FirebaseUser currentUser= mAuth.getCurrentUser();  //유저정보 저장 (정현구)
    DatabaseReference db = FirebaseDatabase.getInstance().getReference(); //Realtime database 정보 가져오기 																				(정현구)
    DatabaseReference boardDBRef = db.child("board"); //child가 board인 정보 가져오기 (정현구)
    //layout안에 view 사용을 위한 선언 (정현구)
    TextView textTitle;
    TextView textContent;
    TextView textAuthor;
    Button edit_btn;
    EditText board_edit;

    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_board);
        //댓글 출력을 위한 listview (정현구)
        final ListView listView = (ListView)findViewById(R.id.board_comment_listView);
        final ArrayList<Comment> commentData = new ArrayList<>();
        //id값으로 연결 (정현구)
        textTitle = (TextView)findViewById(R.id.board_title);
        textContent = (TextView)findViewById(R.id.board_content);
        textAuthor = (TextView)findViewById(R.id.board_author);
        edit_btn = (Button)findViewById(R.id.board_edit_btn);
        board_edit = (EditText)findViewById(R.id.board_edit);
        Intent intent= getIntent(); //게시글 등록시에 넘겼던 intent를 받음 (정현구)
        final String key = intent.getExtras().getString("key");//intent에서 key값 가져오기 (정현구)
        final DatabaseReference DBRef = db.child("board").child(key);// 키값을 통해서 클릭했던 게시글의 정보 가져오																		기   (정현구)
        final DatabaseReference commentRef = DBRef.child("comment");// child가 comment인 정보를 가져오기         																	(정현구)
        //실시간 댓글 달기 버튼 클릭 리스너 (정현구)
        edit_btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                //글쓴이는 현재유저의 이메일, EditText에서 받은 내용 String으로 받아와 comment객체에 저장					         (정현구)
                String author = currentUser.getEmail();
                String content = board_edit.getText().toString();
                Comment comment =new Comment(author,content);
                //빈내용이 없을시에 child가 "comment"인 하위노드로 comment 형태로 저장 (정현구)
                if(!content.equals("")){
                    DBRef.child("comment").push().setValue(comment);
                    board_edit.setText(""); // EditText 부분 초기화(정현구)
                }
                else{
                    Toast.makeText(BoardActivity.this,"내용을 입력하세요",Toast.LENGTH_SHORT).show();
                }
            }
        });
        //intent로 받아온 key값 안에 저장되어있는 정보 가져오는 리스너         (정현구)
        ValueEventListener mValueEventListener = new ValueEventListener() {
            @Override
            public void onDataChange(@NonNull DataSnapshot snapshot) {
                Board board =snapshot.child(key).getValue(Board.class);//키값 아래에 Board 객체 형태로 값 가져옴         (정현구)
                //각각의 Textview에 getter를 사용하여 set해줌 (정현구)
                textAuthor.setText(board.getAuthor());
                textTitle.setText(board.getTitle());
                textContent.setText(board.getContent());
            }

            @Override
            public void onCancelled(@NonNull DatabaseError error) {

            }
        };
        //실시간 댓글을 위한 이벤트 리스너 (정현구)
        ValueEventListener commentValueEventListener = new ValueEventListener() {
            @Override
            public void onDataChange(@NonNull DataSnapshot snapshot) {
                commentData.clear();//댓글의 중복 출력 제거 (정현구)
                for (DataSnapshot datasnapshot : snapshot.getChildren()) {
                    Comment comment = datasnapshot.getValue(Comment.class);
                    commentData.add(comment);
                }
                CommentAdapter adapter = new CommentAdapter(commentData);
                listView.setAdapter(adapter);
            }

            @Override
            public void onCancelled(@NonNull DatabaseError error) {

            }
        };
        boardDBRef.addValueEventListener(mValueEventListener);
        commentRef.addValueEventListener(commentValueEventListener);
    }
}
```

- BoardFragment에서 Intent로 받은 key를 통해서 child("board").chile(key)로 게시판에서 선택한 게시판의 정보를 가져와 각각의 TextView에 Setvalue로 값을 지정해준다.

- 또한, 실시간 댓글 기능으로 EditText에 입력한 내용을 버튼을 클릭시에 클릭 이벤트 리스너를 통해서 DB에 해당 게시판에 child("comment")를 생성하여 하위 노드에 Comment객체 형태로 저장

- 저장한 내용을 onDataChange 메소드를 통해서 comment에 있는 하위노드를 가져와 Listview로 출력해준다.

  

**-PostBoardActivity.class**

```java
public class PostBoardActivity extends AppCompatActivity {
    //firebase 사용을 위한 선언        (정현구)
    private FirebaseAuth mAuth= FirebaseAuth.getInstance(); //유저 정보를 사용        (정현구)
    private DatabaseReference mDatabase= FirebaseDatabase.getInstance().getReference();//Realtime Database 사용        (정현구)
    FirebaseUser currentUser= mAuth.getCurrentUser(); //현재 유저 정보 저장        (정현구)
    Button postBoardBtn;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.board_post);

        postBoardBtn = findViewById(R.id.post_board_btn); //게시물 등록 버튼         (정현구)
        // 버튼 클릭 리스너         (정현구)
        postBoardBtn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String author = currentUser.getEmail(); //현재 유저의 이메일 정보를 글쓴이에 저장         (정현구)
                //글 제목과 내용은 각각의 EditText의 내용을 String 형태로 저장         (정현구)
                String post_name = ((EditText) findViewById(R.id.post_board_name)).getText().toString();
                String post_content = ((EditText) findViewById(R.id.post_board_content)).getText().toString();
                Board board =new Board(author,post_name,post_content); // board 객체를 위에 내용으로 생성
                //게시글의 내용중 빈내용이 있을시에 Toast메세지 출력        (정현구)
                //없을시에는 RealtimeDatabase의 "board"하위에 board객체형태로 push        (정현구)
                if(!post_content.equals("") && !post_name.equals("")) {
                    mDatabase.child("board").push().setValue(board);
                    Intent intent = new Intent(PostBoardActivity.this, MainActivity.class);
                    startActivity(intent);
                }
                else{
                    Toast.makeText(PostBoardActivity.this,"제목과 내용을 모두 입력해주세요",Toast.LENGTH_SHORT).show();
                }
            }
        });
    }
}
```

- 게시물을 작성하는 Activity로 버튼 클릭 리스너를 사용하여 EditText로 입력된 제목과 내용을 firebase Realtime Database에서 "board" child 하위에 저장한다.
- 내용이나 제목중 하나라도 입력이 되지않으면 Toast 메세지가 출력된다. 만약 모두 입력시에는 위에 기능이 작동되고 MainActivity로 전환된다.

### 기능 실행 

---

#### 1. BoardFragment

<img src="https://user-images.githubusercontent.com/50823103/99775251-564afe00-2b52-11eb-9f60-186138c2596b.JPG" alt="mp1" style="zoom:80%;" /><img src="https://user-images.githubusercontent.com/50823103/99793261-bd28e100-2b6b-11eb-8480-3437071d1393.JPG" alt="e1" style="zoom:67%;" />

#### **2.PostBoardActivity**

<img src="https://user-images.githubusercontent.com/50823103/99775254-577c2b00-2b52-11eb-95a9-fe3817666c9c.JPG" alt="mp2" style="zoom: 67%;" /><img src="https://user-images.githubusercontent.com/50823103/99775257-5814c180-2b52-11eb-9646-01658770f67c.JPG" alt="mp4" style="zoom:67%;" /><img src="https://user-images.githubusercontent.com/50823103/99775256-577c2b00-2b52-11eb-99f3-27e53d527e1a.JPG" alt="mp3" style="zoom: 67%;" />

#### **3.BoardActivity**

#### <img src="https://user-images.githubusercontent.com/50823103/99775260-5814c180-2b52-11eb-92ed-b01c40e34c77.JPG" alt="mp5" style="zoom:67%;" /><img src="https://user-images.githubusercontent.com/50823103/99775262-58ad5800-2b52-11eb-8623-7c0924227ae5.JPG" alt="mp6" style="zoom:67%;" /><img src="https://user-images.githubusercontent.com/50823103/99775263-58ad5800-2b52-11eb-9592-b97f51be3f6f.JPG" alt="mp7" style="zoom:67%;" />

#### **4.Logout_btn**

<img src="https://user-images.githubusercontent.com/50823103/99775267-5945ee80-2b52-11eb-8068-84ec24377d0e.JPG" alt="mp9" style="zoom:67%;" />









