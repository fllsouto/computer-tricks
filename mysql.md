## MySQL
## Useful Commands
## Troubleshooting
### Change mysql root password on Centos7/Fedora 25

```bash
# Run all comands as root user

# 1. Stop mysql:
systemctl stop mysqld

# 2. Set the mySQL environment option
systemctl set-environment MYSQLD_OPTS="--skip-grant-tables"

# 3. Start mysql usig the options you just set
systemctl start mysqld

# 4. Login as root
mysql -u root

# 5. Update the root user password with these mysql commands
mysql> UPDATE mysql.user SET authentication_string = PASSWORD('MyNewPassword')
    -> WHERE User = 'root' AND Host = 'localhost';
mysql> FLUSH PRIVILEGES;
mysql> quit

#6. Stop mysql
systemctl stop mysqld

#7. Unset the mySQL envitroment option so it starts normally next time
systemctl unset-environment MYSQLD_OPTS

#8. Start mysql normally:
systemctl start mysqld

#7. Try to login using your new password:
mysql -u root -p
```
