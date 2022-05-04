### Solution

```c#
public class Solution {
    public ListNode ReverseList(ListNode head) 
    {
        ListNode prev = null;
        ListNode curr = head;
        ListNode next;
        
        while(curr != null)
        {
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        
        head = prev;
        return head;
    }
}
```

### Time/Space Complexity

- Runtime: 125 ms (beats 31.54% of C# online submissions)
- Memory: 37.8 MB (beats 80.50% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)