android studio控件13

禁用与恢复按钮：

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="5dp">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        <Button
            android:id="@+id/btn_enable"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="启用测试按钮"
            android:textColor="@color/black"
            android:textSize="17sp"/>
        <Button
            android:id="@+id/btn_disable"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="禁用测试按钮"
            android:textColor="#000000"
            android:textSize="17sp"/>
    </LinearLayout>
    <Button
        android:id="@+id/btn_test"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="测试按钮"
        android:textSize="17sp"
        android:textColor="#000000"
        android:enabled="false"/>
    <TextView
        android:id="@+id/tv_result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="这里查看测试按钮点击结果"
        android:textSize="17sp"
        android:textColor="#000000"/>






</LinearLayout>
```

```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

public class ButtonEnableActivity extends AppCompatActivity implements View.OnClickListener {

   private Button btn_test;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_button_enable);
        Button btn_enable= findViewById(R.id.btn_enable);
        Button btn_disable= findViewById(R.id.btn_disable);
        btn_test = findViewById(R.id.btn_test);
        TextView tv_result= findViewById(R.id.tv_result);

        btn_enable.setOnClickListener(this);
        btn_disable.setOnClickListener(this);
        btn_test.setOnClickListener(this);

    }

   @Override
    public void onClick(View v) {
        switch (v.getId()){
            case R.id.btn_enable:
                //启用当前控件
                btn_test.setEnabled(true);
                //设置按钮颜色为黑色
                btn_test.setTextColor(Color.BLACK);
                break;
            case R.id.btn_disable:
                //重置当前控件
                btn_test.setEnabled(false);
                btn_test.setTextColor(Color.GRAY);
                break;
        }

    }
}
```

![1690556569760](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\1690556569760.png)

