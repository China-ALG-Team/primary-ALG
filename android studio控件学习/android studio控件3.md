android studio控件3

设置文本颜色：在线性布局中<LinearLayout  xmlns:android="http://schemas.android.com/apk/res/android"                                                 

​                          然后设置基础版面根节点android:layout_width="match_parent"(对宽的设置"填充父容器")

​                                                                  android:layout_height="match_parent"(对高的设置"填充父容器") 

​                                                                  android:orientation="vertical/horizontal">  (设置文本叠加方向v从上往下h从左往右)                      

​                        <TextView( 在TextView中设置文本内容、字体、颜色等属性）

​                                                       android:layout_width="wrap_content"(对宽的设置"包裹内容"）

​                                                       android:layout_height="wrap_content"(对高的设置"包裹内容")

​                                                        android:text="俆hello world"（用text设置文本内容）

​                                                         android:textSize="50dp/sp/px"(用textSize设置文本大小单位3个dp/sp/px)

​                                                        android:textColor="@color/green(#00ff00)"(用textColor设置文本颜色)

​                                                       android:background="#ff00ff00"(用background设置文本背景颜色)

​                                                       android:layout_margin="10dp"(用margin设置文本的外间距)/>

​                                             </LinearLayout>

![1689599804685](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689599804685.png)