class TreeNode {
    int val;
    TreeNode left;
    TreeNode right;
    TreeNode(int x) { val = x; }
}

public class Solution {
    public int maxDepth(TreeNode root) {
        return treeHeight(root);
    }

    private int treeHeight(TreeNode node) {
        if (node == null) return 0; 

        int leftHeight = treeHeight(node.left); 
        int rightHeight = treeHeight(node.right); 

        return 1 + Math.max(leftHeight, rightHeight);
    }
}
