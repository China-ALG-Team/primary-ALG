android studio控件8

设置视图<GridLayout：在线性布局中<GridLayout  xmlns:android="http://schemas.android.com/apk/res/android"                                                 

​                          然后设置基础版面根节点android:layout_width="match_parent"(对宽的设置"填充父容器")

​                                                                  android:layout_height="match_parent"

​                                                                    android:columnCount="2"(指定了网格的列数，有几列每行放几个)

​                                                                    android:rowCount="2">(指定了网格的行数，有几行每列放几个)

​                                             <TextView        

android:layout_width="0dp"        

android:layout_height="60dp"        

android:layout_columnWeight="1" (占比)       

android:background="#ffcccc"        

android:text="浅红色"       

 android:textColor="#000000"        

android:textSize="17dp"        

android:gravity="center"/>    (<TextView 内容居中处理)

​                                              <TextView        

android:layout_width="0dp"        

android:layout_height="60dp"        

android:layout_columnWeight="1"        

android:background="#ffaa00"        

android:text="橙色"        

android:textColor="#000000"        

android:textSize="17dp"        

android:gravity="center"/>    

​                                                <TextView        

android:layout_width="0dp"        

android:layout_height="60dp"        

android:background="#00ff00"        

android:text="绿色"        

android:textColor="#000000"        

android:textSize="17dp"        

android:gravity="center"        

android:layout_columnWeight="1"/>    

​                                                  <TextView        

android:layout_width="0dp"        

android:layout_height="60dp"        

android:background="#660066"        

android:text="深紫色"        

android:textColor="#000000"        

android:textSize="17dp"        

android:gravity="center"        

android:layout_columnWeight="1"/>

</GridLayout>

![1689774352803](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689774352803.png)

![1689774331651](C:\Users\徐元孜H\AppData\Roaming\Typora\typora-user-images\1689774331651.png)