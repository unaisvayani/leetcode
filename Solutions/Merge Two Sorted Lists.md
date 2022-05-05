### Solution

```c#
public class Solution {
    public ListNode MergeTwoLists(ListNode list1, ListNode list2) {
        if (list1 == null) return list2;
        else if (list2 == null) return list1;
       
        var listCheck = list1.val < list2.val;
        var c = listCheck ? list1 : list2;
        var p = listCheck ? list2 : list1;
        var n = c.next;
        var head = c;
        
        if(n == null)
        {
            c.next = p;
            return c;
        }

        while (n != null)
        {
            if (n.val > p.val)
            {
                c.next = p;
                c = c.next;
                p = n;
                n = c.next;
            }
            else
            {
                c = n;
                n = c.next;
            }
        }
        c.next = p;
        return head;
    }
}
```

### Time/Space Complexity

- Runtime: 112 ms (beats 49.87% of C# online submissions)
- Memory: 37.9 MB (beats 84.70% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)