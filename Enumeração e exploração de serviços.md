## Serviços

Porta 21: FTP

Porta 22: SSH

Porta 25: SMTP

Porta 53: DNS

Porta 80: HTTP

Portas 110/143/993/995: imap e pop3

Porta 111: rpcbind

## exploração

### FTP

<img width="1296" height="594" alt="image" src="https://github.com/user-attachments/assets/6ae402a2-be11-4277-aed3-d42eabb131af" />


<img width="519" height="95" alt="image" src="https://github.com/user-attachments/assets/5121ea25-a875-48fe-9c92-58eed6b3f7d2" />

não consigo fazer upload de arquivos, vamos para o proximo serviço.

ssh - sem sucesso

SSH-2.0-OpenSSH_8.2p1 Ubuntu-4ubuntu0.5


rodei novamente um nmap na porta 25 que está rodando um serviço smtp, serviço de email

<img width="1250" height="295" alt="image" src="https://github.com/user-attachments/assets/b8f4dc29-c66c-42d8-ac74-cf24da430970" />

tentei um nmap com script e tbm sem resposta

<img width="788" height="249" alt="image" src="https://github.com/user-attachments/assets/70a23c95-6134-4ade-83ea-c3b481b8ae77" />

a porta 111 é o rpcbind, um servicoe que nao deve ser exposto extermanemte. Não identifiquei nada de interessante tb

<img width="805" height="303" alt="image" src="https://github.com/user-attachments/assets/dce325bc-7253-4ba8-b443-4275d9ae1492" />

por ultimo, temos a porta 80, http.

