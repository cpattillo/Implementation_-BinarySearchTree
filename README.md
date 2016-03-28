# Implementation_-BinarySearchTree

I implement a binary tree that stores INT and CHAR objects. The program reads a text file and inserts, searches for, deletes and prints
the data in pre-order, post-order and in-order notation. In my main function I extract the file path of the text file from the command
line. I then pass this file path to my load function and create an ifstream object. I then test to see if the ifstream object opens.
Next, I have a large while loop that traverses each line of the text file using the getline function and a stringstream object. If the
command from the text file is “L:” I create a new ifstream object that opens the INT file, which is stored in the project and debug
folder. I then convert each number into an INT object and insert the INT objects into the binary tree. The rest of the while loop
inserts, deletes, search for and prints out the data. 	

My program contains a CHAR and INT struct that has a data pointer. The data pointer points to a new CHAR or INT. Both of the classes
contain copy constructors, destructors and overloaded =, ==, < and > operators. The data in the text file is converted to a CHAR or
INT object and then inserted into the binary tree. Additionally, I have a BNode and BinaryTree class that contains all the operations
for the binary tree.

The BNode class has three pointers: a left, right and node pointer that points to the information in the node. Similar to the INT and
CHAR structs, the BNode class has a copy constructor, overloaded =, ==, > and < operators. The BinaryTree class has a BNode pointer
that points to the root of the tree and a nodeCount parameter that keeps track of the number of nodes. I have a deleteNode, deleteAll,
insert, find, height, printInOrder, printPreOrder and printPostOrder. All these methods contain internal helper methods to access the
root pointer. The insert method checks if the root pointer is pointing to null. If it is not null, there are a series of if statements
that compare the values in the node and then insert the node into the tree. The deleteAll method works by recursively traversing the
tree until the current pointer is null and then deleting the nodes. The find method traverses the left and right branches of the tee
by comparing the values and return true or false. The remove function first locates the node to remove and then deletes the node. If
node to delete has only has one child, the node’s parent will point to the child. If the node has two children, the parent points to
the right node. Then, I traverse the right subtree to find the smallest node. The left subtree is then attached to the smallest node
in the right subtree. 
