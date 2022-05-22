### Solution

```c#
public class Node {
    public int key;
    public int value;
}

public class MyHashMap {

    public List<Node> NodeList;

    public MyHashMap() {
        NodeList = new List<Node>();
    }

    public void Put(int key, int value) {
        var nodeHavingKey = getNodeHavingKey(key, NodeList);

        if(nodeHavingKey != null)
        {
            nodeHavingKey.value = value;
        }
        else
        {
            var newNode = new Node() { key = key, value = value};
            NodeList.Add(newNode);
        }
    }

    public int Get(int key) {
        var nodeHavingKey = getNodeHavingKey(key, NodeList);

        return nodeHavingKey != null ? nodeHavingKey.value : -1;
    }

    public void Remove(int key) {
        var nodeHavingKey = getNodeHavingKey(key, NodeList);

        if(nodeHavingKey != null)
        {
            NodeList.Remove(nodeHavingKey);
        }
    }

    public Node getNodeHavingKey(int key, List<Node> list)
    {
        return list.Find(x => x.key == key);
    }
}
```

### Time/Space Complexity

- Runtime: 604 ms (beats 12.61% of C# online submissions)
- Memory: 51.3 MB (beats 62.89% of C# online submissions)

### Links

- [github.com/unaisvayani](https://github.com/unaisvayani)
