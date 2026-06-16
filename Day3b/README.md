# Day 3b

## Objective

The objective of this lab was to learn how to automate tasks using Bash scripts and cron jobs.
I also learned how to install and configure additional server services such as Docker, MariaDB and Syslog on Ubuntu.

---

## Bash Backup Script and Cron Jobs

### What I Did

For this activity, I created test files and folders inside the Documents directory. I then created a Bash script called `testscript` that copies files from the Documents folder to a backup folder.

After that, I modified the script so that it creates a ZIP archive with the current date as the filename. I gave the script execute permission and moved it to `/usr/bin` so that it could be executed from any directory.

Finally, I edited the crontab file and added a cron job to run the backup script automatically every hour.

### Commands Used

bash
chmod 777 testscript

sudo mv testscript /usr/bin/

sudo nano /etc/crontab


## Docker

### What I Did

I installed Docker on Ubuntu and started the Docker service. 
I also verified that Docker was installed successfully by checking the version and running the Hello World container.

### Commands

bash
sudo apt install docker.io -y

sudo systemctl start docker

sudo systemctl enable docker

docker --version

sudo docker run hello-world



## MariaDB

### What I Did

I installed MariaDB and started the service. I checked the version using `mysql --version` and logged into MariaDB using `sudo mysql`.

Inside MariaDB, I ran:

sql
SHOW DATABASES;


The command displayed the default databases, which confirmed that MariaDB was installed and working correctly.

I also attempted to run `mysql_secure_installation`, but the command was not available in my environment.
However, MariaDB was running successfully and I was able to access the databases.


## Syslog Server

### What I Did

I installed and enabled rsyslog. After starting the service, I checked its status to make sure it was running properly.

I also used the `logger` command to create a test message and checked `/var/log/syslog` to confirm that the message was recorded.

### Commands Used

bash
sudo apt install rsyslog -y

sudo systemctl start rsyslog

sudo systemctl enable rsyslog

systemctl status rsyslog

logger "This is a test log from Day3b"

tail /var/log/syslog

This lab taught me how Bash scripts can automate repetitive tasks and how cron jobs can run tasks automatically at scheduled times. I also learned how to install and configure server services such as Docker, MariaDB and Syslog.

Although I made a few mistakes while running some commands, troubleshooting the problems helped me understand Linux better. Overall, this lab gave me more confidence in using Ubuntu and managing different server services.
