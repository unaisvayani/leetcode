### Solution

```c#
public class Solution {
    public ListNode DeleteDuplicates(ListNode head) {
        var curr = head;

        while (curr != null && curr.next != null)
        {
            if (curr.val == curr.next.val)
            {
                var temp = curr.next.next;
                curr.next.next = null;
                curr.next = temp;

                if(temp != null && curr.val != temp.val)
                    curr = curr.next;
            }
            else curr = curr.next;
        }
        return head;
    }
}
```

### Time/Space Complexity

- Runtime: 120 ms (beats 43.36% of C# online submissions)
- Memory: 37.8 MB (beats 97.69% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)