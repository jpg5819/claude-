# 🚀 快速启动指南

## Hive Intelligence MCP - 加密货币数据分析

### ⚡ 一分钟开始使用

#### 1. 启动 Claude Code Research Preview

```bash
claude-code
```

#### 2. 验证 MCP 已连接

在 Claude Code 中输入：

```
有哪些可用的工具？
```

您应该能看到 **Hive Intelligence** 相关的工具。

#### 3. 开始分析

直接在 Claude Code 中请求：

```
使用 Hive Intelligence 分析 BTC 最近 7 天的交易所流入流出数据
```

### 📋 配置说明

**MCP 配置已自动设置**，您无需手动配置！

- **用户级配置**: `~/.config/claude/mcp_settings.json`
- **项目级配置**: `.claude/mcp.json`

### 🎯 使用示例

#### 基础数据查询

```
查询 ETH 的最新价格和交易量
```

#### 深度分析（结合项目分析框架）

```
根据 crypto_analysis_prompt_fixed2.md 中定义的分析框架，
分析 BTC 最近 14 天的数据，并给出交易建议
```

#### 多币种对比

```
对比 BTC、ETH、SOL 最近 7 天的交易所净流入情况
```

### 📁 项目文件

- **分析框架**:
  - `crypto_analysis_prompt_fixed2.md` - 修正版框架
  - `crypto_analysis_prompt_optimized最新版.md` - 最新优化版

- **配置文件**:
  - `.claude/mcp.json` - MCP 服务器配置
  - `.claude/README.md` - 详细文档

### 🔑 API 密钥（可选）

如果 Hive Intelligence 需要 API 密钥：

```bash
# 1. 复制模板
cp .env.example .env

# 2. 编辑 .env 文件，添加您的 API 密钥
# HIVE_INTELLIGENCE_API_KEY=your_key_here

# 3. 重启 Claude Code
```

### ❓ 遇到问题？

#### MCP 未连接

1. 确认 Claude Code Research Preview 已安装
2. 检查网络连接
3. 查看详细文档：`.claude/README.md`

#### 需要帮助

```bash
# 查看完整文档
cat .claude/README.md
```

### 🎉 就这么简单！

配置已全部完成，现在就可以开始使用 Hive Intelligence 进行加密货币数据分析了！

---

**配置完成时间**: 2024-11-14
**服务器**: https://hiveintelligence.xyz/mcp
