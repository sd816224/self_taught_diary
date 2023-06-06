# **self taught diary**
## This is the diary for my journey to becoming a developer job by self-taught coding.

i'll keep every it concise and concludes what i've done on the day.
task of the day can be any of the bellow:
- solve problem on leetcode
- contribute on github
- build up own project

i know the journey may be very long and tough. i may pivat my target a few times.
but how can i view the scene without starting the journey. 
let's go.


interesting projects to do:
- personal profile page
- slot booking system
- backtesting framework

---
### 05/06/2023
work on leetcode 226, met the binary tree. 
the main takeaway is its sturcture and insert function that i can build a tree for testcase simulation
```python
# data structure:
class TreeNode(object):
    def __init__(self,val=0,left=None,right=None):
        self.val=val
        self.left=left
        self.right=right
# inset function
    def insert(self,val):
        if self.val:
            if val<self.val:
                if self.left is None:
                    self.left=TreeNode(val)
                else:
                    self.left.insert(val)
            elif val>self.val:
                if self.right is None:
                    self.right=TreeNode(val)
                else:
                    self.right.insert(val)
        else:
            self.val=val
# print tree
    def PrintTree(self):
        if self.left:
            self.left.PrintTree()
        print(self.val)
        if self.right:
            self.right.PrintTree()
```
there's 3 tree traversals: 
- in order traversal
- pre order traversal
- post order traversal

- [x] get into detail of different traversals algorithm 
  - https://www.tutorialspoint.com/python_data_structure/python_tree_traversal_algorithms.htm
- [x] need to learn to mark a note in Markdown as well.
  - https://www.markdownguide.org/basic-syntax/#italic
  - https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
- [x] after that leetcode problem is still not solved, need to carry on tmr.

other takeaway:
```python
# exchange value: 
a,b = b,a

# to create the input output loop function:
def function(init_input):
    next_input=2+init_input
    return function(next_input)
```

---
### 06/06/2023

markdown takeaway:
```markdown
click to the linked file: []()
[click to redirect to the file](./test_dict/test_py.py)

divider: ---

crossover line: ~~~text~~~

```

inorder: left-root-right
preorder: root-left-right
postorder: left-right-root
```python
def inorder_traversal(self,root):
    res=[]
    if root:
        res=self.inorder_traversal(root.left)
        res.append(root.val)
        res=res+self.inorder_traversal(root.right)
    return res
  
def preorder_traversal(self,root):
    res=[]
    if root:
        res.append(root.val)
        res=res+self.preorder_traversal(root.left)
        res=res+self.preorder_traversal(root.right)
    return res

def postorder_traversal(self,root):
    res=[]
    if root:
        res=self.postorder_traversal(root.left)
        res=res+self.postorder_traversal(root.right)
        res.append(root.val)
    return res
```

leetcode 104: done the basic solution
- [] need to learn deep to the better solution with queue/stack method
