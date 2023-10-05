# PostgreSQL-Schedule-Backup
Using Crontab we will schedule our PostgreSQL Backup,Here is the corontab file command thath we can schedule our backup
* Step 1: Open pg_hba.conf file which is located in /etc/postgresql/14/main/pg_hba.conf here 14 is postgresql version.
Put the database and database username.
* Check the Screenshot file

      vi /etc/postgresql/14/main/pg_hba.conf
* Step 2: Open Crontab file iam using vi editor

      vi /etc/crontab
* Then copy the line below and paste it to the end of the corntab file then save and exit.
   
      * 0 * * * root PGPASSWORD=ibos@123 pg_dump -U ibos -d PGDB -f /var/opt/backup/PGDB_$(date +\%Y\%m\%d).backup
  
