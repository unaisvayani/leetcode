### Solution

```c#
public class Solution {
    public ListNode RemoveElements(ListNode head, int val) {
        var curr = head;
        var prev = head;
        
        if(curr == null || (curr.val == val && curr.next == null)) 
            return null;
       
        while(curr != null)
        {
            if(curr == head && curr.val == val)
            {
                head = curr.next;
                prev = head;
                curr = head;
            }
            else if(curr.val == val && curr.next == null)
            {
                prev.next = curr.next;
                curr = prev;
            }
            else if(curr.val == val)
            {
                prev.next = curr.next;
                curr = prev.next;
            }
            else
            {
                prev = curr;
                curr = curr.next;
            }
        }
        return head;
    }
```

### Time/Space Complexity

- Runtime: 94 ms (beats 80.04% of C# online submissions)
- Memory: 42.1 MB (beats 19.55% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)