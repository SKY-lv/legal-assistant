# Legal Assistant Agent Skill

> AI-powered legal document analysis and contract review

## 功能

- **合同审查** - 风险条款识别、修改建议
- **法律咨询** - 常见法律问题解答
- **法规检索** - 法律法规数据库搜索
- **文书生成** - 起诉状、合同、协议模板
- **案例分析** - 类似案例检索分析

## 使用场景

```
用户: 帮我审查这份劳动合同有没有问题
Agent: [调用legal-assistant skill分析合同，标注风险条款]
```

## 工具函数

### `review_contract(contract_text)`

合同审查。

```python
{
    "risks": [
        {
            "clause": "第5条：加班不支付加班费",
            "risk_level": "high",
            "issue": "违反劳动法规定",
            "suggestion": "修改为：加班按法律规定支付加班费"
        }
    ],
    "compliance_score": 65
}
```

### `search_regulations(query)`

法规检索。

### `generate_legal_document(type, params)`

文书生成。

### `find_similar_cases(case_description)`

案例检索。

## 配置

```json
{
    "jurisdiction": "CN",
    "databases": ["law", "regulation", "case"],
    "language": "zh"
}
```

## 安装

```bash
clawhub install SKY-lv/legal-assistant
```

## License

MIT
