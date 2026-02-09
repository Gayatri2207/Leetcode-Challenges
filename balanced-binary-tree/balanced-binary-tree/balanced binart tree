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
    List<Integer> arr;
    private void inOrder(TreeNode root) {
        arr = new ArrayList<>();
        Deque<TreeNode> stack = new ArrayDeque<>();
        TreeNode node = root;
        while (node != null || !stack.isEmpty()) {
            while (node != null) {
                stack.push(node);
                node = node.left;
            }
            node = stack.pop();
            arr.add(node.val);
            node = node.right;
        }
    }
    private TreeNode balanceBST(int l, int r) {
        if (l > r) return null;
        
        int m = (l + r) / 2;
        TreeNode left = (l > m - 1) ? null : balanceBST(l, m - 1);
        TreeNode right = (m + 1 > r) ? null : balanceBST(m + 1, r);
        
        return new TreeNode(arr.get(m), left, right);
    }
    public TreeNode balanceBST(TreeNode root) {
        inOrder(root);
        return balanceBST(0, arr.size() - 1);
    }
}
