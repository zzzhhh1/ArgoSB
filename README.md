## ArgoSB一键无交互代理脚本【当前版本：25.6.5】

### 1、脚本主打极简、轻便的体验，记忆式变量脚本，一次回车随装随用

### 2、使用Sing-box主内核+可选Cloudflared-Argo内核

### 3、支持非root模式，一个脚本兼容主流VPS系统与容器NIX系统

### 4、支持单个或多个代理协议任意组合

### 5、目前支持Vless-reality、Vmess-ws、Hy2、Tuic、Argo临时/固定隧道，其他协议增加中

### 6、如果需要多样的功能，推荐使用VPS专用四合一脚本[sing-box-yg](https://github.com/yonggekkk/sing-box-yg)

----------------------------------------------------------

### 一、自定义变量参数说明：

| 变量意义 | 变量名称| 变量值""设置| 删除变量 | 变量值""留空 | 变量要求 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1、启用vless | vlpt | 端口指定 | 关闭vless | 端口随机 | 必选之一 |
| 2、启用vmess | vmpt | 端口指定 | 关闭vmess | 端口随机 | 必选之一 |
| 3、启用hy2 | hypt | 端口指定 | 关闭hy2 | 端口随机 | 必选之一 |
| 4、启用tuic | tupt | 端口指定 | 关闭tuic | 端口随机 | 必选之一 |
| 5、uuid密码 | uuid | 符合uuid规定格式 | 随机生成 | 随机生成 | 可选 |
| 6、reality域名 | reym | 符合reality域名规定 | yahoo | yahoo | 可选 |
| 7、argo开关 | argo | 填写y | 关闭argo隧道 | 关闭argo隧道 | 可选，填写y时，vmess必须启用变量 |
| 8、argo固定域名 | agn | 解析在CF上的域名 | 使用临时隧道 | 使用临时隧道 | 可选，argo填写y才可激活固定/临时隧道|
| 9、argo token | agk | CF获取的token | 使用临时隧道 | 使用临时隧道 | 可选，argo填写y才可激活固定/临时隧道 |
| 10、切换ipv4或ipv6配置 | ip | 填写4或者6 | 自动识别IP配置 | 自动识别IP配置 | 可选 |

#### 一键脚本模版：
```
vlpt="" vmpt="" hypt="" tupt="" uuid="" reym="" argo="" agn="" agk="" ip="" bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```
注意：变量值填写在""之间，变量之间空一格

#### 三类组合推荐 (端口随机)：

1：全协议共存或者单协议 + Argo临时/固定隧道
```
vlpt="" vmpt="" hypt="" tupt="" argo="y" agn="" agk="" bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

2：仅argo临时隧道，固定隧道必须填写端口(vmpt)、域名(agn)、token(agk)

类似无公网的【IDX Google VPS】容器推荐使用此脚本，快速一键内网穿透获取节点

```
vmpt="" argo="y" agn="" agk="" bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

3：单协议，主流UPD协议或者TCP协议单独运行 (hy2为例)
```
hypt="" bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

---------------------------------------------------------

### 二、相关快捷方式 (首次重连SSH后，agsb快捷方式生效)：

#### 1、查看Argo的固定域名、固定隧道的token、临时域名、当前已安装的节点信息：

```agsb list``` 或者 ```bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh) list```


#### 2、在线切换IPV4/IPV6节点配置 (双栈VPS专享)：

显示IPV4节点配置：

```ip=4 agsb cip```或者```ip=4 bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosbx.sh) cip```

显示IPV6节点配置：

```ip=6 agsb cip```或者```ip=6 bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosbx.sh) cip```

#### 3、卸载脚本：

```agsb del``` 或者 ```bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh) del```

----------------------------------------------------------


#### 相关教程可参考甬哥博客，视频教程如下：

最新推荐：[Claw.cloud免费VPS搭建代理最终教程（二）：最低仅需2美分；支持Argo | Reality | Vmess | Hysteria2 | Tuic代理协议任意组合](https://youtu.be/NnuMgnJqon8)

[Claw.cloud免费VPS搭建代理最终教程（一）：全网最简单 | 两大无交互回车脚本 | 套CDN优选IP | workers反代 | ArgoSB隧道搭建](https://youtu.be/Esofirx8xrE)

[IDX Google免费VPS代理搭建教程（二）：ArgoSB一键代理脚本发布 | 一次回车搞定一切 | 懒人小白最强Argo代理节点脚本](https://youtu.be/OoXJ_jxoEyY)

[IDX Google免费VPS代理搭建教程（三）：NIX容器最新工作区方式搭建Argo免费节点 | 一次回车搞定一切 | Argo固定隧道一键复活](https://youtu.be/0I5eI1KKx08)

[IDX Google免费VPS代理搭建教程（四）：支持重置后自动启动代理节点功能 | 最简单的保活方法](https://youtu.be/EGrz6Wvevqc)

更新中……

----------------------------------------------------------

### 交流平台：[甬哥博客地址](https://ygkkk.blogspot.com)、[甬哥YouTube频道](https://www.youtube.com/@ygkkk)、[甬哥TG电报群组](https://t.me/+jZHc6-A-1QQ5ZGVl)、[甬哥TG电报频道](https://t.me/+DkC9ZZUgEFQzMTZl)

----------------------------------------------------------
### 感谢支持！微信打赏甬哥侃侃侃ygkkk
![41440820a366deeb8109db5610313a1](https://github.com/user-attachments/assets/e5b1f2c0-bd2c-4b8f-8cda-034d3c8ef73f)

----------------------------------------------------------
### 感谢你右上角的star🌟
[![Stargazers over time](https://starchart.cc/yonggekkk/ArgoSB.svg)](https://starchart.cc/yonggekkk/ArgoSB)

----------------------------------------------------------

### Thanks to [VTEXS](https://console.vtexs.com/?affid=1558) for the sponsorship support

