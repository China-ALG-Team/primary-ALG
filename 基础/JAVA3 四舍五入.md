#  [ **JAVA3** **四舍五入** ](https://www.nowcoder.com/practice/cae89de6292b4084acb93659353260e0?tpId=220&tags=&title=&difficulty=0&judgeStatus=0&rp=0&sourceUrl=%2Fexam%2Foj%3Fpage%3D1%26tab%3D%25E8%25AF%25AD%25E6%25B3%2595%25E7%25AF%2587%26topicId%3D220)

##### 描述：定义一个int类型变量i,i为由浮点数变量d四舍五入后的整数类型，请将转换后的i进行输出

##### 输入描述：用户随机输入的浮点数

##### 输出描述：四舍五入之后的整数（小数点后一位>=5则进一，否则舍去）

```Java
import java.util.Scanner;
public class 牛客练习3 {//需求四舍五入
    public static void main(String []args){
        Scanner sc=new Scanner(System.in);
        double i=sc.nextDouble();
       //double c=sc.nextDouble();
        int a=(int)i;
        int w=(int)i;
        if((i-a)>=0.5){
            w=(int)i+1;
        }
System.out.println(w);
       // System.out.println(Math.round(c));


    }
}

```

