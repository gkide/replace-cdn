[declarativeNetRequest]: https://sunnyzhou-1024.github.io/chrome-extension-docs/extensions/declarativeNetRequest.html

# manifest.json  [declarative_net_request](declarativeNetRequest) 配置示例

## 高级玩法

使用时请把 `proxy.domain.com` 更换为你自己的域名
固定替换地址/动态替换地址不能同时使用，否则会产生冲突

- 固定地址替换  fix-redirect.json
- 动态地址替换  dyn-redirect.json
- 内容安全策略  remove-google.json

## manifeset.json 参考 `declarative_net_request` 配置

```json
"declarative_net_request": {
  "rule_resources": [{
    "enabled": true,
    "id": "redirectGoogleId",
    "path": "rules/redirect-google.json"
  }, {
    "enabled": true,
    "id": "removeGoogleId",
    "path": "rules/remove-google.json"
  }, {
    "enabled": true,
    "id": "blockId",
    "path": "rules/dev/block.json"
  }, {
    "enabled": true,
    "id": "dynRedirectId",
    "path": "rules/dev/dyn-redirect.json"
  }]
},
```

## 指定匹配域名

> github.com  -> github-com.proxy.domain.com

```json
{
  "enabled": true,
  "id": "fixRedirectId",
  "path": "rules/dev/fix-redirect.json"
}
```
## 动态匹配域名

> www.google.com -> https://2_www_xn--3px_google_xn--3px_com.proxy.domain.com/

```json
{
  "enabled": true,
  "id": "dynRedirectId",
  "path": "rules/dev/dyn-redirect.json"
}
```
### 阻止指定域名

```json
{
  "enabled": true,
  "id": "blockId",
  "path": "rules/dev/block.json"
}
```