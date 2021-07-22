<<<<<<< HEAD
24.[两两交换链表中的节点](https://leetcode-cn.com/problems/swap-nodes-in-pairs/)

/*
 要么就递归要么就多指针
 多指针加一个哨兵指针
 
  */
时间复杂度O(n)
空间复杂度O(1)
```java
class Solution {
    public ListNode swapPairs(ListNode head) {
        if(head == null || head.next == null){
            return head;
        }
        ListNode phead = new ListNode();
        phead.next = head;
        ListNode temp = phead;
        //其实是三个指针的之间的移动
        while(temp.next != null && temp.next.next != null){
            ListNode cur = temp.next;
            ListNode next = temp.next.next;
            temp.next = next;
            cur.next = next.next;
            next.next = cur;
            temp = cur;
            
        }
        return phead.next;

    }
}
```
递归终止条件
中间过程就是模拟递归的结果是处理好的一个链
进行模拟
时间复杂度O(n)
空间复杂度O(n)栈的大小

```java
class Solution {
    public ListNode swapPairs(ListNode head) {
        if(head == null || head.next == null){
            return head;
        }
        ListNode cur = head.next;
        cur.next = swapPairs(cur.next);
        head.next = cur.next;
        cur.next = head;
        return cur;
    }
    
}
```
15.[三数之和](https://leetcode-cn.com/problems/3sum/)
dfs（回溯）超时剪枝困难存在问题
```java
class Solution {
    public List<List<Integer>> threeSum(int[] nums) {
         int l = nums.length;
         List<List<Integer>> res = new ArrayList<>();
         if(l < 3) {return res;}
         Arrays.sort(nums);
         List<Integer> temp = new ArrayList<>();
         dsp(nums,0,temp,res,0);
         return res;

    }
    //数组 开始的序号 层数  中间的temps 结果
    private void dsp(int[] nums,int start,List<Integer> temp, List<List<Integer>> res,int sum){
        if(temp.size() > 3){return;}
        if( temp.size() == 3 && sum ==0){
            res.add(new ArrayList<>(temp));
            return;
        }
        if( temp.size() == 3 && sum !=0) {
        	return;
        }
        for(int i = start;i < nums.length;i++){
           
            temp.add(nums[i]);
            sum = sum+nums[i];
            dsp(nums,start+1,temp,res,sum);
            temp.remove(temp.size()-1);
            sum = sum -nums[i];

        }
    }
}
```
双指针 具体就是排序以后获得的思路
```java
class Solution {
    public List<List<Integer>> threeSum(int[] nums) {
         int l = nums.length;
         List<List<Integer>> res = new ArrayList<>();
         if(l < 3) {return res;}
         Arrays.sort(nums);
         //本来是l-1考虑到right的原因，直接设置为l-2;考虑过不知道0的位置，所以需要除掉很多情况
         for(int i = 0;i < l-2;i++){
             if(nums[i] > 0){break;}
             if(i > 0 && nums[i] == nums[i-1]){continue;}//防止重复
             int target = -nums[i];
             int left = i+1;
             int right =l-1;
             while(left < right){
                 //只是一种情况而已，对应要在有限范围内移动指针
                if((nums[left] + nums[right]) == target){
                     List<Integer> temp = new ArrayList<>();
                    temp.add(-target);
                    temp.add(nums[left]);
                    temp.add(nums[right]);
                    res.add(temp);
                    //防止重复
                left++;
                right--;
                  while(left<right && nums[left] == nums[left-1]){
                    left++;
                 }
                   while(left<right && nums[right] == nums[right+1]){
                    right--;
                  }    
                }
                 
                else if((nums[left] + nums[right]) < target){
                    left++;
                }
                else{
                    right--;
                }
             }
        
         }
           return res;
    }
    
}
=======
24.[两两交换链表中的节点](https://leetcode-cn.com/problems/swap-nodes-in-pairs/)

/*
 要么就递归要么就多指针
 多指针加一个哨兵指针
 
  */
时间复杂度O(n)
空间复杂度O(1)
```java
class Solution {
    public ListNode swapPairs(ListNode head) {
        if(head == null || head.next == null){
            return head;
        }
        ListNode phead = new ListNode();
        phead.next = head;
        ListNode temp = phead;
        //其实是三个指针的之间的移动
        while(temp.next != null && temp.next.next != null){
            ListNode cur = temp.next;
            ListNode next = temp.next.next;
            temp.next = next;
            cur.next = next.next;
            next.next = cur;
            temp = cur;
            
        }
        return phead.next;

    }
}
```
递归终止条件
中间过程就是模拟递归的结果是处理好的一个链
进行模拟
时间复杂度O(n)
空间复杂度O(n)栈的大小

```java
class Solution {
    public ListNode swapPairs(ListNode head) {
        if(head == null || head.next == null){
            return head;
        }
        ListNode cur = head.next;
        cur.next = swapPairs(cur.next);
        head.next = cur.next;
        cur.next = head;
        return cur;
    }
    
}
```
15.[三数之和](https://leetcode-cn.com/problems/3sum/)
dfs（回溯）超时剪枝困难存在问题
```java
class Solution {
    public List<List<Integer>> threeSum(int[] nums) {
         int l = nums.length;
         List<List<Integer>> res = new ArrayList<>();
         if(l < 3) {return res;}
         Arrays.sort(nums);
         List<Integer> temp = new ArrayList<>();
         dsp(nums,0,temp,res,0);
         return res;

    }
    //数组 开始的序号 层数  中间的temps 结果
    private void dsp(int[] nums,int start,List<Integer> temp, List<List<Integer>> res,int sum){
        if(temp.size() > 3){return;}
        if( temp.size() == 3 && sum ==0){
            res.add(new ArrayList<>(temp));
            return;
        }
        if( temp.size() == 3 && sum !=0) {
        	return;
        }
        for(int i = start;i < nums.length;i++){
           
            temp.add(nums[i]);
            sum = sum+nums[i];
            dsp(nums,start+1,temp,res,sum);
            temp.remove(temp.size()-1);
            sum = sum -nums[i];

        }
    }
}
```
双指针 具体就是排序以后获得的思路
```java
class Solution {
    public List<List<Integer>> threeSum(int[] nums) {
         int l = nums.length;
         List<List<Integer>> res = new ArrayList<>();
         if(l < 3) {return res;}
         Arrays.sort(nums);
         //本来是l-1考虑到right的原因，直接设置为l-2;考虑过不知道0的位置，所以需要除掉很多情况
         for(int i = 0;i < l-2;i++){
             if(nums[i] > 0){break;}
             if(i > 0 && nums[i] == nums[i-1]){continue;}//防止重复
             int target = -nums[i];
             int left = i+1;
             int right =l-1;
             while(left < right){
                 //只是一种情况而已，对应要在有限范围内移动指针
                if((nums[left] + nums[right]) == target){
                     List<Integer> temp = new ArrayList<>();
                    temp.add(-target);
                    temp.add(nums[left]);
                    temp.add(nums[right]);
                    res.add(temp);
                    //防止重复
                left++;
                right--;
                  while(left<right && nums[left] == nums[left-1]){
                    left++;
                 }
                   while(left<right && nums[right] == nums[right+1]){
                    right--;
                  }    
                }
                 
                else if((nums[left] + nums[right]) < target){
                    left++;
                }
                else{
                    right--;
                }
             }
        
         }
           return res;
    }
    
}
>>>>>>> aea41fa4ac160a271bc1583a07778e883208e170
```