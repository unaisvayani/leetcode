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

### Solution 2 (More efficient)

```c#
public class Solution {
    public bool HasCycle(ListNode head) {
        var fast = head;
        var slow = head;
        
        if(head == null || head.next == null)
            return false;
       
        while(fast != null && fast.next != null)
        {
            slow = slow.next;
            fast = fast.next.next;
            
            if(slow == fast)
                return true;
        }
        return false;
    }
}
```

### Time/Space Complexity

- Runtime: 123 ms (beats 69.73 % of C# online submissions)
- Memory: 41.3 MB (beats 70.80 % of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)
