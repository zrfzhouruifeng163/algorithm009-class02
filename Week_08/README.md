学习笔记
一  LRU
LRU：least recent use   最近最少使用
实现：HashMap+双向链表

二 比较类排序：
- 通过比较元素间次序来排序

O(n*n):
1. 选择：每次找到最小值，然后放到待排序数组的起始位置

2. 插入：从前到后逐步构建有序序列，对于未排序数据，在已排序序列中从后往前扫，找到相应位置并插入。

3. 冒泡：嵌套循环，每次查看相邻的元素，如果逆序则交换

O(nlogn):
1. 堆排序

2. 重点-快速排序：取数组标杆pivot，所有小于pivot的放在左侧，大于的放在右侧，然后继续对左右数组进行快排，以达到整个数组有序。

3. 重点-归并排序：将长度为n的序列分为两个长度为n/2的子序列，然后分别对子序列归并排序，将两个排好序的子序列合并

4. 归并与快排
- 二者具有高度相似性，但步骤顺序相反
- 归并:先排序左右子数组，然后合并两个有序子数组
- 快排：先调配出两个左右子数组，然后对左右子数组进行排序

三 非比较类排序：
- 不用比较两个元素间关系
- 一般只能整型