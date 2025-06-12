# EtherSentinel - 区块链安全监控系统

EtherSentinel是一个功能强大的区块链安全监控系统，用于检测和评估区块链交易和地址的潜在风险。

## 功能特点

- 交易甄别：实时检测交易风险，防范欺诈和恶意行为
- 地址检测：分析区块链地址的历史行为和交易模式，评估风险等级
- 代码生成：智能合约代码解析和重构安全配置
- 实时数据：区块链交易的全面统计和数据分析

## 安装说明

### 前提条件

- Python 3.7+
- Node.js (可选，仅用于开发)

### 安装步骤

1. 克隆仓库
```bash
git clone https://github.com/yourusername/EtherSentinel.git
cd EtherSentinel
```

2. 安装Python依赖
```bash
pip install -r requirements.txt
```

## 使用方法

### 启动服务器

```bash
python app.py
```

服务器将在 http://localhost:5000 启动

### 使用Web界面

打开浏览器访问 http://localhost:5000 即可使用Web界面：

1. 交易甄别：输入交易哈希，检测交易风险
2. 地址检测：输入区块链地址，评估地址风险
3. 代码生成：解析智能合约代码，识别潜在风险
4. 实时数据：查看区块链交易的实时统计数据

## API文档

### 检查地址风险

```
POST /api/check_address_risk
```

请求参数：
```json
{
  "address": "0x..."
}
```

响应示例：
```json
{
  "address": "0x...",
  "risks": ["钓鱼活动", "黑名单地址"],
  "addressInfo": {
    "balance": "0.5432",
    "value": "$2115.98 (@ $3892.64/ETH)",
    "lastTxn": "...",
    "firstTxn": "..."
  },
  "riskLevel": "高风险",
  "riskDetails": {
    "钓鱼活动": {
      "title": "钓鱼活动风险",
      "description": "...",
      "recommendations": ["...", "..."],
      "severity": "高"
    }
  }
}
```

### 检查交易风险

```
POST /api/check_transaction_risk
```

请求参数：
```json
{
  "txHash": "0x..."
}
```

响应示例：
```json
{
  "txHash": "0x...",
  "status": "success",
  "isSafe": true,
  "risks": [],
  "timestamp": "2023-05-23T10:30:15.123Z"
}
```

## 许可证

MIT

## 联系方式

如有任何问题或建议，请联系：xrose0431@gmail.com 