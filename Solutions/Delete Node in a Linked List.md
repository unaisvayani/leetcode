### Solution

```c#
public class Solution {
    public void DeleteNode(ListNode node) {
        node.val = node.next.val;
        node.next = node.next.next;
    }
}
```

### Time/Space Complexity

- Runtime: 111 ms (beats 48.80% of C# online submissions)
- Memory: 37.7 MB (beats 81.12% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)