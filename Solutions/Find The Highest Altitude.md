### Solution

```c#
public class Solution {
    public int LargestAltitude(int[] gain) {
        
        var alt = 0;
        var max = alt;
        
        for(int i = 0; i < gain.Length; i++)
        {   
            alt += gain[i];
            if(alt > max) 
            {
                max = alt;
            }
        }
        return max;
        
    }
}
```

### Time/Space Complexity

- Runtime: 109 ms (beats 67.14% of C# online submissions)
- Memory: 37.1 MB (beats 27.14% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)