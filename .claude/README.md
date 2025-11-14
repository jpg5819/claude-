# Hive Intelligence MCP 配置指南

## 🚀 快速开始

### Claude Code Research Preview 自动加载配置

此项目已完整配置 Hive Intelligence MCP 服务器，启动 Claude Code Research preview 即可直接使用。

## 📁 配置文件位置

### 方式一：用户级别配置（推荐）
**位置**: `~/.config/claude/mcp_settings.json`

所有项目都可以使用此配置，启动 Claude Code 即自动加载。

### 方式二：项目级别配置
**位置**: `.claude/mcp.json`

仅当前项目使用，适合项目特定的 MCP 配置。

## 🔧 MCP 服务器配置

### Hive Intelligence

```json
{
  "mcpServers": {
    "hive-intelligence": {
      "url": "https://hiveintelligence.xyz/mcp",
      "transport": "sse",
      "description": "加密货币链上数据分析服务"
    }
  }
}
```

**服务功能**：
- ✅ 链上数据查询
- ✅ 交易所流入流出分析
- ✅ 市场数据获取
- ✅ 技术指标计算

## 📖 使用方法

### 1. 启动 Claude Code

```bash
# 直接启动 Claude Code Research preview
claude-code
```

MCP 服务器会自动连接和加载。

### 2. 验证 MCP 连接

在 Claude Code 中询问：

```
你现在可以使用哪些工具？
```

或

```
列出所有可用的 MCP 服务器
```

### 3. 使用示例

#### 加密货币数据分析

```
请使用 Hive Intelligence 分析 BTC 最近 7 天的交易所流入流出数据
```

#### 结合项目分析框架

项目中已包含两个专业的分析提示词文件：
- `crypto_analysis_prompt_fixed2.md` - 修正版分析框架
- `crypto_analysis_prompt_optimized最新版.md` - 最新优化版

可以直接引用这些框架进行分析：

```
根据 crypto_analysis_prompt_fixed2.md 中的框架，分析 ETH 14 天数据
```

## 🔑 API 密钥配置（如需要）

如果 Hive Intelligence 需要认证：

### 1. 创建环境变量文件

```bash
cp .env.example .env
```

### 2. 编辑 .env 文件

```bash
HIVE_INTELLIGENCE_API_KEY=your_api_key_here
```

### 3. 重启 Claude Code

```bash
# 重启以加载新的环境变量
```

## 🗂️ 项目文件结构

```
claude-/
├── .claude/
│   ├── mcp.json              # 项目级 MCP 配置
│   └── README.md             # 本文档
├── .env.example              # 环境变量模板
├── .gitignore                # Git 忽略配置
├── crypto_analysis_prompt_fixed2.md           # 分析框架（修正版）
├── crypto_analysis_prompt_optimized最新版.md  # 分析框架（最新版）
├── *.pdf                     # 参考文档
└── *.drawio                  # 流程图
```

## ✅ 验证清单

使用前请确认：

- [ ] Claude Code Research preview 已安装
- [ ] MCP 配置文件已创建（用户级或项目级）
- [ ] 网络连接正常，可访问 https://hiveintelligence.xyz
- [ ] 如需认证，API 密钥已配置
- [ ] Claude Code 已重启以加载配置

## 🛠️ 故障排除

### MCP 服务器未连接

**问题**：Claude Code 启动后看不到 Hive Intelligence 工具

**解决方案**：
1. 检查配置文件位置是否正确
2. 验证 JSON 格式是否有效
3. 查看 Claude Code 日志：
   ```bash
   # 查看日志文件（位置可能因系统而异）
   tail -f ~/.claude/logs/mcp.log
   ```

### 连接超时

**问题**：MCP 服务器连接超时

**解决方案**：
1. 检查网络连接
2. 验证 URL 是否正确：`https://hiveintelligence.xyz/mcp`
3. 尝试在浏览器中访问该 URL
4. 检查防火墙设置

### 认证失败

**问题**：API 密钥认证失败

**解决方案**：
1. 确认 `.env` 文件在项目根目录
2. 验证 API 密钥格式正确
3. 确保 `.env` 未被 `.gitignore` 排除（应该被排除）
4. 重启 Claude Code

## 🔄 更新配置

如需修改配置：

### 用户级配置
```bash
nano ~/.config/claude/mcp_settings.json
```

### 项目级配置
```bash
nano .claude/mcp.json
```

修改后重启 Claude Code 生效。

## 📚 相关资源

- [Claude Code 文档](https://docs.anthropic.com/claude/docs)
- [MCP 协议说明](https://modelcontextprotocol.io/)
- Hive Intelligence 官网：https://hiveintelligence.xyz

## 💡 使用技巧

1. **自动分析**：结合项目中的分析提示词文件，可以快速执行标准化分析
2. **批量查询**：可以同时请求多个币种的数据分析
3. **历史对比**：可以要求 AI 对比不同时间段的数据
4. **自定义报告**：基于分析框架自定义输出格式

## 🎯 下一步

配置完成后，您可以：

1. 在 Claude Code 中测试 Hive Intelligence 连接
2. 尝试分析您感兴趣的加密货币
3. 根据需要调整分析提示词框架
4. 将分析结果导出或保存

---

**最后更新**：2024-11-14
**维护者**：项目团队
