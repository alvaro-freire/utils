## [DISCORD] Error sharing entire screen: black screen (Ubuntu)

- Run this command to edit `/etc/gdm3/custom.conf` file.

```sh
sudo nano /etc/gdm3/custom.conf
```

> Note: I used `nano`, but you can use the text editor you want :)

- Uncomment #WaylandEnable=false

> Uncomment by removing `#`

- Run this command to reconfigure your display manager

```sh 
sudo dpkg-reconfigure gdm3
```

- Reboot

That's it! You can now share your entire screen.
