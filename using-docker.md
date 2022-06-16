```
sudo apt -y update
```

```
sudo apt -y install openssl
sudo apt -y install zip
sudo apt -y install tree
```

## Install Docker
```
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
sudo usermod -aG docker $USER
exit
```

## Install Hadoop
- Visit: https://www.cloudera.com/downloads/hortonworks-sandbox.html
- Install Guide: https://www.cloudera.com/tutorials/sandbox-deployment-and-install-guide/3.html
- Download Docker based setup:
```
wget https://archive.cloudera.com/hwx-sandbox/hdp/hdp-2.6.5/HDP_2.6.5_deploy-scripts_180624d542a25.zip
```
- For passwords: https://www.cloudera.com/tutorials/learning-the-ropes-of-the-hdp-sandbox.html
- Unzip
```
unzip HDP_2.6.5_deploy-scripts_180624d542a25.zip
```
- Install Hadoop
```
bash docker-deploy-hdp265.sh
```

- Check hadoop:
```
curl localhost:1080
curl localhost:8080
curl localhost:8080
```


### Reset admin password:
- Login to vmhadoop.eastus2.cloudapp.azure.com:4200
- Reset password using below command
```
ambari-admin-password-reset
```
