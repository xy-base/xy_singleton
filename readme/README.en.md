# xy_singleton

| [简体中文](../README.md)         | [繁體中文](./README.zh-hant.md)        |                      [English](./README.en.md)          |
| ----------- | -------------|---------------------------------------|

## Description
Singleton Tools.

## Source Code Repositories

| [Github](https://github.com/xy-base/xy_singleton.git)         | [Gitee](https://gitee.com/xy-opensource/xy_singleton.git)        |                      [GitCode](https://gitcode.com/xy-opensource/xy_singleton.git)          |
| ----------- | -------------|---------------------------------------|


## Installation

```bash
# bash
pip install xy_singleton
```

## How to use

```python
# Python解释器 (Python Interpreter)
from xy_singleton.Decorators import singleton, Singleton

@singleton
class Cls_0(object):
    count = 0
    def __init__(self):
        pass

@Singleton
class Cls_1(object):
    count = 0
    def __init__(self):
        pass

Cls_0().count = 10
Cls_0().count
# 10
Cls_0().count = 11
# 11
Cls_1().count = 10
# 10
Cls_1().count = 11
Cls_1().count
# 11

from xy_singleton.Singleton import CallSingleton, NewSingleton

class Foo_0(metaclass=CallSingleton):
    count = 0

Foo_0().count = 10
Foo_0().count
# 10
Foo_0().count = 11
Foo_0().count
# 11

class Foo_1(Singleton):
    count = 0
Foo_1().count = 10
Foo_1().count
# 10
Foo_1().count = 11
Foo_1().count
# 11

```

## License
xy_singleton is licensed under the <Mulan Permissive Software License，Version 2>. See the [LICENSE](../LICENSE) file for more info.

## Donate

If you think these tools are pretty good, Can you please have a cup of coffee?  
![pay-total](./pay-total.png)  

## Contact

```
WeChat: yuyangiit
Mail: yuyangit.0515@qq.com
```