---
layout: post
author: galaxy
tags:
     - python
     - code
---

# python的enumerate函数

实现一个列表变成字典，可以用enumerate函数

- input = ['a', 'b', 'c' , 'd' , 'e']
- {f: i for f, i in zip(input, range(len(input)))}
- {'a': 0, 'c': 2, 'b': 1, 'e': 4, 'd': 3}
- dict(zip(input, range(len(input))))
- {'a': 0, 'c': 2, 'b': 1, 'e': 4, 'd': 3}
- list(enumerate(input))
- [(0, 'a'), (1, 'b'), (2, 'c'), (3, 'd'), (4, 'e')]
- dict(enumerate(input))
- {0: 'a', 1: 'b', 2: 'c', 3: 'd', 4: 'e'}
- {f:i for i, f in enumerate(input)}
- {'a': 0, 'c': 2, 'b': 1, 'e': 4, 'd': 3}
