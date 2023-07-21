android studio控件6

设置视图<LinearLayout：在线性布局中<LinearLayout  xmlns:android="http://schemas.android.com/apk/res/android"                                                 

​                          然后设置基础版面根节点android:layout_width="match_parent"(对宽的设置"填充父容器")

​                                                                  android:layout_height="400dp"(对高的设置"填充父容器") 

​                                                                 android:background="#f0ff"(父容器背景)

​                                                                  android:orientation="vertical/horizontal">  (设置文本叠加方向v从上往下h从左往右)                                                             android:padding="10dp"(约束内布局)

​                                                                                      

​                                    <LinearLayout    (1   底板)

​                                                               android:layout_width="match_parent"   

​                                                                 android:layout_height="wrap_content"

​                                                               android:orientation="horizontal" (设置从左到右)

​                                                               android:background="@color/black"   

​                                                            android:layout_margin="20dp"   (远离外部)

​                                                             android:padding="30dp">   (约束内部)

​                                           <TextView        (1,1模板)

​                                                            android:layout_width="wrap_content"     

​                                                           android:layout_height="wrap_content"      

​                                                            android:text="第一行第一个"    

​                                                             android:textColor="@color/white"     

​                                                                  android:textSize="20dp"       

​                                                            android:layout_weight="1">  (占比) 

​                                          </TextView>    

​                                      <TextView    (1，2)   

​                                                              android:layout_width="wrap_content"     

​                                                              android:layout_height="wrap_content"    

​                                                              android:text="第一行第二个"     

​                                                             android:textSize="20dp"     

​                                                              android:textColor="@color/white"     

​                                                               android:layout_weight="1">   (占比)

​                                         </TextView>

​                        </LinearLayout>（底板2)

​                            <LinearLayout    

​                                                              android:layout_width="match_parent"  

​                                                             android:layout_height="wrap_content"  

​                                                            android:orientation="vertical"  

​                                                           android:background="#00ffff"  

​                                                           android:padding="20dp">   (约束内部)

​                                     <TextView       

​                                                             android:layout_width="wrap_content"     

​                                                           android:layout_height="wrap_content"      

​                                                            android:text="第二行第一个"      

​                                                           android:textSize="30dp"    

​                                                            android:background="#00ff00"     

​                                                              android:layout_margin="10dp"   

​                                                            android:layout_weight="2">  

​                                    </TextView>   

​                                     <TextView      

​                                                              android:layout_width="wrap_content"    

​                                                             android:layout_height="wrap_content"   

​                                                              android:text="第三行第一个"     

​                                                              android:layout_margin="10dp"  

​                                                               android:textSize="30dp"    

​                                                             android:background="#ffffff"       

​                                                                android:layout_weight="2">    

</TextView>

</LinearLayout>

</LinearLayout>

![1689664635062](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689664635062.png)