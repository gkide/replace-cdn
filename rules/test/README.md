# 测试验证

## 禁止访问百度首页

```json
// 修改 `manifest.json` 文件
"declarative_net_request": {
  "rule_resources": [{
      "enabled": true,
      "id": "TestIdBlockBaidu",
      "path": "rules/test/block-baidu.json"
    }
  ]
}
```

## 修改 Request Headers 部分

- 启用后，Chrome访问 `https://example.com/`
- 打开控制台，Network标签，选择All，点击 example.com
- 查看其 Request Headers 部分，找到 x-replacecdn-token
- 标签及其值，验证其与 modify-header.json 设置内容是否一致


```json
// 修改 `manifest.json` 文件
"declarative_net_request": {
  "rule_resources": [{
      "enabled": true,
      "id": "TestIdModifyHeader",
      "path": "rules/test/modify-header.json"
    }
  ]
}
```

## 正则匹配

- 启用后，Chrome访问
- https://www.example.com/

```json
// 修改 `manifest.json` 文件
"declarative_net_request": {
  "rule_resources": [{
      "enabled": true,
      "id": "TestIdRedirect",
      "path": "test/v3/rules/redirect.json"
    }
  ]
}
```