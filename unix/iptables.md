A RH-Firewall-1-INPUT -p udp -m tcp --dport 80 -j ACCEPT
A RH-Firewall-1-INPUT -p tcp -m tcp --dport 443 -j ACCEPT

 /etc/sysconfig/iptables