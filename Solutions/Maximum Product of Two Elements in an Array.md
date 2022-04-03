### Solution

```c#
public class Solution {
    public int MaxProduct(int[] nums) {
        Array.Sort(nums);
        return (nums[nums.Length-1] - 1) * (nums[nums.Length-2] - 1);
    }
}
```

### Time/Space Complexity

- Runtime: 116 ms (beats 66.09% of submissions)
- Memory: 37.6 MB (beats 50.43% of submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)