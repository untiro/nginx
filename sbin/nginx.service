[Unit]
Description=nginx - high performance web server
Documentation=http://nginx.org/en/docs/
After=network-online.target remote-fs.target nss-lookup.target
Wants=network-online.target
 
[Service]
Type=forking
PIDFile=/home/yshchanouski/nginx/logs/nginx.pid
ExecStartPre=/home/yshchanouski/nginx/sbin/nginx -t -c /home/yshchanouski/nginx/conf/nginx.conf
ExecStart=/home/yshchanouski/nginx/sbin/nginx -c /home/yshchanouski/nginx/conf/nginx.conf
ExecReload=/bin/kill -s HUP $MAINPID
ExecStop=/bin/kill -s QUIT $MAINPID
 
[Install]
WantedBy=multi-user.target
