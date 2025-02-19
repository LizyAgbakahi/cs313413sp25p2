COMP 413 Spring 2025
Student: Lizy Agbakahi

Answers to questions for project 2

TestIterator.java

TODO Question. Is there a difference behaviorally if an ArrayList or LinkedList is used?

 Answer: No, there is no behavioral difference in how the Iterator works in this test. Both
 ArrayList and LinkedList implement the List interface so they follow the same iteration and ordering behavior.

TODO Question: What happens if you use list.remove(Integer.valueOf(77))?

Answer: If you use list.remove(Integer.valueOf(77)), only the first occurrence of 77 would be removed in the list.


TestList.java

TODO Question: Also try with a LinkedList - does it make any difference?

Answer: No, there is no difference with a LinkedList here behaviorally because both ArrayList and LInkedLIst implement the List interface.

TODO Question: What does this method do?

The list.remove(5); method used in the TestRemoveObject method removes the element at index 5.

TODO Question: What does this one do?

list.remove(Integer.valueOf(5)); This method removes the element with the value of 5.

TestPerformance.java

Results of Performance test with size at 10 and reps at 10,000,000

testArrayListAccess 18 ms
testLinkedListAddRemove 77 ms
testLinkedListAccess 26 ms
testArrayListAddRemove 115 ms

Results of Performance test with size at 100 and reps at 10,000,000

testArrayListAccess 17 ms
testLinkedListAddRemove 76 ms
testLinkedListAccess 122 ms
testArrayListAddRemove 193 ms

Results of Performance test with size at 1000 and reps at 100,000,000

testArrayListAccess 89 ms
testLinkedListAddRemove 432 ms
testLinkedListAccess 29 sec 782 ms
testArrayListAddRemove 14 sec 155 ms

Results of Performance test with size at 10000 and reps at 10,000,000

testArrayListAccess 17 ms
testLinkedListAddRemove 77 ms
testLinkedListAccess 43 sec 875 ms
testArrayListAddRemove 15 sec 353 ms


TODO Question: What conclusions can you draw about the performance of LinkedList vs. ArrayList when comparing their running times for AddRemove vs. Access?

Answer: The results revealed that ArrayList generally performs better for access operations due to its
contiguous memory allocation and faster indexing, while LinkedList performs better for add/remove operations
at both ends due to its node-based structure.

As the size of the list increases, ArrayList generally performs better due to its constant time access speed and
efficient memory usage. While LinkedList excels art frequent insertions and deletions at the beginning, its poor
random access performance makes it significantly slower as the list grows. On the other hand though, ArrayList suffers
when adding and removing elements at the start and middle due to shifting, but where random access is frequent,
ArrayList scales better with size.