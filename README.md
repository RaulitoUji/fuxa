[Unit]
Description=Fuxa Server
After=network.target

[Service]
ExecStart=/ruta/a/FUXA/start.sh
WorkingDirectory=/ruta/a/FUXA/
Restart=always
ExecStartPre=/bin/bash -c 'cd /ruta/a/nombre-del-repositorio && git pull'

[Install]
WantedBy=multi-user.target
