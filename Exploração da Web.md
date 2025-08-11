Para começar a exploração web, criei um arquivo com os subdominios que vamos explorar.

<img width="466" height="330" alt="image" src="https://github.com/user-attachments/assets/19954ff7-0e66-4240-b350-d5949f4730b7" />


Vamos começar pelo blog.inlanefreight.local

<img width="1124" height="651" alt="image" src="https://github.com/user-attachments/assets/eccd2fbc-645c-43c2-bd04-4d465a8b6422" />

dando um ctrl + u para analisar o codigo fonte, vi que está rodando um Drupal, pesquisei no google para saber oq é.

<img width="940" height="513" alt="image" src="https://github.com/user-attachments/assets/eb19e80e-b02e-4fdc-8816-0c57fb379379" />

pesquisei no google por cves e vulnerabilidades que efetam a versão 9 do Drupal, mas não encontrei nada. Vou seguir para a próxima aplicação.

Vamos pesquisar o subdominio careers

<img width="1375" height="810" alt="image" src="https://github.com/user-attachments/assets/3977882f-3cd6-4914-b9f3-c073d5b6b9eb" />

encontramos uma pagina de login careers.inlanefreight.local/login

<img width="1326" height="695" alt="image" src="https://github.com/user-attachments/assets/7f690389-87f6-4728-9bcf-b909d1ee72bf" />

tentei logar com senhas padrões como admin x admin mas sem sucesso.

a pagina careers.inlanefreight.local/login é para nos canditatar a uma vaga e enviar um currículo. Testando essa funcionalidade, vemos q ela permite o upload de qualquer tipo de arquivo, mas não mostra onde o arquivo está localizado depois do upload. 

<img width="923" height="771" alt="image" src="https://github.com/user-attachments/assets/92a6799f-e52a-443e-94ed-ddc49e02b260" />

vou criar uma conta e me registrar na aplicação.

<img width="928" height="809" alt="image" src="https://github.com/user-attachments/assets/326a8719-b250-4428-add3-300f461efe95" />

<img width="722" height="383" alt="image" src="https://github.com/user-attachments/assets/9dba18dd-564c-4555-92b1-6f1725dbe3c4" />


Logo de cara identificamos um IDOR

<img width="580" height="355" alt="image" src="https://github.com/user-attachments/assets/c97030bc-9fea-4d86-ad74-25178f3d23fb" />



IDOR (Insecure Direct Object Reference), ou Referência Direta de Objeto Insegura, ocorre quando um aplicativo web permite que usuários acessem dados ou recursos através de identificadores diretos (como IDs em URLs ou parâmetros de formulário) sem verificar se o usuário tem permissão para acessá-los. Essencialmente, um atacante pode manipular esses identificadores para acessar informações ou funcionalidades que não deveria ter acesso.

Basicamente conseguimos mudar de conta passando outro id.

