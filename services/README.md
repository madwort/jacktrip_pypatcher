# copy and set permissions for service and config files

```bash
sudo cp services/jackd.service /etc/systemd/system/
sudo chmod 644 /etc/systemd/system/jackd.service
sudo chmod u+x /etc/systemd/system/jackd.service
sudo mkdir /etc/jacktrip_pypatcher
sudo cp services/config/jackd.conf /etc/jacktrip_pypatcher/jackd.conf
systemctl daemon-reload
```

# start jackd and jacktrip services (which also starts all dependencies) and icecast2

```bash
$ sudo systemctl start jackd.service
$ sudo systemctl start jacktrip.service
$ sudo systemctl start icecast2.service
```

# enable all services

```bash
$ sudo systemctl enable jackd.service
$ sudo systemctl enable jacktrip.service
$ sudo systemctl enable mpg123.service
$ sudo systemctl enable pypatcher_darkice.service
$ sudo systemctl enable pypatcher_callback.service
$ sudo systemctl enable pypatcher_watchgod.service
$ sudo systemctl enable icecast2.service
```
