android studio控件11

Button点击事件:在线性布局中创建Button属性<?xml version="1.0" encoding="utf-8"?>

​               <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"    

xmlns:app="http://schemas.android.com/apk/res-auto"    

xmlns:tools="http://schemas.android.com/tools"   

 android:layout_width="match_parent"   

 android:layout_height="match_parent"    

android:orientation="vertical">    

​                        <Button        

android:id="@+id/btn_click_single"        

android:layout_width="match_parent"        

android:layout_height="wrap_content"        

android:text="指定单独的点击事件监听"        

android:textColor="#000000"        

android:textSize="15sp"/>   

​                             <TextView       

 android:id="@+id/tv_result"        

android:layout_width="match_parent"        

android:layout_height="wrap_content"       

 android:padding="5dp"        

android:gravity="center"        

android:textSize="15sp"        

android:text="这里查看按钮点击的结果"/>

​                        </LinearLayout>

![1690476818278](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\1690476818278.png)

```java
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import java.text.SimpleDateFormat;
import java.util.Date;

import gj.DateUtil;

public class ButtonClickActivity extends AppCompatActivity {

    private TextView tv_result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_button_click);
        tv_result = findViewById(R.id.tv_result);
        Button btn_click_single=findViewById(R.id.btn_click_single);
        btn_click_single.setOnClickListener(new MyOnClickListener(tv_result));
    }


    static class MyOnClickListener implements View.OnClickListener{
        private final TextView tv_result;

        public MyOnClickListener(TextView tv_result) {
            this.tv_result=tv_result;
        }

        @Override
        public void onClick(View v){
            String desc=String.format("%s 您点击了按钮：%s", DateUtil.getNowTime(), ((Button) v).getText());
            tv_result.setText(desc);

        }
    }
}
```

