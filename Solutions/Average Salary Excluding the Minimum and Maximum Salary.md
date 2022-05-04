### Solution

```c#
public class Solution {
    public double Average(int[] salary) {
        Array.Sort(salary);
        double sum = 0;

        for(int i = 1 ; i < salary.Length - 1 ; i++)
        {
            sum += salary[i];
        }
        return sum/(salary.Length - 2);
    }
}
```

### Time/Space Complexity

- Runtime: 82 ms (beats 84.42% of C# online submissions)
- Memory: 38.1 MB (beats 38.1 MB of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)