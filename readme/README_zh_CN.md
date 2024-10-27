<!--
 * @Author: yuyangit yuyangit.0515@qq.com
 * @Date: 2024-10-18 14:44:40
 * @LastEditors: yuyangit yuyangit.0515@qq.com
 * @LastEditTime: 2024-10-18 19:25:51
 * @FilePath: /xy_singleton/readme/README_zh_CN.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# xy_singleton

- [简体中文](README_zh_CN.md)
- [繁体中文](README_zh_TW.md)
- [English](README_en.md)

## 说明
单例工具。

## 源码仓库

- <a href="https://github.com/xy-base/xy_singleton.git" target="_blank">Github地址</a>  
- <a href="https://gitee.com/xy-base/xy_singleton.git" target="_blank">Gitee地址</a>

## 安装

```bash
# bash
pip install xy_singleton
```

## 使用

###### python脚本

```python
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

## 许可证
xy_singleton 根据 <木兰宽松许可证, 第2版> 获得许可。有关详细信息，请参阅 [LICENSE](../LICENSE) 文件。

## 捐赠

如果小伙伴们觉得这些工具还不错的话，能否请咱喝一杯咖啡呢?  

![Pay-Total](./Pay-Total.png)


## 联系方式

```
微信: yuyangiit
邮箱: yuyangit.0515@qq.com
```