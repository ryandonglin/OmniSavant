# raw link

[Throne Inheritance](https://leetcode.cn/problems/throne-inheritance/description/?envType=daily-question&envId=2024-04-07)

# Difficulty
`Medium`

# Tags
`DFS` `PreOrderTraversal` `trie`

# Solution


## Code slice
```java
public class TreeNode{
    int val;
    List<TreeNode> children;
}


public List<Integer> preOrderTraversal(TreeNode root) {

    List<Integer> result = new ArrayList();

     if (root == null) {
        return result;
    }

    result.add(root.val);

    if (null != root.children) {
        for (TreeNode child: root.children) {
            result.addAll(preOrderTraversal(child));
        }
    }

    return result;
}
```

