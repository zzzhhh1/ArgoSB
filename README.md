### ArgoSB真一键无交互脚本：最新sing-box内核+最新Cloudflared-Argo内核

#### 目前仅支持Argo临时域名，为Google IDX VPS专门设计，其他VPS也可安装

#### 脚本仅VMESS协议，输出13个端口及不死IP全覆盖（包含两个IPV6）：7个关tls 80系端口节点、6个开tls 443系端口节点

#### 脚本如下：
```
bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```
或者
```
bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

### 可自定义设置：

1、卸载脚本：
```
bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh) del
```

2、查看argo临时域名：
```
bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh) agn
```

3、自定义UUID:
```
uuid=你的uuid bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

4、自定义主协议vmess端口
```
vmpt=vps可使用的端口 bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

更新中……………………
