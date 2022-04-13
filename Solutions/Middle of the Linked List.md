### Solution

```c#
public class Solution {
    public ListNode MiddleNode(ListNode head) {
        var ptr1 = head;
        var ptr2 = head;
        
        while(ptr2.next != null)
        {
            ptr1 = ptr1.next;
            
            if(ptr2.next.next != null)
                ptr2 = ptr2.next.next;
            else 
                break;
        }
        return ptr1;
    }
}
```

### Time/Space Complexity

- Runtime: 94 ms (beats 73.16% of C# online submissions)
- Memory: 38 MB (beats 18.18% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)