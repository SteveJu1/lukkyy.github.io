#### [3. 无重复字符的最长子串](https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/)



给定一个字符串，请你找出其中不含有重复字符的 **最长子串** 的长度,

```
输入: "abcabcbb"
输出: 3 
解释: 因为无重复字符的最长子串是 "abc"，所以其长度为 3
```



1.从左到右遍历子串

滑动窗口来规定最长的子串， 

滑动窗口要用左右两指针L,R表示窗口内的子串，若无重复，L向右移动，

2. 滑动窗口内用哈希表来计数（key是值，value是索引)， 

