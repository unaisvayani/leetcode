### Solution

```c#
public class Solution {
    public bool IsPalindrome(ListNode head) {
        Stack stk = new Stack();
        var curr = head;
        
        while(curr != null)
        {
            stk.Push(curr.val);
            curr = curr.next;
        }
        
        while(head != null)
        {
            if((int) stk.Pop() != head.val)
            {
                return false;
            }
            head = head.next;
        }
        return true;
    }
}
```

### Time/Space Complexity

- Runtime: 435 ms (beats 15.33% of C# online submissions)
- Memory: 54.2 MB (beats 38.67% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)