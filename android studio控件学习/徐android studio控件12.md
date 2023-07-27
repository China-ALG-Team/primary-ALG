android studio控件12

Button长按点击事件:在线性布局中创建Button属性<?xml version="1.0" encoding="utf-8"?>

​                 <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"    

xmlns:app="http://schemas.android.com/apk/res-auto"    

xmlns:tools="http://schemas.android.com/tools"    

android:layout_width="match_parent"    

android:layout_height="match_parent"    

android:orientation="vertical">    

​                     <Button        

android:id="@+id/btn_long_click"        

android:layout_width="match_parent"        

android:layout_height="wrap_content"        

android:text="指定长按的点击事件监听"        

android:textColor="#000000"        

android:textSize="15sp"/>    

​                      <TextView        

android:id="@+id/tv_result"        

android:layout_width="match_parent"       

 android:layout_height="wrap_content"        

android:padding="5dp"       

 android:gravity="center"        

android:textSize="15sp"        

android:text="这里查看按钮点击的结果"/>

​                    </LinearLayout>

![1690477053411](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\1690477053411.png)

```java
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import gj.DateUtil;

public class ButtonLongClickActivity extends AppCompatActivity {



    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_button_long_click);
        TextView tv_result = findViewById(R.id.tv_result);
        Button btn_long_click=findViewById(R.id.btn_long_click);
        btn_long_click.setOnLongClickListener(v -> {
            String desc=String.format("%s 您点击了按钮：%s", DateUtil.getNowTime(), ((Button)v).getText());
            tv_result.setText(desc);
            return true;
        });
    }
}
```

