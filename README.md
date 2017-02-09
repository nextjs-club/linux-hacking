# 配置iptables,把80端口转到8080
iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 8080

service iptables save
