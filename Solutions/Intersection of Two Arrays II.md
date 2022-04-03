### Solution

```c#
public class Solution {
    public int[] Intersect(int[] nums1, int[] nums2) {
        
        var list1 = nums1.ToList();
        var list2 = nums2.ToList();
        
        var longest = list1.Count() <= list2.Count() ? list2 : list1;
        var shortest = longest == list2 ? list1 : list2;
        var result = new List<int>();
        
        foreach(int i in shortest)
        {
            if(longest.Contains(i))
            {
                result.Add(i);
                longest.Remove(i);
            }
        }
        return result.ToArray();
    }
}
```

### Time/Space Complexity

- Runtime: 141 ms (beats 81.00% of submissions)
- Memory: 41.9 MB (beats 60.84% of submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)