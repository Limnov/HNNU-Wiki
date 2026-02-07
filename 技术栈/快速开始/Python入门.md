# Python 入门指南

## 为什么选择 Python？

Python 是最适合编程初学者的语言：

- ✅ **语法简洁** - 接近英语，易于理解
- ✅ **应用广泛** - 数据分析、AI、Web开发、自动化
- ✅ **生态丰富** - 海量的第三方库
- ✅ **学习资源多** - 免费教程和社区支持

## 安装 Python

### Windows

1. 访问 [Python官网](https://www.python.org/downloads/)
2. 下载最新版安装包（3.10+）
3. **重要**：安装时勾选 "Add Python to PATH"
4. 验证：`python --version`

### macOS

```bash
brew install python3
python3 --version
```

### Linux

```bash
sudo apt install python3  # Ubuntu/Debian
```

## 选择开发工具

**推荐：VS Code**
1. 下载 [VS Code](https://code.visualstudio.com/)
2. 安装 Python 扩展

**其他选择：**
- PyCharm Community（功能强大）
- Jupyter Notebook（适合数据分析）
- Thonny（专为初学者）

## 基础语法

### Hello World

```python
print("Hello, World!")
```

### 变量和数据类型

```python
name = "张三"        # 字符串
age = 20            # 整数
height = 1.75       # 浮点数
is_student = True   # 布尔值

print(f"我叫{name}，今年{age}岁")
```

### 基本运算

```python
a, b = 10, 3

print(a + b)   # 13 加法
print(a - b)   # 7  减法
print(a * b)   # 30 乘法
print(a / b)   # 3.333... 除法
print(a // b)  # 3  整除
print(a % b)   # 1  取余
print(a ** b)  # 1000 幂运算
```

### 列表（List）

```python
fruits = ["苹果", "香蕉", "橙子"]

print(fruits[0])        # 输出：苹果
fruits.append("葡萄")   # 添加
fruits.remove("香蕉")   # 删除

# 遍历
for fruit in fruits:
    print(fruit)
```

### 条件语句

```python
age = 18

if age >= 18:
    print("你已经成年")
elif age >= 13:
    print("你是青少年")
else:
    print("你是儿童")

# 布尔运算
score = 85
if 90 <= score <= 100:
    print("优秀")
elif 70 <= score < 90:
    print("良好")
elif score >= 60:
    print("及格")
```

### 循环

```python
# for 循环
for i in range(5):  # 0, 1, 2, 3, 4
    print(f"第{i+1}次循环")

# while 循环
count = 0
while count < 3:
    print(count)
    count += 1
```

### 函数

```python
def greet(name):
    return f"你好，{name}！"

# 调用函数
message = greet("小红")
print(message)

# 带默认参数
def introduce(name, age=18):
    print(f"我叫{name}，今年{age}岁")

introduce("小李")      # 使用默认年龄
introduce("小王", 25)  # 指定年龄
```

### 字典（Dictionary）

```python
student = {
    "name": "小明",
    "age": 20,
    "major": "计算机科学"
}

print(student["name"])       # 访问值
student["grade"] = "大二"    # 添加
student["age"] = 21         # 修改

# 遍历
for key, value in student.items():
    print(f"{key}: {value}")
```

## 项目练习

### 猜数字游戏

```python
import random

def guess_number_game():
    number = random.randint(1, 100)
    attempts = 0

    print("欢迎来到猜数字游戏！")
    print("我想了一个1到100之间的数字")

    while True:
        guess = int(input("请输入你的猜测: "))
        attempts += 1

        if guess < number:
            print("太小了！")
        elif guess > number:
            print("太大了！")
        else:
            print(f"恭喜你猜对了！用了{attempts}次尝试。")
            break

guess_number_game()
```

### 简单计算器

```python
def calculator():
    while True:
        try:
            num1 = float(input("请输入第一个数字: "))
            operator = input("请输入运算符 (+, -, *, /): ")
            num2 = float(input("请输入第二个数字: "))

            if operator == "+":
                result = num1 + num2
            elif operator == "-":
                result = num1 - num2
            elif operator == "*":
                result = num1 * num2
            elif operator == "/":
                if num2 == 0:
                    print("错误：除数不能为零")
                    continue
                result = num1 / num2
            else:
                print("无效的运算符")
                continue

            print(f"结果: {result}")

        except ValueError:
            print("错误：请输入有效的数字")

        another = input("\n是否继续计算? (y/n): ")
        if another.lower() != 'y':
            break

calculator()
```

## 常用库

### 数据处理

```bash
pip install pandas numpy
```

### Web开发

```bash
pip install flask django
```

### 数据可视化

```bash
pip install matplotlib seaborn
```

### 网络爬虫

```bash
pip install requests beautifulsoup4
```

## 学习建议

1. **多动手实践** - 不要只看书，多写代码
2. **从简单项目开始** - 完成小项目建立信心
3. **学会查文档** - 遇到问题先查官方文档
4. **参与社区** - 加入Python学习群，与他人交流
5. **保持耐心** - 编程需要时间积累

## 常见问题

### Python 2 和 Python 3 的区别？

**A**: Python 2 已于2020年停止维护，新手直接学习 Python 3 即可。

### 遇到报错怎么办？

1. 仔细阅读错误信息
2. 复制错误信息到搜索引擎
3. 检查代码的语法和逻辑
4. 使用 print() 调试

### 如何提升编程能力？

1. 坚持每天写代码
2. 做项目练习
3. 阅读优秀代码
4. 学习算法和数据结构

## 学习资源

- [Python官方教程](https://docs.python.org/zh-cn/3/tutorial/)
- [廖雪峰Python教程](https://www.liaoxuefeng.com/wiki/1016959663602400)
- [菜鸟教程Python](https://www.runoob.com/python3/python3-tutorial.html)
- [B站黑马程序员Python教程](https://www.bilibili.com/video/BV1q54y1s75o)

---

**下一步**：
- 深入Python（面向对象、装饰器、生成器）
- 选择方向（Web开发、数据分析、AI、自动化）
- 做项目（个人博客、爬虫、数据分析项目）

记住：多写代码是学好编程的唯一途径！🐍
