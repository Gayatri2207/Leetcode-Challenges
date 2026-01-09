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
    TreeNode ans;
    int deepest = 0;
    public TreeNode subtreeWithAllDeepest(TreeNode root) {
        dfs(root, 0);
        return ans;
    }
    public int dfs(TreeNode root, int level){
        deepest = Math.max(deepest, level);
        if(root == null){
            return level;
        }
        int left = dfs(root.left, level + 1);
        int right = dfs(root.right, level + 1);
        if(left == deepest && right == deepest){
            ans = root;
        }
        return Math.max(left, right);
    }
}
