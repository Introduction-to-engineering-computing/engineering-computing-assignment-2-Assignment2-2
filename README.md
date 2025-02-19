# Assignment2
# 题目2 - 多项式乘积计算

## 题目要求

编写程序计算 `(x - x0)(x - x1)...(x - xn)`  
**输入格式**：  
```
n x x0 x1 x2 ... xn

```
其中：
- `n` 为整数（n ≥ 0）
- `x` 为浮点数

- `x0, x1,...,xn` 为浮点数列表

**输出格式**：  
```
乘积结果为: {结果保留2位小数}
```
或错误提示：
```
输入错误: {具体原因}
```

---

## 如何开始

1. **克隆仓库**
   ```bash

   git clone https://github.com/your-classroom/assignment-2.git

   cd assignment-2/problem2

   ```

2. **编写代码**
   - 在 `main.py` 中实现 `calculate_product()` 函数

   - 通过标准输入获取数据

3. **本地测试**
   ```bash

   # 安装测试工具

   pip install pytest

   
   # 运行所有测试

   pytest test_problem2.py -v

   
   # 运行单个测试（示例）
   pytest test_problem2.py::test_normal_case -v

   ```

---

## 输入输出示例

| 输入                    | 输出                      |
|-------------------------|--------------------------|
| `3 5 1 2 3 4`           | 乘积结果为: 24.00        |
| `0 2.5 3.1`             | 乘积结果为: -0.60        |
| `2 1`                   | 输入错误: 应有3个节点... |

---

## 重要提示

✅ **输入处理技巧**  
- 使用 `input().split()` 获取数据后转换为浮点数列表

- 第一个元素转换为整数 `n`
- 第二个元素是 `x`
- 后续元素是 `x0-xn`

🚨 **常见错误排查**  
1. 测试失败时，检查：
   - 输入解析是否正确（注意顺序）
   - 乘积计算是否包含所有因子

   - 浮点数精度问题（使用绝对值误差判断）

2. 出现 `ModuleNotFoundError` 时：
   - 确保文件命名为 `main.py`
   - 确认测试文件与 `main.py` 同级目录

💡 **高级挑战**  
- 尝试用 `math.prod()` 简化计算（Python 3.8+）
- 添加命令行参数支持：`python main.py 3 5 1 2 3 4`

---

## 提交作业

1. 推送修改到GitHub

   ```bash

   git add main.py

   git commit -m "完成题目2"
   git push origin main

   ```
2. 在仓库的 **Actions** 标签页确认测试通过
