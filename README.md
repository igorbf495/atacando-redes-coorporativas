# Cenário e Início


Nosso cliente, a Inlanefreight, contratou nossa empresa, a Acme Security, Ltd., para realizar um Teste de Penetração Externa de escopo completo para avaliar a segurança de seu perímetro. O cliente nos solicitou a identificação do maior número possível de vulnerabilidades; portanto, testes evasivos não são necessários. Eles gostariam de verificar que tipo de acesso pode ser obtido por um usuário anônimo na internet. De acordo com as Regras de Engajamento (RoE), se conseguirmos violar a DMZ e obter acesso à rede interna, eles gostariam que avaliássemos até onde podemos levar esse acesso, incluindo o comprometimento do domínio do Active Directory. O cliente não forneceu credenciais de usuário de aplicativo web, VPN ou Active Directory. Os seguintes domínios e intervalos de rede estão no escopo dos testes:

|**Teste externo**|**Testes internos**|
|---|---|
|10.129.xx (host de destino voltado para "externo")|172.16.8.0/23|
|*.inlanefreight.local (todos os subdomínios)|172.16.9.0/23|
||INLANEFREIGHT.LOCAL (domínio do Active Directory)|

O cliente forneceu o domínio primário e as redes internas, mas não forneceu detalhes sobre os subdomínios exatos dentro desse escopo, nem sobre os hosts "ativos" que encontraremos na rede. Eles gostariam que realizássemos uma descoberta para ver que tipo de visibilidade um invasor pode obter em sua rede externa (e interna, se conseguir uma posição segura).

Técnicas de teste automatizadas, como enumeração e varredura de vulnerabilidades, são permitidas, mas devemos trabalhar com cuidado para não causar interrupções no serviço. Os seguintes itens estão fora do escopo desta avaliação:

- Phishing/Engenharia Social contra qualquer funcionário ou cliente da Inlanefreight
- Ataques físicos contra instalações da Inlanefreight
- Ações destrutivas ou testes de negação de serviço (DoS)
- Modificações no ambiente sem o consentimento por escrito da equipe de TI autorizada da Inlanefreight

---

## Início do Projeto

Neste ponto, temos um Escopo de Trabalho (SoW) assinado pela gerência da nossa empresa e por um membro autorizado do departamento de TI da Inlanefreight. Este documento SoW lista as especificações do teste, nossa metodologia, o cronograma, as reuniões e entregas acordadas. O cliente também assinou um documento separado de Regras de Engajamento (RoE), comumente conhecido como documento de Autorização para Teste. Este documento é crucial para ter em mãos antes de iniciar o teste e lista o escopo para todos os tipos de avaliação (URLs, endereços IP individuais, intervalos de rede CIDR e credenciais, se aplicável). Este documento também lista o pessoal-chave da empresa de testes e da Inlanefreight (um mínimo de dois contatos para cada lado, incluindo seu número de celular e endereço de e-mail). O documento também lista detalhes específicos, como a data de início e término do teste e a janela de teste permitida.

Temos uma semana para testes e dois dias adicionais para escrever o rascunho do nosso relatório (no qual devemos trabalhar à medida que avançamos). O cliente nos autorizou a testar 24 horas por dia, 7 dias por semana, mas nos pediu para executar varreduras pesadas de vulnerabilidades fora do horário comercial normal (após as 18h, horário de Londres). Verificamos todos os documentos necessários e temos as assinaturas necessárias de ambas as partes, e o escopo está totalmente preenchido, então estamos prontos para prosseguir do ponto de vista administrativo.

---

## Início dos testes

É a primeira hora da manhã de segunda-feira e estamos prontos para começar os testes. Nossa máquina virtual de testes está configurada e pronta para uso, e configuramos um esqueleto para anotações e uma estrutura de diretórios para fazer anotações usando nossa ferramenta de anotações favorita. Enquanto nossas varreduras de descoberta iniciais são executadas, como sempre, preencheremos o máximo possível do modelo de relatório. Essa é uma pequena vantagem que podemos obter enquanto aguardamos a conclusão das varreduras para otimizar o tempo que temos para os testes. Redigimos o seguinte e-mail para sinalizar o início dos testes e enviamos cópia para todo o pessoal necessário.

![E-mail de Bryan Robinson para Sarah McDonald sobre o início de um teste de penetração externa para a Inlanefreight. Testando tráfego do IP 10.10.14.15. Contato secundário: John Lee, Consultor de Segurança Principal. Inclui detalhes de contato e uma visão geral do procedimento de teste.](https://academy.hackthebox.com/storage/modules/163/start_testing.png)

Clicamos em enviar no e-mail e iniciamos nossa coleta de informações externas.
