学习笔记
一 字典树：
要点：
- 以字符串每个字符为节点，从顶到底依次查找。从顶到叶子节点，串联起来为完成的单词
- 是一个多叉树，如果只论小写字母，即26叉树，每个节点都是26叉。
- 精准查询，避免冗余的比较。
- 控件使用巨大，查询效率极高，空间换时间

用途：
- 输入部分字母后，搜索提示

二 并查集
用途：
- 用于解决两个个体是否在一个集合当中
- 在一个大集合中有多少个独立的小集合

三 二叉搜索树
- 每个节点最多二叉
- 左子树小于根节点，根节点小于右子树
- 中序遍历的话，是有序数组

四  平衡二叉树  
- 二叉搜索树的时间复杂度等于树的深度，因此尽量让深度变小
- 对于二叉树的极端情况，其时间复杂度很高
- 因此，左右子树高度尽量平衡，依次类推每个子树也这样，这样就构成了平衡二叉树

五 AVL
- 平衡因子，左子树高度减去右子树的高度，在[-1，0，1】之间
- 通过旋转来平衡（四种旋转方法）左旋  右旋  左右旋  右左旋

不足之处；
- 节点要存储额外信息
- 频繁旋转操作

六 近似平衡二叉树
原因：AVL过于严格，有时可能-2 -3也是可以接受的，因此出现近似平衡二叉树

红黑树
- 左右子树高度差小于2倍

AVL与红黑树对比
- AVL比红黑树查询效率高，因为AVL更加平衡，深度更小
- 红黑树比AVL删除和插入效率高，因为AVL要保持平衡需要更多的旋转操作。
- AVL比红黑树需要更多的存储空间-1 0 1      红黑树需要0 或1  表示红或黑
- 读操作多用AVL  写操作多用红黑树
- 高级语言的map set等用的是红黑树，数据库里的读操作一般用AVL
