```
1. pertama buat script .sh untuk backup lalu masukan scipt tersebut ke cronjob untuk menjadwalkan backup secara otomatis.
2. install aws di ubuntu
3. aws configure
4. buat bucket di s3 untuk meyimpan file dump dari RDS
5. buat lifecycle rule untuk menghapus file setelah 7 hari

#!/bin/bash

mysqldump -h database-1.cxwy2y2my8cl.us-east-1.rds.amazonaws.com -u admin --password=UPsila210#$ my_db > my_db-date '+%Y-%m-%d-%H:%M'.sql

aws s3 cp /home/ubuntu/my_db* s3://my-datas/backup/

```
<img src="https://raw.githubusercontent.com/AbelJasen15/RDS---S3-Simple-Backup-Script/main/Screenshot%202024-06-21%20160524.png"/>
 
<img src="https://raw.githubusercontent.com/AbelJasen15/RDS---S3-Simple-Backup-Script/RDS---S3-Simple-Backup-Script/Screenshot%202024-06-21%20184056.png"/>
