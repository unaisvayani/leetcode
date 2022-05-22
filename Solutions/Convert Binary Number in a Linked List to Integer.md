### Solution

```c#
public class Solution {
    public int GetDecimalValue(ListNode head) {
        var stack = new Stack();
        var index = 0;
        var sum = 0;
        
        while(head != null)
        {
            stack.Push(head.val);
            head = head.next;
        }
        
        while(stack.Count != 0)
        {
            sum = sum + ((int)stack.Pop() * (int)Math.Pow(2, index));
            index = index + 1;
        }
        
        return sum;
    }
}
```

### Time/Space Complexity

- Runtime: 139 ms (beats 16.11% of C# online submissions)
- Memory: 37.3 MB (beats 27.18% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)