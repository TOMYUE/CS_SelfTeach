# 容器用法整理

[TOC]

## list

==list 是可变有序容器==

| 列表生成     | 直接`a=[1,2]`            | 转换为列表形式`list([1,2])` | 列表生成式`[x**2 for x in range(10)]` |                 |
| ------------ | ------------------------ | --------------------------- | ------------------------------------- | --------------- |
| **拼接**     | `+`                      | `a.extend(b)`               |                                       |                 |
| **复制**     | `*`                      | `a.copy()`                  |                                       |                 |
| **逻辑运算** | `in`                     | `not in`                    | `!=` `==`                             |                 |
| **内置函数** | `len()`                  | `min()`                     | `max()`                               | `del()`         |
| **删除**     | `del a[0]`               | `a.pop(0)`                  | a.remove(a[0])                        |                 |
| **索引**     | `a[index]`               | `a.index(i)`                |                                       |                 |
| **提取**     | `a[index]`               | `a[start:]`                 | `a[:stop]`                            | `a[start:stop]` |
| **排序**     | `a.sort()`               | `a.reverse()`               |                                       |                 |
| **添加元素** | `a.append(value)`        | `a.insert(i,x)`             |                                       |                 |
| **合并列表** | `a.extend(another_list)` | `a_list + b_list`           |                                       |                 |
| **移除元素** | `del a[index]`           | `a.pop(index)`              | `a.remove(value)`                     |                 |
| **列表逆序** | `a.reverse()`            |                             |                                       |                 |
| **清空列表** | `a = [ ]`                | `a.clear()`                 |                                       |                 |

### 几个容易混淆用法的比对

> 有逻辑的东西分开记忆，无逻辑的东西一起记忆。无逻辑的用理解和比对把他们变成有逻辑的再记忆

#### 索引的区分

![image-20220314135242744](../../../../Library/Application%20Support/typora-user-images/image-20220314135242744.png)

#### 拼接list

![image-20220314135010373](../../../../Library/Application%20Support/typora-user-images/image-20220314135010373.png)

#### 删除list元素

![image-20220314134901881](../../../../Library/Application%20Support/typora-user-images/image-20220314134901881.png)、





## tuple

==tuple是不可变有序容器==

| tuple创建 | 直接`a = (1,2)` `a = (2,)` |      |      |      |
| --------- | -------------------------- | ---- | ---- | ---- |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |
|           |                            |      |      |      |



#### tuple使用的原因

`tuple`不可改变，相对`list`来说使用的空间更小

## dictionary



