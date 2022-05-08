### Solution

```c#
public class Solution {
    public ListNode GetIntersectionNode(ListNode headA, ListNode headB) {
        var a = headA;
        var b = headB;
        ListNode c = null;
        var count = 0;

        while (true)
        {
            if (a == null)
            {
                c = b;
                a = headB;
                b = headA;
                break;
            }
            if (b == null)
            {
                c = a;
                a = headA;
                b = headB;
                break;
            }

            a = a.next;
            b = b.next;
        }
        while (c != null)
        {
            c = c.next;
            count++;
        }

        while (a != null)
        {
            if (count > 0)
            {
                count--;
                a = a.next;
                continue;
            }
            if (a == b)
            {
                return a;
            }
            else
            {
                a = a.next;
                b = b.next;
            }
        }
        return a;
    }
}
```

### Time/Space Complexity

- Runtime: 104 ms (beats 98.65% of C# online submissions)
- Memory: 51.9 MB (beats 7.73% of C# online submissions)

### Explaination

- [Check my post on discussion forum] (https://leetcode.com/problems/intersection-of-two-linked-lists/discuss/2020002/Runtime-faster-than-98.65-of-C-online-submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)