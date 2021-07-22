__DAY2 数组、链表__
====
__1.【两两交换链表中的节点】
题目描述：给定一个链表，两两交换其中相邻的节点，并返回交换后的链表。
你不能只是单纯的改变节点内部的值，而是需要实际的进行节点交换。
 <br>__
```javascript
//JS版本
var swapPairs = function (head) {
    if (!head || !head.next) return head
    var one = head
    var two = one.next
    var three = two.next

    two.next = one
    one.next = swapPairs(three)

    return two
};
```


****

__2.【三数之和】
题目描述：给你一个包含 n 个整数的数组 nums，判断 nums 中是否存在三个元素 a，b，c ，使得 a + b + c = 0 ？请你找出所有和为 0 且不重复的三元组。
注意：答案中不可以包含重复的三元组。<br>__
```javascript
//JS版本
var threeSum = function(nums){
            let arr = [];
            nums.sort((a,b) => {
                return a - b;
            })
            for(let i = 0;i < nums.length;i++){
                if(i > 0 && nums[i] === nums[i - 1]) continue;
                let left = i + 1,right = nums.length - 1;
                let a = nums[i];
                while(left < right){
                    let b = nums[left];
                    let c = nums[right];
                    if(a + b + c === 0){
                        arr.push([a,b,c]);
                        //神来之笔，诸位道友有想过for循环怎么用嘛，哈哈哈
                        for(left++;left < right && nums[left] === nums[left - 1];left++);
                    }else if(a + b + c < 0){
                        left++;
                    }else{
                        right--;
                    }
                }
            }
            return arr;
        }
```
__题解：<br>
核心思想—双指针；当我们需要枚举数组中的两个元素时，如果我们发现随着第一个元素的递增，第二个元素是递减的，那么就可以使用双指针的方法，降低枚举的时间复杂度。在枚举的过程每一步中，左指针会向右移动一个位置，而右指针会向左移动若干个位置。
<br>__

****

