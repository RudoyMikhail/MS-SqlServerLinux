# MS_SqlServerLinux

#To install vai cmd=> https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15
#For Ubuntu 20.04 version is 

#Getting data from Microsoft source 
sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2019.list)"
#Update existing source and install new software 
sudo apt-get update
sudo apt-get install -y mssql-server
sudo /opt/mssql/bin/mssql-conf setup
#After that cmd choose version you are going to use from 1 to 8 by typing, for example 2(second one)
#You will recieve a prompt to enter a password. Password should contain one capital letter, one special sign, have minimun length of 8 characters and also a number
#Enter password once again and try to keep in a safe place and don't forget 

