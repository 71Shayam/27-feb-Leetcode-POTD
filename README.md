class Solution {
public:
    int Diameter=0 ;
    int height(TreeNode*root){
        if(root==NULL)
        return 0;
        int leftHeight=height(root->left) ;
        int rightHeight=height(root->right) ;
        int currentDiameter = leftHeight+rightHeight ;
        Diameter = max(Diameter, currentDiameter) ;
        return max(leftHeight,rightHeight) + 1 ;
    }
    int diameterOfBinaryTree(TreeNode* root) {
        height(root) ;
        return Diameter;
    }
};
