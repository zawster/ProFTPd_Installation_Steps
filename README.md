# Proftpd-Setup-Steps
//  Install proFTPd
          
       sudo apt install proftpd
       
       # Edit config file
       sudo vi /etc/proftpd/proftpd.conf
       // changings
       ServerName       "example.com"
       //  jail the user
       DefaultRoot      ~
       
       //  Restart proftpd server
       sudo service proftpd restart
       
      
#  add new User
      
      
      #  make directory for user
      sudo mkdir /home/ftp
      
      //  don't access to shell
      sudo vi /etc/shells
      
      // add this line in file
      /bin/false
      
      // Now add user
      sudo useradd ftpUserName  -p  yourPasswd  -d  /home/ftp  -s  /bin/false
      
//   Use ProFTPd
      
      //  Go to your local browser and type 
      ftp://localhost
      
      // If you wana access proFTPd from other computers type in browser
      ftp://mainServerIP
      // for example
      ftp://912.168.11.124
