### ArgoSB真一键无交互脚本：最新sing-box内核+最新Cloudflared-Argo内核

#### 支持Argo临时隧道、固定隧道，为Google IDX VPS专门设计，其他VPS也可安装

#### 脚本仅VMESS协议，聚合分享可输出13端口节点及对应的优选不死IP全覆盖（包含两个IPV6）：7个关tls 80系端口节点、6个开tls 443系端口节点

#### 脚本如下，默认安装为Argo临时隧道
```
bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```
或者
```
bash <(curl -Ls https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

卸载脚本：
```
bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh) del
```

### 可自定义设置：

1、查看argo固定域名、固定域名token、临时域名：
```
bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh) agn
```

2、Argo临时隧道自定义UUID:
```
uuid=你的uuid bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

3、Argo临时隧道自定义主协议vmess端口
```
vmpt=vps可使用的端口 bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

4、Argo固定隧道 (脚本前必须要有端口、固定域名、token三个变量，uuid可选)：
```
vmpt=VPS可使用的端口 agn=固定域名 agk=token bash <(wget -qO- https://raw.githubusercontent.com/yonggekkk/argosb/main/argosb.sh)
```

