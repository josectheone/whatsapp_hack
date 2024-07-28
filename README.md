This program is for Educational purpose ONLY. Do not use it without permission. I am not responsible for any of your actions. Use this tool with caution.

Note: updated hotspot using nmcli instead of the outdated hotspotd

- Step 1: Run hotspotd with these steps:
```
sudo nmcli device wifi hotspot con-name t-450 ssid t-450 band bg password <password_here>
```

- Step 2: Run the following commands:
```
 echo 1 > /proc/sys/net/ipv4/ip_forward
 iptables -t nat -I POSTROUTING -j MASQUERADE
```

- Step 3: Start the PoC script (below) on attacker machine which is now acting as a router for attacker phone
- Step 4: Call any whatsapp user randomly to capture the server IP addresses to filter
- Step 5: Call victim on his whatsapp
- Step 6: Disconnect the call once established
- Step 7: Script will reveal the public IP address of the target
