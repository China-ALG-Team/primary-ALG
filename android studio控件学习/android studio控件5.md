android studio控件5

设置视图对齐方式：在线性布局中<LinearLayout  xmlns:android="http://schemas.android.com/apk/res/android"                                                 

​                          然后设置基础版面根节点android:layout_width="match_parent"(对宽的设置"填充父容器")

​                                                                  android:layout_height="400dp"(对高的设置"填充父容器") 

​                                                                 android:background="#f0ff"(父容器背景)

​                                                                  android:orientation="vertical/horizontal">  (设置文本叠加方向v从上往下h从左往右)                                                             android:padding="10dp"(约束内布局)

​                                                                                      

​                                     <LinearLayout    android:layout_width="200dp"  

​                                                                android:layout_height="200dp" (设置父内容器)

​                                                                 android:layout_margin="10dp" (设置父内容器与父容器的边距)

​                                                                  android:background="#00ff00"(设置子容器背景)

​                                                                 android:layout_gravity="bottom"(此布局对于外布局向下靠)

​                                                                  android:gravity="right">(此布局约束内部靠右)

​                                       <View        

​                                                                android:layout_width="match_parent"        

​                                                                android:layout_height="match_parent"       

​                                                                 android:background="#0f00ff"

​                                                                 android:layout_margin="22dp"/>(距离约束)

</LinearLayout>

<LinearLayout    

​                                                             android:layout_width="200dp" 

​                                                              android:layout_height="200dp"   

​                                                                android:background="#ff00ff"   

​                                                                 android:layout_margin="10dp"  (远离距离约束)

​                                                              android:layout_gravity="top"   (此布局对外部靠上)

​                                                               android:gravity="left">   (此布局约束内部靠右)

 <TextView        

​                                                              android:layout_width="100dp"      

​                                                               android:layout_height="100dp"      

​                                                               android:background="#f000"        

​                                                                android:layout_margin="23dp"/>(离外部)

</LinearLayout>

</LinearLayout>

知

```
layout_gravity属性：

top：将视图与父容器的顶部对齐。
bottom：将视图与父容器的底部对齐。
left：将视图与父容器的左边对齐。
right：将视图与父容器的右边对齐。
center_vertical：将视图在垂直方向上居中对齐。
center_horizontal：将视图在水平方向上居中对齐。
center：将视图在水平和垂直方向上都居中对齐。
start：将视图与父容器的起始位置对齐（在LTR布局中为左边，在RTL布局中为右边）。
end：将视图与父容器的结束位置对齐（在LTR布局中为右边，在RTL布局中为左边）。
gravity属性：

top：将视图内部内容在垂直方向上顶部对齐。
bottom：将视图内部内容在垂直方向上底部对齐。
left：将视图内部内容在水平方向上左边对齐。
right：将视图内部内容在水平方向上右边对齐。
center_vertical：将视图内部内容在垂直方向上居中对齐。
center_horizontal：将视图内部内容在水平方向上居中对齐。
center：将视图内部内容在水平和垂直方向上都居中对齐。
start：将视图内部内容在水平方向上起始位置对齐（在LTR布局中为左边，在RTL布局中为右边）。
end：将视图内部内容在水平方向上结束位置对齐（在LTR布局中为右边，在RTL布局中为左边）。
```

![1689604705500](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689604705500.png)