# tinyllm

从零开始手写一个大语言模型训练框架，在实现中学习 LLM 训练的原理。

## 这是什么

这是一个学习项目：不用现成的高级 API，从最基础的自动微分开始，一步步实现
Tokenizer → GPT 模型 → 训练循环 → 推理生成，最终能在小语料上训练出一个
可以生成文本的小模型。

## 仓库结构

```
├── PROGRESS.md     # 进度总文档：做到哪了、下一步是什么（新设备接手先看这里）
├── AGENTS.md       # 给 AI agent 的接手指引（CLAUDE.md 指向这里）
├── notes/          # 每个阶段的知识点讲解（按编号顺序）
└── tinyllm/        # 框架代码本体
```

## 学习路线图

- [ ] **阶段 0**：mini 自动微分引擎（Tensor + 反向传播）
- [ ] **阶段 1**：BPE Tokenizer
- [ ] **阶段 2**：GPT 模型（Attention / MLP / LayerNorm / 残差）
- [ ] **阶段 3**：训练循环（loss、AdamW、学习率调度）
- [ ] **阶段 4**：进阶（RoPE、KV Cache、采样策略、分布式等）

当前进度详见 [PROGRESS.md](PROGRESS.md)。
