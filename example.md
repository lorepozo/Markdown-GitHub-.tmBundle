# Syntactic Examples
### Javascript

```Javascript
function $(e){
	var q=document.querySelectorAll(e);
	return q.length==0?null:q.length==1?q[0]:q;
}
```

### Python

```Python
def search(successors, startState, goalTest, dfs = False):
    if goalTest(startState):
        return [startState]
    else:
        agenda = [SearchNode(startState, None)]
        visited = {startState}
        while len(agenda) > 0:
			parent = agenda.pop(-1 if dfs else 0)
            for childState in successors(parent.state):
                child = SearchNode(childState, parent)
                if goalTest(childState):
                    return child.path()
                if childState not in visited:
                    agenda.append(child)
                    visited.add(childState)
        return
```

### Shell

```Bash
mkcd () {
    mkdir -p "${1}"
    cd "${1}"
}
```

### And countless more...
