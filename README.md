foolish-list
============

过滤出的垃圾评论的IP列表

```
 总条数          |  1635       
-----------------+----------------------
 最后更新        |  2014-10-01 07:52:54     
```

### usage

将IP列表增加到防火墙里

```bash
cd foolish-list
cat ips.txt | while IDF= read -r ip; do /sbin/iptables -I INPUT -s "$ip" -j DROP; done
service iptables save
```
