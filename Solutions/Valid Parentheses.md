### Solution

```c#
public class Solution {
    public bool IsValid(string s) {
        if(s.Length % 2 != 0 || IsCloseBracket(s[0])) return false;
       
        var stack = new Stack();
        
        for(int i = 0 ; i < s.Length; i++)
        {
            if(IsOpenBracket(s[i]))
            {
                stack.Push(s[i]);
                continue;
            }
            else if(IsCloseBracket(s[i]) && stack.Count > 0 && IsPairMatch((char)stack.Peek(), s[i]))
            {
                stack.Pop();
                continue;
            }
            else return false;
        }
        return stack.Count == 0;
        
    }
    public bool IsOpenBracket(char c)
    {
        return "({[".Contains(c);
    }
     public bool IsCloseBracket(char c)
    {
        return "]})".Contains(c);
    }
    public bool IsPairMatch(char c, char d)
    {
        var joined = c.ToString() + d.ToString();
        return joined == "()" || joined == "{}" || joined == "[]";
    }
}
```

### Time/Space Complexity

- Runtime: 77 ms (beats 80.53% of C# online submissions)
- Memory: 38.2 MB (beats 17.26% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)