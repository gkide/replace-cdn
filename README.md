# Replace CDN

[![](https://img.shields.io/github/issues/gkide/ReplaceCDN.svg)](https://github.com/gkide/ReplaceCDN/issues)
[![](https://img.shields.io/github/release/gkide/ReplaceCDN.svg)](https://github.com/gkide/ReplaceCDN/releases)

- 将 Google CDN 替换为国内可以访问的 CDN

## 缘起

> 由于众所周知的原因，Google 在国内被完全屏蔽，无法正常访问，其提供的前端公共服务接口也无法访问。
> 国外大量技术网站使用了Google的前端公共服务接口，国内访问时会变的奇慢无比！
> 例如，当以下资源无法加载时，整个网页不能正常访问！
> - http://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js
> - http://ajax.googleapis.com/ajax/libs/angularjs/1.2.13/angular.js

## 原理

- `ajax.googleapis.com` - 前端公共库
  * 替换为 `ajax.loli.net`
- `fonts.googleapis.com` - 免费字体库
  * 替换为 `fonts.loli.net`
- `themes.googleusercontent.com` - fonts 可能使用的主题资源
  * 替换为 `themes.loli.net`
- `fonts.gstatic.com` - 免费字体库
  * 替换为 `gstatic.loli.net`
- `www.google.com/recaptcha` - Google 图像验证库
  * 替换为 `www.recaptcha.net/recaptcha`
- `secure.gravatar.com` - gravatar 头像
  * 替换为 `gravatar.loli.net`
- `maxcdn.bootstrapcdn.com/bootstrap` - bootstrap 框架使用的 CDN
  * 替换为 `cdn.bootcdn.net/ajax/libs/twitter-bootstrap`

### 手动安装

> 1. 克隆 [ReplaceCDN](https://github.com/gkide/ReplaceCDN)
> 2. 打开 Chrome，输入: `chrome://extensions/`
> 3. 勾选 Developer Mode
> 4. 选择 Load unpacked extension... 然后定位到 `ReplaceCDN` 目录，确定
> 5. 安装完毕，去掉 Developer Mode 勾选