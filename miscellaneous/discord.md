## Error sharing entire screen: black screen

1. sudo nano /etc/gdm3/custom.conf
2. Uncomment #WaylandEnable=false
3. sudo dpkg-reconfigure gdm3
4. Reboot
