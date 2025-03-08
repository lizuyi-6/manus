
## 安装指南

1. 创建新的 conda 环境：

```bash
conda create -n open_manus python=3.12
conda activate open_manus
```

2. 克隆仓库：

```bash
git clone https://github.com/mannaandpoem/OpenManus.git
cd OpenManus
```

3. 安装依赖：

```bash
pip install -r requirements.txt
```

## 配置说明

OpenManus 需要配置使用的 LLM API，请按以下步骤设置：

1. 在 `config` 目录创建 `config.toml` 文件（可从示例复制）：

```bash
cp config/config.example.toml config/config.toml
```

2. 编辑 `config/config.toml` 添加 API 密钥和自定义设置：

```toml
# 全局 LLM 配置
[llm]
model = "gpt-4o"
base_url = "https://api.openai.com/v1"
api_key = "sk-..."  # 替换为真实 API 密钥
max_tokens = 4096
temperature = 0.0

# 可选特定 LLM 模型配置
[llm.vision]
model = "gpt-4o"
base_url = "https://api.openai.com/v1"
api_key = "sk-..."  # 替换为真实 API 密钥
```

## 快速启动

一行命令运行 OpenManus：

```bash
python main.py
```

然后通过终端输入你的创意！

如需体验开发中版本，可运行：

```bash
python run_flow.py
```

## 发展路线

- [ ] 更优的规划系统
- [ ] 实时演示功能
- [ ] 运行回放
- [ ] 强化学习微调模型
- [ ] 全面的性能基准测试

