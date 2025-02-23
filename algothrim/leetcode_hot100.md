# LeetCode Hot 100

Java Version

## 哈希

### 两数之和

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

## 滑动窗口

## 子串

## 普通数组

## 矩阵

## 链表

## 二叉树

### 二叉树的中序遍历

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