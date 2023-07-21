android studio控件7

![1689770701003](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689770701003.png)

设置视图<RelativeLayout：在相对布局中<RelativeLayout  xmlns:android="http://schemas.android.com/apk/res/android"                                                 

​                          然后设置基础版面根节点android:layout_width="match_parent"(对宽的设置"填充父容器")

​                                                                  android:layout_height="150dp"(对高的设置"填充父容器") 

​                                       <TextView        android:id="@+id/tv_center"    

​                                                               android:layout_width="wrap_content"       

​                                                                 android:layout_height="wrap_content"      

​                                                                  android:text="中心"     

​                                                                   android:textSize="20dp"     

​                                                                   android:textColor="@color/black"       

​                                                               android:background="@color/white"     

​                                                                    android:layout_centerInParent="true"/>                                                            

​                                        <TextView        

android:id="@+id/tv_center_horizontal"     

   android:layout_width="wrap_content"       

 android:layout_height="wrap_content"   

  android:text="水平中间"        

android:textSize="20dp"        

android:textColor="@color/black"        

android:background="@color/white"        

android:layout_centerHorizontal="true"/>   

​                                        <TextView        

android:id="@+id/tv_center_vertical"        

android:layout_width="wrap_content"        

android:layout_height="wrap_content"        

android:text="垂直中间"       

 android:textSize="20dp"        

android:textColor="@color/black"        

android:background="@color/white"       

 android:layout_centerVertical="true"/>     

​                                       <TextView        

android:id="@+id/tv_center_left"       

 android:layout_width="wrap_content"       

 android:layout_height="wrap_content"       

 android:text="我跟上级左边对其"        

android:textSize="20dp"        

android:textColor="@color/black"        

android:background="@color/white"        

android:layout_alignParentLeft="true"/>    

​                                       <TextView        

android:id="@+id/tv_center_right"        

android:layout_width="wrap_content"        

android:layout_height="wrap_content"        

android:text="我跟上级右边对齐"        

android:textSize="20dp"        

android:textColor="@color/black"        

android:background="@color/white"        

android:layout_alignParentRight="true"/>    

​                                        <TextView        

android:id="@+id/tv_center_top"        

android:layout_width="wrap_content"        

android:layout_height="wrap_content"        

android:text="我跟上级顶部对齐"        

android:textSize="20dp"       

 android:textColor="@color/black"        

android:background="@color/white"        

android:layout_alignParentTop="true"/>    

​                                         <TextView        

android:id="@+id/tv_center_bottom"       

 android:layout_width="wrap_content"        

android:layout_height="wrap_content"        

android:text="我跟上级的底部对齐"       

 android:textSize="20dp"        

android:textColor="@color/black"        

android:background="@color/white"       

 android:layout_alignParentBottom="true"/>    

​                                            <TextView    

android:id="@+id/tv_left_center"    

android:layout_width="wrap_content"    

android:layout_height="wrap_content"    

android:text="我在中间右边"    

android:textSize="20dp"    

android:textColor="@color/black"    

android:background="@color/white"    

android:layout_toLeftOf="@id/tv_center"   

 android:layout_alignTop="@id/tv_center"/>   

​                                                 <TextView       

 android:id="@+id/tv_right_center"       

 android:layout_width="wrap_content"        

android:layout_height="wrap_content"        

android:text="我在中间右边"        

android:textSize="20dp"       

 android:textColor="@color/black"        

android:background="@color/white"        

android:layout_toRightOf="@id/tv_center"        

android:layout_alignBottom="@id/tv_center"/>    

​                                               <TextView        

android:id="@+id/tv_above_center"        

android:layout_width="wrap_content"        

android:layout_height="wrap_content"        

android:text="我在中间上面"        

android:textSize="20dp"       

 android:textColor="@color/black"        

android:background="@color/white"        

android:layout_alignRight="@id/tv_center"       

 android:layout_above="@id/tv_center"/>  

​                                                 <TextView        

android:id="@+id/tv_below_center"        

android:layout_width="wrap_content"        

android:layout_height="wrap_content"        

android:text="我在中间下面"        

android:textSize="20dp"        

android:textColor="@color/black"        

android:background="@color/white"        

android:layout_alignRight="@id/tv_center"        

android:layout_below="@id/tv_center"/>



</RelativeLayout>

![1689772977411](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689772977411.png)

![1689773114411](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689773114411.png)



​                                                                 

​                                                                                                                               