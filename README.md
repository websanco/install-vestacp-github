# install-vestacp-github
apt-get update  
apt-get install $your_package  
apt-get install yum  

systemctl nginx stop
systemctl apache2 stop

service nginx stop
service httpd stop


yum install wget gcc gcc-c++ flex bison make bind bind-libs bind-utils openssl openssl-devel perl quota libaio libcom_err-devel libcurl-devel gd zlib-devel zip unzip libcap-devel cronie bzip2 cyrus-sasl-devel perl-ExtUtils-Embed autoconf automake libtool which patch mailx db4-devel  

wget https://raw.githubusercontent.com/websanco/install-vestacp-github/master/Letscript.sh  
chmod 777 ./Letscript.sh    
./Letscript.sh    
