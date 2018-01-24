
apt-get update  
apt-get install $your_package  
apt-get install yum  

systemctl nginx stop
systemctl apache2 stop

service nginx stop
service httpd stop


yum install wget gcc gcc-c++ flex bison make bind bind-libs bind-utils openssl openssl-devel perl quota libaio libcom_err-devel libcurl-devel gd zlib-devel zip unzip libcap-devel cronie bzip2 cyrus-sasl-devel perl-ExtUtils-Embed autoconf automake libtool which patch mailx db4-devel  

# install-vestacp-github
curl -O http://vestacp.com/pub/vst-install.sh

ash vst-install.sh --nginx yes --apache yes --phpfpm no --named no --remi yes --vsftpd yes --proftpd no --iptables yes --fail2ban yes --quota yes --exim yes --dovecot yes --spamassassin yes --clamav yes --softaculous yes --mysql yes --postgresql no --hostname sudomain_here --email email_here --password pass_here


yum install git -y  
git clone https://github.com/letsencrypt/letsencrypt /opt/le  
cd /opt/le  



# install-vestacp- VULTR 521M
bash vst-install.sh --nginx yes --apache yes --phpfpm no --named no --remi no --vsftpd yes --proftpd no --iptables yes --fail2ban yes --quota yes --exim yes --dovecot yes --spamassassin yes --clamav yes --softaculous no --mysql yes --postgresql no

yum install git -y  
git clone https://github.com/letsencrypt/letsencrypt /opt/le 
service nginx stop 
service httpd stop 
cd /opt/le 
./letsencrypt-auto certonly --standalone -d b1.hostviet.pro 

rm -rf /usr/local/vesta/ssl/certificate.crt 
ln -s  /etc/letsencrypt/live/b1.hostviet.pro/cert.pem /usr/local/vesta/ssl/certificate.crt 

rm -rf /usr/local/vesta/ssl/certificate.key 
ln -s  /etc/letsencrypt/live/b1.hostviet.pro/privkey.pem /usr/local/vesta/ssl/certificate.key 

service vesta restart 


wget https://vestacp.ss88.uk/Install_CSF_on_VestaCP/Install.sh -O ./Install.sh  
chmod 777 ./Install.sh  
sudo ./Install.sh 
