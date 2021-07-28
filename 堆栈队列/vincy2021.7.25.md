##84.[柱状图中最大的矩形](https://leetcode-cn.com/problems/largest-rectangle-in-histogram/?utm_source=LCUS&utm_medium=ip_redirect&utm_campaign=transfer2china)

####暴力法(超时了)
思想就是遍历一遍，对于每一个柱子找到他周围能组成的最大矩形（嵌套了两个
时间复杂度O(N*N):最差的情况就是全部相等，每一个都遍历N次
空间复杂度O(1):只开辟了了3个新变量
```java
class Solution {
    //每加进来一个就判断一次
    public int largestRectangleArea(int[] heights) {
        //循环遍历一次找到宽度
        int area = heights[0];

        
        for(int i = 0;i < heights.length;i++){
              int left = i;
              int right = i;
              while(left > 0 && heights[left-1] >= heights[i]){
                left--;
              }
              while(right <heights.length-1 && heights[right+1] >= heights[i]){
                  right++;
              }
              area = Math.max(area,(right-left+1)*heights[i]);
        }
        return area;
    }
}
```
####单调栈的方法
注意的特点就是加入哨兵节点进行简化
（我们做普通单调栈的时候第一次遍历会有栈不为空的情况因为遇到严格单调小的才能加进来所以我们在完成for以后还需要while并且只剩一个的时候要多些一个if（因为最后一个未出栈的元素的len计算不一样,它的len就是数组的长度因为没有peek可以给他参考，并且他是最矮的）
所以
* 左边加一个元素就可以有最小的peek进行计算
* 右边加一个就可以不用加一个while（）进行判断

时间复杂度O(n)：外层的for循环的时间复杂度，然后里面的while的次数是pop的pop一定小于push，push就算全部进栈也只是循环了length次，因为while的次数是每次递增的，前n次都是小于length的所以永远是常数级别
空间复杂度O(N):新数组
```java

class Solution {
    //这里可以简化一个单调递增栈
    //1213 对于栈我们保证栈里面都是比未进栈的大，那么左边的边界就知道到，当遇到一个小的我们就里面弹出，那么右边边界我们也知道了，时间复杂度就只是遍历一遍
    public int largestRectangleArea(int[] heights) {
        
        int n = heights.length;
        if(n == 0){return 0;}
        if(n == 1){return heights[0];}
        int area = 0;
        Deque<Integer> stack = new ArrayDeque<>();
        int[] newHeights = new int [n+2];
        newHeights[0] = 0;
        newHeights[n+1] = 0;
        //加两个哨兵节点
        for(int i = 0;i < n;i++){
            newHeights[i+1] = heights[i];
        }
        //栈里面存的是下标左右都是严格小的不能算所以-1
        for(int i = 0;i < n+2;i++){
            while(!stack.isEmpty() && newHeights[i]< newHeights[stack.peek()]){
                int h = newHeights[stack.pop()];
                area = Math.max(area,(i - stack.peek()-1)*h);
            }
            stack.push(i);
        }
        return area;
    }    
}
```


## 42.[接雨水](https://leetcode-cn.com/problems/trapping-rain-water/?utm_source=LCUS&utm_medium=ip_redirect&utm_campaign=transfer2china)
时间复杂度O(n):除了最外层里面的循环都是常数级别的
空间复杂度O(n):就是栈的大小，最坏就是O(n)

```java
class Solution {
    //单调栈，这里是单调递减栈
    public int trap(int[] height) {
        int n = height.length;
        if(n == 0){return 0;}
        int res = 0;
        Deque<Integer> Stack = new ArrayDeque<>();
        for(int i = 0;i < n;i++){
            //遇到第一个比自己大的时候3212
            while(!Stack.isEmpty() && height[i] > height[Stack.peek()] ){
                int cur = Stack.pop();
                //去重
                while (!Stack.isEmpty() && height[Stack.peek()] == height[cur]) {
                    Stack.pop();
                }
                //3 1 2 主要注意一下就是每个pop进来一个只然后就计算一次雨水的大小
               if(!Stack.isEmpty() ){
                    int stackTop = Stack.peek();
                    res +=(Math.min(height[stackTop],height[i]) - height[cur])*(i - stackTop -1);
                }
    
            }
            Stack.push(i);
        }
        return res;
    }
}
``