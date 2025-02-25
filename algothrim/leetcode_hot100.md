# LeetCode Hot 100

Java Version

# 目录
1. [Base Knowledge](#base-knowledge)
    1. [List](#list)
    2. [Set](#set)
    3. [Map](#map)
    4. [Stack](#stack)
    5. [Queue](#queue)
2. [数组对象与 Java 集合的互相转换](#数组对象与-java-集合的互相转换)
    1. [字符串转字符数组](#字符串转字符数组)
    2. [字符串转字符串数组（按特定分隔符分割）](#字符串转字符串数组按特定分隔符分割)
    3. [数组转列表](#数组转列表)
        1. [基本数据类型数组转列表](#基本数据类型数组转列表)
        2. [对象数组转列表](#对象数组转列表)
    4. [列表转数组](#列表转数组)
        1. [列表转对象数组](#列表转对象数组)
    5. [列表切片得到子列表](#列表切片得到子列表)
    6. [集合转数组](#集合转数组)
    7. [数组转集合（除了使用 `Arrays.asList()`）](#数组转集合除了使用-arraysaslist)
    8. [注意事项](#注意事项)
3. [哈希](#哈希)
    1. [两数之和](#两数之和)
    2. [字母异位词分组](#字母异位词分组)
    3. [最长连续序列](#最长连续序列)
4. [双指针](#双指针)
    1. [双指针模板](#双指针模板)
    2. [移动零](#移动零)
5. [滑动窗口](#滑动窗口)
    1. [无重复字符的最长子串](#无重复字符的最长子串)
6. [子串](#子串)
7. [普通数组](#普通数组)
8. [矩阵](#矩阵)
9. [链表](#链表)
    1. [相交链表](#相交链表)
10. [二叉树](#二叉树)
    1. [二叉树的中序遍历](#二叉树的中序遍历)
    2. [二叉树的最大深度](#二叉树的最大深度)
    3. [翻转二叉树](#翻转二叉树)
11. [图论](#图论)
12. [回溯](#回溯)
13. [二分查找](#二分查找)
14. [栈](#栈)
15. [堆](#堆)
16. [贪心](#贪心)
17. [动态规划](#动态规划)
18. [多维动态规划](#多维动态规划)
19. [技巧](#技巧) 

## Base Knowledge

### 1. `List`
`List` 是一个有序的集合，允许存储重复元素。常见的实现类有 `ArrayList`、`LinkedList` 等。

#### 基本操作方法
- **添加元素**
    - `add(E element)`：在列表末尾添加指定元素。
    - `add(int index, E element)`：在指定索引位置插入指定元素。
- **访问元素**
    - `get(int index)`：返回列表中指定索引位置的元素。
- **修改元素**
    - `set(int index, E element)`：用指定元素替换列表中指定索引位置的元素。
- **删除元素**
    - `remove(int index)`：移除列表中指定索引位置的元素。
    - `remove(Object o)`：移除列表中首次出现的指定元素。
- **获取列表大小**
    - `size()`：返回列表中的元素个数。
- **检查元素是否存在**
    - `contains(Object o)`：判断列表中是否包含指定元素。
- **清空列表**
    - `clear()`：移除列表中的所有元素。

### 2. `Set`
`Set` 是一个不允许存储重复元素的集合。常见的实现类有 `HashSet`、`TreeSet` 等。

#### 基本操作方法
- **添加元素**
    - `add(E element)`：如果集合中尚未包含该元素，则添加该元素。
- **删除元素**
    - `remove(Object o)`：如果集合中包含指定元素，则移除该元素。
- **获取集合大小**
    - `size()`：返回集合中的元素个数。
- **检查元素是否存在**
    - `contains(Object o)`：判断集合中是否包含指定元素。
- **清空集合**
    - `clear()`：移除集合中的所有元素。

### 3. `Map`
`Map` 是一种键值对的集合，键是唯一的。常见的实现类有 `HashMap`、`TreeMap` 等。

#### 基本操作方法
- **添加键值对**
    - `put(K key, V value)`：将指定的键值对插入到映射中。如果键已存在，则替换其对应的值。
- **获取值**
    - `get(Object key)`：返回指定键所映射的值，如果映射中不包含该键，则返回 `null`。
- **删除键值对**
    - `remove(Object key)`：如果映射中存在该键，则移除该键值对。
- **获取映射大小**
    - `size()`：返回映射中的键值对数量。
- **检查键是否存在**
    - `containsKey(Object key)`：判断映射中是否包含指定的键。
- **检查值是否存在**
    - `containsValue(Object value)`：判断映射中是否包含指定的值。
- **清空映射**
    - `clear()`：移除映射中的所有键值对。

### 4. `Stack`
`Stack` 是一种后进先出（LIFO）的数据结构。在 Java 中，`Stack` 类继承自 `Vector`。

#### 基本操作方法
- **入栈**
    - `push(E item)`：将元素压入栈顶。
- **出栈**
    - `pop()`：移除并返回栈顶元素。如果栈为空，则抛出 `EmptyStackException` 异常。
- **查看栈顶元素**
    - `peek()`：返回栈顶元素，但不移除。如果栈为空，则抛出 `EmptyStackException` 异常。
- **检查栈是否为空**
    - `empty()`：判断栈是否为空。
- **查找元素位置**
    - `search(Object o)`：返回对象在栈中的位置，栈顶元素的位置为 1。如果对象不在栈中，则返回 -1。

### 5. `Queue`
`Queue` 是一种先进先出（FIFO）的数据结构。常见的实现类有 `LinkedList`、`PriorityQueue` 等。

#### 基本操作方法
- **添加元素**
    - `add(E element)`：将指定元素插入队列尾部。如果队列已满，会抛出异常。
    - `offer(E element)`：将指定元素插入队列尾部。如果队列已满，会返回 `false`。
- **移除元素**
    - `remove()`：移除并返回队列头部元素。如果队列为空，会抛出异常。
    - `poll()`：移除并返回队列头部元素。如果队列为空，会返回 `null`。
- **查看队列头部元素**
    - `element()`：返回队列头部元素，但不移除。如果队列为空，会抛出异常。
    - `peek()`：返回队列头部元素，但不移除。如果队列为空，会返回 `null`。
- **检查队列是否为空**
    - `isEmpty()`：判断队列是否为空。
- **获取队列大小**
    - `size()`：返回队列中的元素个数。

## Part 2

以下是关于数组对象与 Java 集合进行互相转换的详细笔记：

### 1. 字符串转字符数组
在 Java 中，`String` 类提供了 `toCharArray()` 方法，可以方便地将字符串转换为字符数组。

```java
String str = "Hello";
char[] charArray = str.toCharArray();
```

### 2. 字符串转字符串数组（按特定分隔符分割）
使用 `String` 类的 `split()` 方法，该方法接受一个正则表达式作为分隔符，将字符串分割成字符串数组。

```java
String str = "apple,banana,orange";
String[] strArray = str.split(",");
```

### 3. 数组转列表
#### 基本数据类型数组转列表
基本数据类型数组不能直接转换为列表，需要先将其转换为对应的包装类数组，再使用 `Arrays.asList()` 方法。

```java
int[] intArray = {1, 2, 3};
// 先将 int 数组转换为 Integer 数组
Integer[] integerArray = new Integer[intArray.length];
for (int i = 0; i < intArray.length; i++) {
    integerArray[i] = intArray[i];
}
List<Integer> list = Arrays.asList(integerArray);
```

#### 对象数组转列表
对于对象数组，可以直接使用 `Arrays.asList()` 方法。

```java
String[] strArray = {"apple", "banana", "orange"};
List<String> list = Arrays.asList(strArray);
```

### 4. 列表转数组
#### 列表转对象数组
使用 `List` 的 `toArray()` 方法，该方法返回一个 `Object` 类型的数组。

```java
List<String> list = new ArrayList<>();
list.add("apple");
list.add("banana");
Object[] objectArray = list.toArray();
```

如果需要指定数组的类型，可以使用 `toArray(T[] a)` 方法。

```java
List<String> list = new ArrayList<>();
list.add("apple");
list.add("banana");
String[] strArray = list.toArray(new String[0]);
```

### 5. 列表切片得到子列表
使用 `List` 的 `subList(int fromIndex, int toIndex)` 方法，该方法返回一个从 `fromIndex`（包含）到 `toIndex`（不包含）的子列表。

```java
List<String> list = new ArrayList<>();
list.add("apple");
list.add("banana");
list.add("orange");
list.add("grape");
List<String> subList = list.subList(1, 3); // 包含索引 1，不包含索引 3
```

### 6. 集合转数组
对于其他集合类型，如 `Set`，也可以使用 `toArray()` 方法将其转换为数组。

```java
Set<String> set = new HashSet<>();
set.add("apple");
set.add("banana");
String[] strArray = set.toArray(new String[0]);
```

### 7. 数组转集合（除了使用 `Arrays.asList()`）
可以使用循环将数组元素逐个添加到集合中。

```java
String[] strArray = {"apple", "banana", "orange"};
List<String> list = new ArrayList<>();
for (String str : strArray) {
    list.add(str);
}
```

### 注意事项
- `Arrays.asList()` 返回的列表是一个固定大小的列表，不支持添加、删除元素的操作。如果需要可变大小的列表，可以将其传递给 `ArrayList` 的构造函数。
```java
String[] strArray = {"apple", "banana", "orange"};
List<String> fixedSizeList = Arrays.asList(strArray);
List<String> mutableList = new ArrayList<>(fixedSizeList);
```
- `subList()` 返回的子列表是原列表的一个视图，对该子列表的修改会反映到原列表中，反之亦然。如果需要一个独立的子列表，可以创建一个新的 `ArrayList` 并将子列表的元素添加到其中。
```java
List<String> list = new ArrayList<>();
list.add("apple");
list.add("banana");
list.add("orange");
list.add("grape");
List<String> subList = new ArrayList<>(list.subList(1, 3));
```

## 哈希

### 两数之和

> 当遍历到一个数的时候，哈希该数进行加速

```Java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer, Integer> hashtable = new HashMap<>();
        for (int i = 0; i < nums.length; i++){
            if (hashtable.containsKey(target - nums[i])){
                return new int[] {hashtable.get(target - nums[i]), i};
            }
            hashtable.put(nums[i], i);
        }
        return new int[0];
    }
}
```

### 字母异位词分组

> 字符串转换为字符数组进行排序，判断排序后是否相等来判断是否为异位词

```Java
class Solution {
    public List<List<String>> groupAnagrams(String[] strs) {
        Map<String, List<String>> map = new HashMap<>();
        for (String s : strs){
            char[] array = s.toCharArray();
            Arrays.sort(array);
            String key = new String(array);
            if(map.containsKey(key)){
                map.get(key).add(s);
            } else {
                map.put(key, new ArrayList<String>());
                map.get(key).add(s);
            }
        }
        return new ArrayList<List<String>>(map.values());
    }
}
```

### 最长连续序列

> 去重+排序 遍历时取最大值

```Java
class Solution {
    public int longestConsecutive(int[] nums) {
        if(nums.length==0) return 0;
        Set<Integer> hashset = new HashSet<>();
        for (int num : nums){
            hashset.add(num);
        }
        Integer[] new_nums = hashset.toArray(new Integer[0]);
        Arrays.sort(new_nums);
        int max_length = 0;
        int temp_length = 1;
        for (int i = 0; i < new_nums.length - 1; i++){
            if(new_nums[i] + 1 == new_nums[i+1]){
                temp_length ++;
            } else {
                max_length = temp_length > max_length ? temp_length : max_length;
                temp_length = 1;
            }
        }
        max_length = temp_length > max_length ? temp_length : max_length;
        return max_length;
    }
}
```

## 双指针

### 双指针模板
```Java
// 两边靠内
int left = 0;
int right = 0;
while (right > left) {
    if(){
        left++;
    } else {
        right--;
    }
}
```

### 移动零

> 单向双指针移动，左指针指向第一个0，右指针指向最后一个0后

```Java
class Solution {
    public void moveZeroes(int[] nums) {
        int left = 0;
        int right = 0;
        for (int i = 0; i < nums.length; i++){
            if (nums[right]!=0){
                int temp = nums[left];
                nums[left] = nums[right];
                nums[right] = temp;
                left++;
            }
            right++;
        }
    }
}
```

### 

## 滑动窗口

### 无重复字符的最长子串

```Java
class Solution {
    public int lengthOfLongestSubstring(String s) {
        // 字符串转为字符数组
        char[] charArray = s.toCharArray();
        // 记录目前窗口内的字母
        Set<Character> hashSet = new HashSet<>();
        // 结果
        int result = 0;
        for(int left = 0, right = 0; right < charArray.length; right++){
            while(hashSet.contains(charArray[right])){
                // 右字符已出现过则左边界右移
                hashSet.remove(charArray[left]);
                left++;
            }
            hashSet.add(charArray[right]);
            result = Math.max(result, right - left + 1);
        }
        return result;
    }
}
```

## 子串

## 普通数组

## 矩阵

## 链表

### 相交链表

> 使用集合对节点进行储存，判断两者第一个交集即可

```Java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode getIntersectionNode(ListNode headA, ListNode headB) {
        Set<ListNode> hashSet = new HashSet<>();
        while(headA != null){
            hashSet.add(headA);
            headA = headA.next;
        }
        while(headB != null){
            if(hashSet.contains(headB)) return headB;
            headB = headB.next;
        }
        return null;
    }
}
```

### 

## 二叉树

### 二叉树的中序遍历

> 中序遍历 递归解

```Java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();
        inorderBFS(root, result);
        return result;
    }
    public void inorderBFS(TreeNode node, List<Integer> array){
        if (node == null) return;
        inorderBFS(node.left, array);
        array.add(node.val);
        inorderBFS(node.right, array);
    }
}
```

### 二叉树的最大深度

> 最大深度为左右子树的深度取最大值+1，进行递归

```Java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    public int maxDepth(TreeNode root) {
        if (root == null) return 0;
        int left = maxDepth(root.left);
        int right = maxDepth(root.right);
        return left > right ? left + 1 : right + 1;
    }
}
```

### 翻转二叉树

> 后序遍历二叉树，交换左右子树指针

```Java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    public TreeNode invertTree(TreeNode root) {
        if(root == null) return null;
        invertTree(root.left);
        invertTree(root.right);
        TreeNode temp = root.left;
        root.left = root.right;
        root.right = temp;
        return root;
    }
}
```

## 图论

## 回溯

## 二分查找

## 栈

## 堆

## 贪心

## 动态规划

## 多维动态规划

## 技巧