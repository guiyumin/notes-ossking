+++
title = 'Cloudflare五秒盾不能和它的Turnstile一起用'
date = 2024-02-19T11:22:03-08:00
draft = false
+++

这个`uder attack mode`，也就是所谓`五秒盾`，不能和它自己的`Turnstile`一起用，因为这个`Turnstile`会自动发送一个`POST`请求，而这个`POST`请求，会导致页面发生`405`错误，或者页面空白。

网上一搜就发现很多人在讨论这个问题。

但后来我把`Turnstile`删了，因为有了五秒盾，就不需要这个`Turnstile`了，可以不用同时使用这俩服务。但五秒盾也是有办法绕过的，网上有公司宣称可以绕过五秒盾，从而更快的爬取网页。

先这样吧，我这网站还没到那个程度。

### 2024.2.20 更新

今天突然发现，即便去掉了`Turnstile`，还是会出现 405 错误，所以干脆又把`Turnstile`加回来，然后把`uder attack mode`去掉了。如果真的遭到攻击了，再用这个`uder attack mode`也不迟。
