# cloudscope 구동 방법


01) Raspberry Pi Imager 를 이용하여 raspbian OS 6.1 32bit 클린 설치
02) 타임존 설정 (south korea 영어), wifi 연결, 사용자설정
03) sudo apt-get update; sudo apt-get -y upgrade; sudo apt-get -y dist-upgrade; sudo apt-get -y autoremove
04) curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
05) sudo apt-get install nodejs
06) sudo npm install -g pm2
07) git clone cloudscope; cd cloudscope
08) npm install
09) sudo pm2 start media_server.js --name=CLOUDSCOPE_RTSP
10) sudo pm2 start app.js --name=CLOUDSCOPE
11) sudo pm2 startup systemd -u root
12) sudo pm2 save
13) sudo node init.js

14) 핸드폰이나 랩탑을 이용하여 SSID CLOUDSCOPE_XXXX 에 연결 (패스워드 invisionlab4u)
15) 웹브라우저를 통해 http://10.10.10.1/install 에 접속하여 WIFI 설정
