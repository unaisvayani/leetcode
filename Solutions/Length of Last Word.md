### Solution

```c#
public class Solution {
    public int LengthOfLastWord(string s) {
        var list = s.Trim().Split(' ');
        return list[list.Count() - 1].Length;
    }
}
```

### Time/Space Complexity

- Runtime: 71 ms (beats 71.22% of submissions)
- Memory: 36.1 MB (beats 25.15% of submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)