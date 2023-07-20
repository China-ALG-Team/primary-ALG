android studio控件9

设置视图<ScrollView：在线性布局中创建滚动视图<LinearLayout  xmlns:android="http://schemas.android.com/apk/res/android"                                                 

​                          然后设置基础版面根节点android:layout_width="match_parent"(对宽的设置"填充父容器")

​                                                                  android:layout_height="match_parent"               

​                                                                 android:orientation="vertical">    

​                        <HorizontalScrollView  (左右平移滚动视图)      

android:layout_width="wrap_content"        

android:layout_height="200dp">        

​                            <LinearLayout     (在左右平移滚动视图中创建线性布局用来填满)       

android:layout_width="wrap_content"            

android:layout_height="match_parent"            

android:orientation="horizontal">   (左右滚动所以内容用horizontal)         

​                              <TextView         (用TextView作为内容体现滚动效果)       

android:layout_width="300dp"         (宽可以设的长一点)       

android:layout_height="match_parent"                

android:background="#aaffff" />            

​                                 <TextView                

android:layout_width="300dp"                

android:layout_height="match_parent"                

android:background="#ffff00"/>        

​                                 </LinearLayout>   (线性布局结束) 

​                                 </HorizontalScrollView>    (滚动视图结束)

​                                 <ScrollView     (垂直滚动视图)   

android:layout_width="match_parent"        

android:layout_height="wrap_content">       

​                                   <LinearLayout      (用线性布局体现)      

android:layout_width="match_parent"            

android:layout_height="wrap_content"            

android:orientation="vertical">     (垂直排列效果)       

​                                  <TextView                

android:layout_width="match_parent"                

android:layout_height="400dp"                

android:background="#00ff00" />            

​                                  <TextView                

android:layout_width="match_parent"                

android:layout_height="400dp"                

android:background="#ffffaa"/>        

​                                </LinearLayout>    (线性布局结束)

​                                 </ScrollView>(垂直滚动视图结束)

​                                </LinearLayout>(线性布局结束)

![1689815986206](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689815986206.png)

![1689816494964](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689816494964.png)