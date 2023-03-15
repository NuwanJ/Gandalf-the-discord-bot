<!-- https://medium.com/codex/setup-a-python-script-as-a-service-through-systemctl-systemd-f0cc55a42267 -->

<!-- sudo nano /etc/systemd/system/gandalf-bot.service -->

```
[Unit]
Description=Gandalf-Bot service
After=multi-user.target
[Service]
Type=simple
Restart=always
ExecStart=/usr/bin/python3 -m /home/nuwan/bots/Gandalf-the-discord-bot/src.main
[Install]
WantedBy=multi-user.target
```

```
sudo systemctl daemon-reload
sudo systemctl enable gandalf-bot.service
sudo systemctl start gandalf-bot.service

sudo systemctl status gandalf-bot.service
```