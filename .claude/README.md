# MCP 配置说明

## Hive Intelligence MCP 服务器

此项目已配置 Hive Intelligence MCP 服务器，用于加密货币链上数据分析。

### 配置文件

- `.claude/mcp.json` - MCP服务器配置

### Hive Intelligence MCP

**服务器URL**: `https://hiveintelligence.xyz/mcp`

Hive Intelligence 提供加密货币数据分析功能，包括：
- 链上数据查询
- 交易所流入流出分析
- 市场数据获取
- 技术指标计算

### 使用方法

1. 确保 Claude Code 已正确安装并配置
2. MCP 配置文件已自动加载
3. 在对话中可以直接使用 Hive Intelligence 提供的工具

### 环境变量（如需要）

如果 Hive Intelligence MCP 需要认证，请在项目根目录创建 `.env` 文件：

```bash
HIVE_INTELLIGENCE_API_KEY=your_api_key_here
```

### 验证配置

重启 Claude Code 后，MCP 服务器应该会自动连接。您可以通过以下方式验证：

1. 在 Claude Code 中询问可用的工具
2. 尝试调用 Hive Intelligence 相关功能

### 故障排除

如果连接失败：
1. 检查网络连接
2. 确认 URL 是否正确
3. 检查是否需要 API 密钥
4. 查看 Claude Code 日志获取详细错误信息
