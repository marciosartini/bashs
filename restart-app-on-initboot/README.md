1) Crie um arquivo de script Bash. Por exemplo, você pode criar um arquivo chamado "minha_rotina.sh" usando o editor de texto "nano" no terminal:
- $ sudo nano /etc/minha_rotina.sh

2) Adicione o código da sua rotina Bash ao arquivo. Certifique-se de que o script esteja executável usando o comando:
- $ sudo chmod +x /etc/minha_rotina.sh

3) Crie um arquivo de serviço para sua rotina Bash usando o editor de texto "nano" no terminal:
- $ sudo nano /etc/systemd/system/minha_rotina.service

4) Adicione as seguintes linhas ao arquivo:
file: minha_rotina.service
```
[Unit]
Description=Minha rotina Bash

[Service]
ExecStart=/etc/minha_rotina.sh

[Install]
WantedBy=multi-user.target
```
5) Salve e feche o arquivo.

6) Recarregue a lista de serviços do systemd:
- $ sudo systemctl daemon-reload

7) Ative o serviço para que seja executado na inicialização:
- $ sudo systemctl enable minha_rotina.service

8) Reinicie o sistema para testar se sua rotina Bash está sendo executada automaticamente na inicialização:
- $ sudo reboot

