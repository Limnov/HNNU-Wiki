# C/C++ 入门指南

## 为什么选择 C/C++？

虽然现在大一新生首先接触 Python，但强烈建议掌握 C/C++：

- ✅ **底层理解** - 理解计算机内存管理和系统运行原理
- ✅ **性能卓越** - 执行效率高，适合系统编程和竞赛
- ✅ **基础重要** - 许多现代语言（如 Java、Go）都受 C/C++ 影响
- ✅ **竞赛必备** - NOI、ACM 等算法竞赛的主要语言
- ✅ **就业需求** - 嵌入式、游戏开发、系统编程等领域广泛使用

## 安装开发环境

### Windows

#### 方式一：MinGW-w64
```bash
# 使用 MSYS2 安装
pacman -S mingw-w64-x86_64-gcc
```

#### 方式二：Visual Studio
下载 [Visual Studio Community](https://visualstudio.microsoft.com/downloads/)（免费），安装时选择"使用 C++ 的桌面开发"

#### 方式三：Dev-C++（推荐初学者）
[Dev-C++ 下载](https://sourceforge.net/projects/orwelldevcpp/)
> NOI、NOIP 等比赛的指定工具，体积小、安装简单

### macOS

```bash
xcode-select --install
brew install gcc
gcc --version
```

### Linux

```bash
sudo apt install build-essential gdb  # Ubuntu/Debian
```

## 选择开发工具

**推荐：VS Code**
1. 下载 [VS Code](https://code.visualstudio.com/)
2. 安装扩展：
   - C/C++（Microsoft 官方）
   - Code Runner

**其他选择：**
- Visual Studio（Windows，功能最强大）
- CLion（JetBrains 出品，收费）
- Code::Blocks（免费，跨平台）

## 基础语法

### Hello World

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\\n");
    return 0;
}
```

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```

### 变量和数据类型

```c
// C 语言
int age = 20;              // 整数
float height = 1.75f;      // 单精度浮点数
double weight = 65.5;      // 双精度浮点数
char grade = 'A';          // 字符
char name[] = "张三";       // 字符串

printf("我叫%s，今年%d岁\\n", name, age);
```

```cpp
// C++ 语言
int age = 20;
float height = 1.75f;
double weight = 65.5;
char grade = 'A';
string name = "张三";       // C++字符串
bool is_student = true;

cout << "我叫" << name << "，今年" << age << "岁" << endl;
```

### 基本运算

```c
int a = 10, b = 3;

printf("%d\\n", a + b);    // 13
printf("%d\\n", a - b);    // 7
printf("%d\\n", a * b);    // 30
printf("%f\\n", a / (double)b);  // 3.333...
printf("%d\\n", a % b);    // 1  取余
```

### 数组

```c
int scores[5] = {90, 85, 78, 92, 88};

printf("%d\\n", scores[0]);  // 90
scores[1] = 95;

// 遍历
for (int i = 0; i < 5; i++) {
    printf("%d ", scores[i]);
}

// C++ vector
#include <vector>
vector<int> nums = {1, 2, 3};
nums.push_back(4);
```

### 条件语句

```c
int age = 18;

if (age >= 18) {
    printf("你已经成年\\n");
} else if (age >= 13) {
    printf("你是青少年\\n");
} else {
    printf("你是儿童\\n");
}

// 布尔运算
int score = 85;
if (score >= 90) {
    printf("优秀\\n");
} else if (score >= 70) {
    printf("良好\\n");
} else if (score >= 60) {
    printf("及格\\n");
}
```

### 循环

```c
// for 循环
for (int i = 0; i < 5; i++) {
    printf("%d ", i);
}

// while 循环
int count = 0;
while (count < 3) {
    printf("%d ", count);
    count++;
}

// do-while
int num;
do {
    scanf("%d", &num);
} while (num <= 0);
```

### 函数

```c
// 函数声明
int add(int a, int b);

// 函数定义
int add(int a, int b) {
    return a + b;
}

// 调用
int result = add(3, 5);
printf("3 + 5 = %d\\n", result);
```

### 指针（C/C++ 特色）

```c
int num = 42;
int *ptr = &num;  // ptr 存储 num 的地址

printf("num 的值: %d\\n", num);      // 42
printf("num 的地址: %p\\n", &num);
printf("ptr 指向的值: %d\\n", *ptr); // 42

// 通过指针修改值
*ptr = 100;
printf("修改后: %d\\n", num);  // 100
```

### 结构体

```c
struct Student {
    char name[50];
    int age;
    double score;
};

struct Student stu1;
strcpy(stu1.name, "小明");
stu1.age = 20;
stu1.score = 89.5;

printf("姓名: %s, 年龄: %d, 分数: %.1f\\n",
       stu1.name, stu1.age, stu1.score);
```

## 项目练习

### 猜数字游戏

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    srand(time(NULL));
    int number = rand() % 100 + 1;
    int guess, attempts = 0;

    printf("猜数字游戏 (1-100)\\n");

    while (1) {
        printf("请输入你的猜测: ");
        scanf("%d", &guess);
        attempts++;

        if (guess < number) {
            printf("太小了！\\n");
        } else if (guess > number) {
            printf("太大了！\\n");
        } else {
            printf("恭喜你猜对了！用了%d次。\\n", attempts);
            break;
        }
    }
    return 0;
}
```

### 简单计算器

```c
#include <stdio.h>

int main() {
    double num1, num2, result;
    char operator;

    printf("简单计算器 (+, -, *, /)\\n");

    while (1) {
        printf("请输入第一个数字: ");
        scanf("%lf", &num1);

        printf("请输入运算符: ");
        scanf(" %c", &operator);

        printf("请输入第二个数字: ");
        scanf("%lf", &num2);

        switch (operator) {
            case '+': result = num1 + num2; break;
            case '-': result = num1 - num2; break;
            case '*': result = num1 * num2; break;
            case '/':
                if (num2 == 0) {
                    printf("错误：除数不能为零\\n");
                    continue;
                }
                result = num1 / num2;
                break;
            default:
                printf("无效的运算符\\n");
                continue;
        }

        printf("结果: %.2lf\\n", result);

        char another;
        printf("继续? (y/n): ");
        scanf(" %c", &another);
        if (another != 'y' && another != 'Y') break;
    }
    return 0;
}
```

## 常用库

### 标准库（无需安装）

- `stdio.h` / `iostream` - 输入输出
- `stdlib.h` - 通用工具函数
- `string.h` / `string` - 字符串处理
- `math.h` / `cmath` - 数学函数
- `time.h` - 时间处理

## 学习建议

1. **理解内存管理** - 掌握指针和内存分配
2. **多动手实践** - 在线判题系统刷题
3. **学习调试** - 学会使用调试工具
4. **阅读代码** - 看优秀开源项目
5. **循序渐进** - 先学C语言基础，再学C++特性

## 常见问题

### C 和 C++ 应该先学哪个？

**A**: 建议先学 C 语言打基础，再学 C++ 的面向对象和 STL。

### 指针太难了怎么办？

1. 理解内存和地址的概念
2. 多画图理解指针关系
3. 从简单的指针应用开始
4. 多做练习加深理解

### 段错误（Segmentation Fault）怎么办？

1. 检查数组越界
2. 检查空指针解引用
3. 检查野指针
4. 使用调试工具定位

## 学习资源

### 零基础

- [菜鸟教程 C++](https://www.runoob.com/cplusplus/cpp-tutorial.html)
- [OI-Wiki 语言基础](https://oi-wiki.org/lang/)
- [C++ 在线编辑器](https://www.runoob.com/try/runcode.php?filename=helloworld&type=cpp)

### 有一定基础

推荐以 [洛谷题单广场](https://www.luogu.com.cn/training/list) 的顺序练习

### 其他资源

- [C语言中文网](http://c.biancheng.net/)
- [B站黑马程序员C++教程](https://www.bilibili.com/video/BV1et411b73Z)
- [LeetCode 中国](https://leetcode.cn/) - 算法练习

---

**下一步**：
- 深入C++（面向对象、STL、设计模式）
- 数据结构（数组、链表、树、图）
- 算法（排序、搜索、动态规划）
- 系统编程（操作系统、网络编程）

记住：C/C++ 会让你对计算机有更深刻的理解！💪
