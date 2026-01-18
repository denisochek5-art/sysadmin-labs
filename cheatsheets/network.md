dig example.com
nslookup example.com
getent hosts example.com
Resolve-DnsName example.com
nslookup example.com
ipconfig /displaydns
ip a
cat /etc/resolv.conf
ip a
cat /etc/resolv.conf
ipconfig /all
ipconfig /release
ipconfig /renew
ss -tulpn
sudo lsof -i -P -n | head
nc -vz 1.1.1.1 53
curl -I http://example.com
Get-NetTCPConnection | Select -First 20
Test-NetConnection 1.1.1.1 -Port 53
netstat -ano
traceroute 8.8.8.8
tracert 8.8.8.8
