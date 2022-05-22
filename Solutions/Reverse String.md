### Solution

```c#
public class Solution {
    public void ReverseString(char[] s) {
        for(int i=0, j=s.Length-1; i <= j; i++, j-- )
        {
            var temp = s[i];
            s[i] = s[j];
            s[j] = temp;
        }
    }
}
```

### Time/Space Complexity

- Runtime: 275 ms (beats 66.68% of C# online submissions)
- Memory: 48.4 MB (beats 39.22% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)