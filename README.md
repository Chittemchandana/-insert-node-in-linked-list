# insert node in-linkedlist
# approach1
# Node class
class Node:
 
    # Function to initialize the 
    # node object
    def __init__(self, data):
 
        # Assign data
        self.data = data  
   
        # Initialize next as null
        self.next = None 
 
# Linked List class
class LinkedList:
   
    # Function to initialize the 
    # Linked List object
    def __init__(self): 
        self.head = None



# appoach2
# This function is defined in Linked List 
# class appends a new node at the end.  
# This method is defined inside LinkedList 
# class shown above 
def append(self, new_data):
 
   # 1. Create a new node
   # 2. Put in the data
   # 3. Set next as None
   new_node = Node(new_data)
 
   # 4. If the Linked List is empty, then 
   #    make the new node as head
   if self.head is None:
        self.head = new_node
        return
 
   # 5. Else traverse till the last node
   last = self.head
   while (last.next):
       last = last.next
 
   # 6. Change the next of last node
   last.next =  new_node



# approach3
# node structure
class Node:
  def __init__(self, data):
    self.data = data
    self.next = None

#class Linked List
class LinkedList:
  def __init__(self):
    self.head = None

  #Add new element at the start of the list
  def push_front(self, newElement):
    newNode = Node(newElement)
    newNode.next = self.head 
    self.head = newNode   

  #display the content of the list
  def PrintList(self):
    temp = self.head
    if(temp != None):
      print("The list contains:", end=" ")
      while (temp != None):
        print(temp.data, end=" ")
        temp = temp.next
      print()
    else:
      print("The list is empty.")

# test the code                  
MyList = LinkedList()

#Add three elements at the start of the list.
MyList.push_front(10)
MyList.push_front(20)
MyList.push_front(30)
MyList.PrintList()
