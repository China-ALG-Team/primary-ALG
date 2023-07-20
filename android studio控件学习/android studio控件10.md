android studio控件10

Button点击按钮:在线性布局中创建Button属性<LinearLayout   xmlns:android="http://schemas.android.com/apk/res/android"                                               android:layout_width="match_parent"   

​                                                  android:layout_height="match_parent"    

​                                                  android:orientation="vertical"    

​                                                  android:padding="5dp">    

​                            <TextView       

 android:layout_width="match_parent"        

android:layout_height="wrap_content"        

android:text="下面的按钮英文默认小写"        

android:textColor="@color/black"        

android:textSize="17sp"        

android:gravity="center"/>    

​                          <Button        

android:layout_width="match_parent"        

android:layout_height="wrap_content"       

 android:text="hello world"        

android:textColor="@color/black"        

android:textSize="17sp" />    

​                            <TextView        

android:layout_width="match_parent"        

android:layout_height="wrap_content"        

android:text="下面的按钮英文大写"        

android:textColor="@color/black"        

android:textSize="17sp"        

android:gravity="center"/>    

​                            <Button       

 android:layout_width="match_parent"       

 android:layout_height="wrap_content"        

android:text="hello world"        

android:textColor="@color/black"        

android:textSize="17sp"        

android:textAllCaps="true" />    

​                            <Button        

android:layout_width="match_parent"        

android:layout_height="wrap_content"        

android:text="直接指定点击方法"        

android:textColor="@color/black"        

android:textSize="17sp"        

android:textAllCaps="true"        

android:onClick="doClick"/>    

​                          <TextView        

android:id="@+id/tv_result"        

android:layout_width="match_parent"        

android:layout_height="wrap_content"        

android:text="这里查看按钮的点击结果"        

android:textColor="@color/black"        

android:textSize="17sp"        />

​                         </LinearLayout>

![1689869267959](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\1689869267959.png)



```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;



public class MainActivity extends AppCompatActivity {

    private TextView tv_result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        tv_result=findViewById(R.id.tv_result);
    }
    public void doClick(View view){

        String desc=String.format("%s 您点击了按钮：%s",DateUtil.getNowTime(),((Button)view).getText());
        tv_result.setText(desc);

    }
}
```

![1689869348177](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\1689869348177.png)





```
package com.example.myapplication;

import android.annotation.SuppressLint;

import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.logging.SimpleFormatter;

public class DateUtil {

    public static String getNowTime(){
       SimpleDateFormat sdf=new SimpleDateFormat("HH:mm:ss");
        return sdf.format(new Date());
    }
}
```

![1689869383171](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\1689869383171.png)