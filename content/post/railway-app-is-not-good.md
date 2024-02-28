+++
title = 'Railway App很不靠谱'
date = 2024-02-27T19:32:16-08:00
draft = false
+++

我去年某个时间发现了一个新的 SaaS 服务，[Railwail.app](https://railway.app)，猛一看，确实挺不错的，你自己写好了代码，直接 push 到 github 上， 然后连上他们的服务，就自动帮你部署了。

但为何我觉得这货不行呢？

首先，我有一个小型的 php 项目，需要在本地创建一个 cache 目录，里面是一些 log 和模板文件编译后的文件。这不是很正常的么？Laravel 也会在根目录下写入一些临时文件。但 Railway 死活不给权限，报错，就是没权限。我把同样代码传到 digitalocean，可以跑起来；在本地能跑起来；我把所有代码做成一个 docker，然后把代码 COPY 到容器内，我心想，容器内的目录下写入文件，这你 Railway 总管不着了吧？结果也还是报错，没有权限。

其次，我想把[https://ossk.cc](https://ossk.cc)的反向代理功能放在 Railway。其实本来已经在我自己的服务器搞好了，我又折腾到 Railway。然后好巧不巧，我在推特上看到有个人把服务部署到[Netlify](https://netlify.com)，结果被刷了流量，要支付 1 万多美元的流量费，然后他和 Netlify 墨迹半天，还是要交五千多刀。然后我就立刻跑去看 Railway 的流量是怎么计费的。结果一看，0.1 美元/GB。我吓死了，立刻又把[https://ossk.cc](https://ossk.cc)的反向代理挪回到自己的小鸡里了。

Railway 不靠谱！不能用！
