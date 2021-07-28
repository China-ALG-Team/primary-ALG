1047.[删除字符中的所有的相邻重复项](https://leetcode-cn.com/problems/remove-all-adjacent-duplicates-in-string/)
时间复杂度O(N):遍历s的长度
空间复杂度O(N):转化成了schar
```java
class Solution {
    /**
    注意循环比较
     */
    public String removeDuplicates(String s) {
        int length = s.length();
        //不用开辟多个空间，直接原地改就行
        int peek = -1;
        char[] schar = s.toCharArray();
        for(int i = 0;i < length;i++){
            if(peek >= 0){
                if(schar[peek] == schar[i]){
                    peek--;
                }else{
                    peek++;
                    schar[peek] = schar[i];
                }
            } else{
                peek++;
                schar[peek] = schar[i];

            }
        }
        //第一个0是初始值的位置，第二个参数不是末尾值，而是长度
        return String.copyValueOf(schar,0,peek+1);
    }
}
```
1021.[删除最外层的括号](https://leetcode-cn.com/problems/remove-outermost-parentheses/submissions/)
时间复杂度O（n）
空间复杂度O（n）
```java
class Solution {
    /**
    读了两遍发现这该死的题目好像原语只有最外层的括号
    1.可以用栈把说有的原语处理出来
    2.一定合法所以直接count
    
     */

    public String removeOuterParentheses(String s) {
        //就要删除最外层的括号O(n)
        char[] ch =s.toCharArray();
        StringBuilder res = new StringBuilder();
        //等于0所以就是最外层不能加进来
        int leftcount = 0;
        for(int i = 0;i < s.length();i++){
            //注意主要就是第一个不能进还有就是只要读到就要+++
            if(ch[i] == '(' && leftcount++ > 0){
                res.append('(');
            }
             //注意知道读到就要减，一定要先减再比较因为可以自己想一下就是（（））的时候leftcount会多读一个)
            if( ch[i] ==')' && --leftcount > 0){
          
                res.append(')');
            }
        }
        return res.toString();

    }
}
```