Kubernetes Transform Logs to the Graylog
#### after run docker-compose on all nodes we must ship the log to it we can use filebeat and install on each nodes
```
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -

echo "deb https://artifacts.elastic.co/packages/8.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-8.x.list

apt-get update && sudo apt-get install filebeat

systemctl enable filebeat

systemctl start filebeat

cp filebeat.yml /etc/filebeat/filebeat.yml

systemctl restart filebeat 
```

