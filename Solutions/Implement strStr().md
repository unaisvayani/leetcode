### Solution

```c#
public class Solution {
    public int StrStr(string haystack, string needle)
    {
       var res = -1;
        
        if(haystack.Length < needle.Length)
        {
            return res;
        }

        var indexList = new List<int>();
        for(int i = 0; i <= haystack.Length-1; i++)
        {
            if(haystack[i] == needle[0])
            {
                indexList.Add(i);
            }
        }

        foreach(int i in indexList)
        {
            if (i + needle.Length-1 <= haystack.Length-1)
            {
                res = i;
                for (int j = i, z = 0; z <= needle.Length-1; j++, z++)
                {
                    if(haystack[j] != needle[z])
                    {
                        res = -1;
                        break;
                    }
                }
                if(res != -1) 
                {
                    return res;
                }
            }

        }
        return res;
    }
}

```

### Time/Space Complexity

- Runtime: 69 ms (beats 78.12% of C# online submissions)
- Memory: 36.6 MB (beats 23.92% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)