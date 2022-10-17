# Leetcode-237-deleteNode


# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

          class Solution:
              def deleteNode(self, node):
                  """
                  :type node: ListNode
                  :rtype: void Do not return anything, modify node in-place instead.
                  """
                  node.val = node.next.val
                  node.next = node.next.next
        
        这个方法是：把要删除的node的下一个值覆盖上来，实际删除的是下一个位置，但把它们复制到现有位置了。
        我愿意称之为：覆盖删除
