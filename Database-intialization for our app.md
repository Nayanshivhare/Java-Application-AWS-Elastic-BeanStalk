### ssh from your terminal
![image](https://user-images.githubusercontent.com/66699491/213848911-b930f670-19c6-4a33-aeb5-d5433b8ac8c9.png)

### after ssh run following command for database intialization.

1.  sudo yum install mysql
2.  mysql -h database-1.cnprqxklgg24.us-east-1.rds.amazonaws.com -u admin -pNayanshiv9424
3.  git clone https://github.com/devopshydclub/vprofile-project.git
4.  cd vprofile-project/
5.  git branch -a
6.  git checkout aws-Refactor
7.  cd src/main/resources/
8.  mysql -h database-1.cnprqxklgg24.us-east-1.rds.amazonaws.com -u admin -pNayanshiv9424 RDSProject < db_backup.sql
9.  mysql -h database-1.cnprqxklgg24.us-east-1.rds.amazonaws.com -u admin -pNayanshiv9424 RDSProject
10. show tables;

### database has been intialized.
### exit and logout from instance and terminate instance.
