# PROGRESS — 学习进度总文档

> 任何新设备 / 新会话接手时，**先读这个文件**，再读对应阶段的 notes 和代码。

## 当前状态

- **当前阶段**：阶段 0 — mini 自动微分引擎
- **进度**：知识点已讲解（见 `notes/01-backpropagation.md`），代码**尚未开始**
- **下一步**：实现 `tinyllm/tensor.py` 中的 `Tensor` 类，支持 `+` 和 `*` 两个操作的前向与反向传播，让下面这段代码跑通：

```python
x = Tensor(3.0)
y = Tensor(4.0)
loss = x * y + 1
loss.backward()
assert x.grad == 4.0 and y.grad == 3.0
```

## 路线图与完成度

| 阶段 | 内容 | 状态 | 笔记 | 代码 |
|------|------|------|------|------|
| 0 | mini 自动微分引擎 | 🔵 进行中（讲解完成，未写码） | [01-backpropagation](notes/01-backpropagation.md) | `tinyllm/tensor.py`（待创建） |
| 1 | BPE Tokenizer | ⚪ 未开始 | — | `tinyllm/tokenizer.py`（待创建） |
| 2 | GPT 模型 | ⚪ 未开始 | — | `tinyllm/model.py`（待创建） |
| 3 | 训练循环 | ⚪ 未开始 | — | `tinyllm/train.py`（待创建） |
| 4 | 进阶（RoPE / KV Cache / 采样…） | ⚪ 未开始 | — | — |

## 学习者背景（影响讲解方式）

- AI 领域初学者，讲解需要**简洁易懂，多举例、多配代码**，少用术语，用了术语要当场解释
- 偏好"先讲一个核心原理 → 立刻动手实现"的节奏
- 用中文交流

## 工作方式约定

1. 每个阶段遵循流程：**讲解原理（写入 notes/）→ 实现代码 → 跑验证 → 更新本文档 → commit**
2. 每写完一个组件都要能跑起来验证（gradient checking、对照 PyTorch 输出等）
3. notes 按 `编号-主题.md` 命名，编号与讲解顺序一致
4. 每次取得进展就更新本文档的"当前状态"和路线图表格，并 commit + push

## 更新日志

- **2026-10-12**：仓库初始化；完成反向传播核心原理讲解（notes/01）。
