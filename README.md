## 기말고사


   public class MainActivity extends AppCompatActivity {
    //변수선언 해줍니다.
    TextView text1;
    Button button1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        
        // 뷰 아이디를 찾을 수 있게 해줍니다.
        text1 = (TextView) findViewById(R.id.text1);
        button1 = (Button) findViewById(R.id.button1);

        //버튼을 클릭 했을 때 이벤트를 생성해줍니다.
        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                // int 변수 선언해줍니다.
                int dicenum = 0;

                // Random 선언해줍니다.
                Random random = new Random();

                // 1~6까지 숫자를 가져올 수 있게 해줍니다.
                dicenum = random.nextInt(6) + 1;


                //출력
                text1.setText(String.valueOf(dicenum));
            }
        });
    }
}
