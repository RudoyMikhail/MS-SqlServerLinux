# MS_SqlServerLinux

#To install vai cmd=> https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15</br>
#For Ubuntu 20.04 version is</br> 

#Getting data from Microsoft source</br> 
sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2019.list)"</br>
#Update existing source and install new software</br> 
sudo apt-get update</br>
sudo apt-get install -y mssql-server</br>
sudo /opt/mssql/bin/mssql-conf setup</br>
#After that cmd choose version you are going to use from 1 to 8 by typing, for example 2(second one)</br>
#You will recieve a prompt to enter a password</br>
#Make sure to specify a strong password for the SA account (Minimum length 8 characters, including uppercase and lowercase letters, base 10 digits and/or non-alphanumeric symbols)<br>
#Enter password once again and try to keep in a safe place and don't forget</br> 
systemctl status mssql-server --no-pager



