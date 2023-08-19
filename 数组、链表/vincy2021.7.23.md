242.[有效的字母异位词](https://leetcode-cn.com/problems/valid-anagram/comments/)
考虑是否能O(n)解决问题
##1.首先考虑能不能排序
时间复杂度就是排序O(nlogn)
空间复杂度O(n)
空间复杂度：排序需要O(logn)的空间复杂度，但是java 需要拷贝字符串所以空间复制度是O(n)

这依赖于语言的细节；
这取决于函数的设计方式，例如，可以将函数参数类型更改为 char[]

```java
class Solution {
    /*
    考虑遍历一下是否能得到结果
     */
    public boolean isAnagram(String s, String t) {
        if(s.length() != t.length()){return false;}
        char[] Schar = s.toCharArray();
        char[] Tchar = t.toCharArray();
        Arrays.sort(Schar);
        Arrays.sort(Tchar);
        return Arrays.equals(Schar,Tchar);
    }
}
```
##2.再考虑hashmap(对于unicode就不能用int[26]来维护)


49.[字母异位词分组](https://leetcode-cn.com/problems/group-anagrams/submissions/)
```java

class Solution {
    public List<List<String>> groupAnagrams(String[] strs) {
        //最后输出的集合格式[[],[],[]]
        List<List<String>> list = new ArrayList<>();
        //利用哈希表 key为排序
        HashMap<String,List<String>> map = new HashMap<>();
        for(String str: strs){
            char[] chars = str.toCharArray();
            Arrays.sort(chars);
            //利用Arrays
            String s = Arrays.toString(chars);
            if(map.containsKey(s)){
                List<String> stringList = map.get(s);
                stringList.add(str);
                map.put(s,stringList);
            }
            else{
                map.put(s,new ArrayList<String>(Arrays.asList(str)));
            }
        }
        for(Map.Entry<String,List<String>> entry :map.entrySet()){
            List<String> value = entry.getValue();
            list.add(value);
        }
        return list;
    }
}

```