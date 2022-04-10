### Solution

```c#
public class Solution {
    public string ReverseVowels(string str) {
       
        var newStr = str.ToCharArray();
        
        for(int i=0, j=newStr.Length-1; i<j;  )
        {
            if(!isVowel(newStr[i]))
            {
                i++;
                continue;
            }
            if(!isVowel(newStr[j]))
            {
                j--;
                continue;
            }
            
            var temp = newStr[j];
            newStr[j] = newStr[i];
            newStr[i]= temp;
               
            i++;
            j--;
        }
        return new string(newStr.ToArray());
    }
    
    public bool isVowel(char c) => "aeiou".Contains(Char.ToLower(c)) ? true : false;
}
```

### Time/Space Complexity

- Runtime: 84 ms (beats 87.88% of C# online submissions)
- Memory: 42.9 MB (beats 8.79% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)