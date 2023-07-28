android studio控件14

lmagView图片显示

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <ImageView
        android:id="@+id/iv_scale"
        android:layout_width="match_parent"
        android:layout_height="220dp"
        android:layout_marginTop="5dp"
        android:src="@drawable/t01"/>

</LinearLayout>
```

```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.ImageView;

public class lmageScaleActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_lmage_scale);
        ImageView iv_scale= findViewById(R.id.iv_scale);
        iv_scale.setImageResource(R.drawable.t01);
    }
}
```

```
在Android Studio中，你可以按照以下步骤将图片导入到drawable文件夹中：

在Project视图中，找到你的项目，展开app文件夹。
在app文件夹中，找到res文件夹并展开它。
在res文件夹中，找到drawable文件夹并展开它。
右键点击drawable文件夹，选择"Show in Explorer"（在Windows上）或"Reveal in Finder"（在Mac上）。
这将打开drawable文件夹所在的文件夹。在这个文件夹中，你可以将你的图片文件（如.png、.jpg等）复制或拖放到drawable文件夹中。
返回到Android Studio，你应该能够在drawable文件夹中看到你刚刚导入的图片文件。
一旦你将图片导入到drawable文件夹中，你就可以在布局文件或代码中使用这些图片资源。例如，在布局文件中使用图片资源可以通过以下方式：

<ImageView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:src="@drawable/your_image_file_name" />
其中，"your_image_file_name"是你导入的图片文件的名称（不包括文件扩展名）。

希望这能帮助到你在Android Studio中导入图片到drawable文件夹中。


```

![1690560257351](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\1690560257351.png)