Android Weak Handler - Upgrade Version
====================
It is forked from [badoo/android-weak-handler](https://github.com/badoo/android-weak-handler).

I modified some implementations ,then using it more like **android.os.Handler**


```java
public class ExampleActivity extends Activity {

    private WeakHandler mHandler; // We still need at least one hard reference to WeakHandler

    private View mView;
    
    protected void onCreate(Bundle savedInstanceState) {
        mHandler = new WeakHandler(){
            @override
            public void handleMessage(Message msg){
                view.setVisibility(View.INVISIBLE);
            }
        }.sendEmptyMessage(0);
        ...
    }
}
```

Read more information, click [here](https://github.com/badoo/android-weak-handler)