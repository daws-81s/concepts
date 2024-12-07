# Prometheus

Reference: https://prometheus.io/download/

* move to /opt directory
```
wget https://github.com/prometheus/prometheus/releases/download/v3.0.1/prometheus-3.0.1.linux-amd64.tar.gz
```

* Extract tar file
```
tar -xf prometheus-3.0.1.linux-amd64.tar.gz
```

* Rename if required

```
mv prometheus-3.0.1.linux-amd64 prometheus
```

* Create systemctl service
```
vim /etc/systemd/system/prometheus.service
```

* Enter below info
```
[Unit]
Description=Prometheus Server

[Service]
ExecStart=/opt/prometheus/prometheus --config.file=/opt/prometheus/prometheus.yml

[Install]
WantedBy=multi-user.target
```

```
systemctl start prometheus
```
```
systemctl enable prometheus
```




