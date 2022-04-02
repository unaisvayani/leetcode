### Solution 1

```c#
public class Solution {
    public bool HasCycle(ListNode head) {

        var hashSet = new HashSet<ListNode>();
        var current = head;

        while(true)
        {
            if(current == null || current.next == null)
                return false;
            if(hashSet.Contains(current))
                return true;
            else
                hashSet.Add(current);
            current = current.next;
        }
    }
}
```

### Time/Space Complexity

- Runtime: 182 ms
- Memory: 43.1 MB

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)
