android studio控件4

设置视图间距：在线性布局中<LinearLayout  xmlns:android="http://schemas.android.com/apk/res/android"                                                 

​                          然后设置基础版面根节点android:layout_width="match_parent"(对宽的设置"填充父容器")

​                                                                  android:layout_height="300dp"(对高的设置"填充父容器") 

​                                                                 android:background="#00AAFF"(父容器背景)

​                                                                  android:orientation="vertical/horizontal">  (设置文本叠加方向v从上往下h从左往右)                      

​                                     <LinearLayout    android:layout_width="match_parent"  

​                                                                android:layout_height="match_parent" (设置父内容器)

​                                                                 android:layout_margin="20dp" (设置父内容器与父容器的边距)

​                                                                  android:background="#00ff00"(设置子容器背景)

​                                                                 android:padding="60dp">  (设置子容器与内容边距束缚)

​                                       <View        

​                                                                android:layout_width="match_parent"        

​                                                                android:layout_height="match_parent"       

​                                                                 android:background="#0f00ff"/>

</LinearLayout>

</LinearLayout>           知( android:layout_marginTop="10dp"   上

​                                                  android:layout_marginBottom="20dp"    下

​                                                    android:layout_marginLeft="30dp"    左

​                                                     android:layout_marginRight="40dp" 右)

![1689601434457](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689601434457.png)

​     