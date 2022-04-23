# Chrome `manifest.json` V3 技术文档

[declarativeNetRequest]: https://sunnyzhou-1024.github.io/chrome-extension-docs/extensions/declarativeNetRequest.html
- [declarative_net_request](declarativeNetRequest)
- [RE2 Syntax](https://github.com/google/re2/wiki/Syntax)


## `host_permissions` 配置方式

```json
{
  "host_permissions": [ // 指定地址
    "*://ajax.googleapis.com/*",
    "*://fonts.googleapis.com/*",
    "*://themes.googleusercontent.com/*",
    "*://fonts.gstatic.com/*",
    "*://ssl.gstatic.com/*",
    "*://www.gstatic.com/*",
    "*://secure.gravatar.com/*",
    "*://maxcdn.bootstrapcdn.com/*",
  ],
  "host_permissions": [ // 通配符匹配
    "*://*.google.com/*",
    "*://*/*",
    "<all_urls>"
  ]
}
```

## 国内公共CDN
- CDN公共库 [BootCDN](https://www.bootcdn.cn/)
- CDN公共库 [字节跳动](http://cdn.bytedance.com/)
- CDN公共库 [新浪](http://lib.sinaapp.com/)
- CDN公共库 [360](https://cdn.baomitu.com/)

## 国外公共CDN
- CDN公共库 [CDNJS](https://cdnjs.com/)
- CDN公共库 [jsDelivr](https://www.jsdelivr.com/)
- CDN公共库 [Microsoft ASP.net](https://docs.microsoft.com/en-us/aspnet/ajax/cdn/overview)