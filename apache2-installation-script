#!/bin/bash

banner()
{
  echo "+------------------------------------------+"
  printf "| %-40s |\n" "`date`"
  echo "|                                          |"
  printf "|`tput bold` %-40s `tput sgr0`|\n" "$@"
  echo "+------------------------------------------+"
}

banner "apache installation script"
sleep 2
if [ $(id -un) == "root" ];
then
        apt install apache2 -y >> /dev/null
        echo "this is my new website" >>/var/www/index.html
else
        echo "do not allow anyone access"
        exit 1

fi

banner "Copying files"
cp -v /etc/hosts /tmp
cp -v /etc/passwd /tmp
sleep 4

banner "Downloading article"
curl https://www.shellscript.sh > /tmp/banner.html
sleep 5

banner "Finished."
