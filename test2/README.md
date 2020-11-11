Write a function for reversing a linked list.

Here is the link list node
```
class LinkedListNode {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}
//ANSWER:
//-----------Create single node--------------------//
class LinkedListNode {
    constructor(value) {
      this.value = value;
      this.next = null;
    }
}
//--------------Create linked list chain---------------//
  const listNode = new LinkedListNode(1);
  listNode.next = new LinkedListNode(2);
  listNode.next.next = new LinkedListNode(3);
  listNode.next.next.next = new LinkedListNode(4);
  listNode.next.next.next.next = new LinkedListNode(5);
//---------------Print the linked list----------//
// console.log(listNode)
//---------------Reverse the linked list------------//
function reverseList(head) {
    let previous = null
    let current = head
    let following = head
    while(current !== null) {
        following = following.next
        current.next = previous
        previous = current          
        current = following  
    } 
    return previous
}
console.log(reverseList(listNode));
  
```
