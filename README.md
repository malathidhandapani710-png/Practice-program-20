class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class Solution:
    def insertAtEnd(self, head, x):
        # 1. Create the new node
        new_node = Node(x)
        
        # 2. If the list is empty, return the new node as head
        if head is None:
            return new_node
        
        # 3. Start from the head and find the last node
        current = head
        while current.next:
            current = current.next
        
        # 4. Point the last node's 'next' to the new node
        current.next = new_node
        
        # 5. Return the original head
        return head
