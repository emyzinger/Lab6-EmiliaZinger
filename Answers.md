**Why does FixedArrayQueue require an explicit constructor?**
FixedArrayQueue requires an explicit constructor because this implementation uses an array which requires a size when it is instantiated. Additionally this FixedArrayQueue is of a fixed size, so the size should be decided at the beginning. When there is not an explicit constructor, java sets all the values to null or to zero which is not how all the values are supposed to be set. 

**What happens when you offer an item to a full FixedArrayQueue?**
If you offer an item to a full FixedArrayQueue, then the offer() method returns false and it is up to the main program how to handle adding too many items to the queue.

**What happens when you poll an empty FixedArrayQueue?**
When an empty FixedArrayQueue is polled the method returns null and again it is up to the main program how to handle the null value and then let the user know. 

**What is the time and (extra) space complexity of each of the FixedArrayQueue methods?**
All the methods other than asList() are O(1) because the only things they have to do have indexes in the array and do not include a loop. The space complexity of those methods is O(1) because none of them require any extra space. The asList() method has complexity of O(n) because it has one single loop that has to be done n times. The asList() method has a space complexity of O(n) because creating the list requires the same amount of space as the queue has already. 