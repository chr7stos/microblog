This is a simple solution that takes a list of nodes and 
outputs a graph as a list of tuples representing edges between 
nodes that have an Eulerean tour.

``` python
def edge(x, y):
    return (x, y) if x < y else (y, x)

def create_tour(nodes):
    # a very simple solution could just connect
    # the first node with the second node
    # second with third... and the last with the
    # first
    tour = []
    l = len(nodes)
    for i in range(l):
        t = edge(nodes[i], nodes[(i+1) % l])
        tour.append(t)
    return tour
```

From Udacity-cs215 Intro to algorithms by Michael Litman.
https://www.udacity.com/wiki/cs215/problemset1code