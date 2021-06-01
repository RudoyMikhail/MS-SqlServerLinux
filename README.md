# MS_SqlServerLinux

#To install via cmd=> https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15</br>
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
systemctl status mssql-server --no-pager</br>
#If you plan to connect remotely, you might also need to open the SQL Server TCP port (default 1433) on your firewall</br>
#Use the following steps to install the mssql-tools on Ubuntu</br>
#The following one is a bit generic</br>
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -</br>
#Then specific one for the version you are going to install on your machine</br>
curl https://packages.microsoft.com/config/ubuntu/20.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list</br>
sudo apt-get update</br> 
sudo apt-get install mssql-tools unixodbc-dev</br>
echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bash_profile</br>
echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bashrc</br>
source ~/.bashrc</br>
#It looks like that's it</br>

#How to connect locally? That is how to connect to your PC</br>
sqlcmd -S localhost -U SA -P '<YourPassword>'#Note that password should be set without single quotes and angle brackets</br>
If successful, you should get to a sqlcmd command prompt: 1></br>






