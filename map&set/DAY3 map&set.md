__DAY3 map&set__
====
__1.【有效的字母异位词】
给定两个字符串s和t，编写一个函数来判断t是否是s的字母异位词。
注意：若s和t中每个字符出现的次数都相同，则称s和t互为字母异位词。
 <br>__
```javascript
//JS版本
var isAnagram = function(s, t) {
    if (s.length !== t.length) {
        return false;
    }
    const table = new Array(26).fill(0);
    for (let i = 0; i < s.length; ++i) {
        table[s.codePointAt(i) - 'a'.codePointAt(0)]++;
    }
    for (let i = 0; i < t.length; ++i) {
        table[t.codePointAt(i) - 'a'.codePointAt(0)]--;
        if (table[t.codePointAt(i) - 'a'.codePointAt(0)] < 0) {
            return false;
        }
    }
    return true;
};
```
题解：有两种方法——一是给s、t先排序，然后比较是否相等即可；二是利用哈希值，先遍历s中的所有字母，给相应哈希值个数加一，后遍历t，对相应哈希值减一，最后若存在哈希值不为0，则s t不是有效的字母异位词。

****

__2.【字母异位词分组】
题目描述：给定一个字符串数组，将字母异位词组合在一起。可以按任意顺序返回结果列表。<br>__
```javascript
//JS版本
var groupAnagrams = function(strs) {
    const map = new Map();
    for (let str of strs) {
        let array = Array.from(str);
        array.sort();
        let key = array.toString();
        let list = map.get(key) ? map.get(key) : new Array();
        list.push(str);
        map.set(key, list);
    }
    return Array.from(map.values());
};

```
__题解：<br>
利用hash的思想,将每个子串使用质数乘法进行hash, 只要两个字符串包含的字符与对应数量一致,hash结果则一致： 例如: 'abc' = 2*3*4 'acb' = 2*4*3 然后通过哈希表Map将我们的答案保存。 复杂度分析： 时间复杂度O(mn) m为字符串平均长度,n为strs.length 空间复杂度O(mn) 因为需要将结果保存到map中。
<br>__

****

