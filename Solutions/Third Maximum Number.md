### Solution

```c#
public class Solution {
    public int ThirdMax(int[] nums) {
        var newArray = nums.Distinct().ToArray();
        Array.Sort(newArray);
        
        return  newArray.Length > 2 
            ? newArray[newArray.Length - 3] 
            : newArray[newArray.Length - 1];
    }
}
```

### Time/Space Complexity

- Runtime: 107 ms (beats 73.90% of C# online submissions)
- Memory: 37.8 MB (beats 90.76% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)