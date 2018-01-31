---
layout: post
author: galaxy
tags:
    - python
    - code
---

python正则表达式

re里面先compile生成一个pattern，然后调用match，seach，find，findall，finditer，sub，subn，split等方法

```python
import re

pattern = re.compile(r'\d+')

str = 'hello123world456'

m = pattern.match(str, 5, 10)

print(m.group(0), m.start(), m.end(), m.span())

m = pattern.search(str, 10)

print(m.group(), m.span())

m = pattern.findall(str)

print(m)

pattern = re.compile(r'([a-z]+) ([a-z]+)')

str = 'hello world helle galaxy'

m = pattern.match(str)

print(m.group(1), m.group(2), m.span(1))

m = pattern.finditer(str)

for i in m:
    print(i.group(0))
pattern = re.compile(r' ')
m = pattern.split(str, 2)
print(m)

print(pattern.sub(r'!!', str))

#sub subn
str = 'hello 123, hello 456'
pattern = re.compile(r'(\w+) (\w+)')
def display(m):
    return 'hi ' + m.group(2)
print(pattern.sub(display, str, 1))
print(pattern.subn(display, str, 2))
print(pattern.sub(r'\2 \1', str))
```
