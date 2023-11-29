# Mobile Security Framework (MobSF) 

It is an automated mobile application (Android/iOS/Windows) pen-testing, malware analysis and security assessment framework capable of performing static and dynamic analysis.

#  Installation steps for Kali Linux OS :

1. Install Git using below provided command in terminal

`sudo apt-get install git`

2. Install Python 3.8/3.9 using below provided command

`sudo apt-get install python3.8`

3. Install latest version of JDK

4. Install the required dependencies using below provided command

`sudo apt install python3-dev python3-venv python3-pip build-essential libffi-dev libssl-dev libxml2-dev libxslt1-dev libjpeg62-turbo-dev zlib1g-dev wkhtmltopdf`

5. Download MobSF using below provided command

`git clone https://github.com/MobSF/Mobile-Security-Framework-MobSF.git`

Change working directory to MobSF

`cd Change working directory to MobSF`

Setup MobSF using command — sudo ./setup.sh

`./setup.sh`

Use below command to run MobSF –

`./run.sh 127.0.0.1:8000`

Note: we can use any port number instead of 8000, but it must be available

Access the MobSF web interface in browser using the URL — http://127.0.0.1:8000
