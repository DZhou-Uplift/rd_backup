# rd_backup
Backup procedure listed here.

Method using Snapshots and AMI:

1. Create AMI from snapshot of redash instance (one with no problems)
2. Launch instance from AMI, make sure to use correct security settings (launch-wizard-7 works)
3. Once instance has been started, ssh into instance and run the following commands:

sudo apt-get update
cd /opt/redash
sudo docker-compose start

4. Redash should be up and running now. Point browser to http://<Public DNS>/redash to get to login screen.
  The users should be saved and can login as usual now.
  

Snapshots should be taken everytime a new 'version' is created as well as every day or so. 
