import java.util.Scanner;

/

描述

设计一个方法，将一个小于2147483647的double类型变量以截断取整方式转化为int类型



输入描述：

随机double类型变量

输出描述：

转化后的int类型变量

 */*

public class sjzh {



    public static void main(String[]args){

        System.out.println("请输入一个浮点数");

        Scanner sc=new Scanner(System.in);

        double i=sc.nextDouble();

        zhuanghuan(i);



    }

    public static void zhuanghuan(double i){

        int s=(int)i;

        System.out.println(s);

    }



}

