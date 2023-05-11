# dio-aws
Bootcamp AWS - Digital Inovation One
Primeiro projeto - DIO bootcamp AWS

Premissas adotadas no projeto:
* Excluir diretórios, arquivos, grupos e usuários criados anteriomente;
* Todo provisionamento deve ser feito em um arquivos do tipo Bash Script;
* O dono de todos os diretórios criados será o uruário root;
* Todos os usuários terão permissão total dentro do diretório 'publico';
* Os usuários de cada grupo terão permissão total dentro de seu respectivo diretório;
* Os usuários não poderão ter permissão de leitura, escrita e execução em diretórios de departamentos que eles não pertencem;
* Subir arquivo de script criado para a sua conta Github.


DIRETÓRIOS: 
/publico /adm /ven /sec

GRUPOS:
GRP_ADM 
GRP_VEN
GRP_SEC


USUÁRIOS:
ADM: carlos	maria		joao
VEN: debora	sebastiana	roberto
SEC: josefina	amanda		rogerio

Descritivo:
* logar como usuário root
* acessar a raiz 0 diretórios 

Realizar os seguintes passos (substituir o que tiver entre ''):
PRIMEIRO PASSO - * Excluir diretórios, arquivos, grupos e usuários criados anteriomente:
 ** Excluir os diretórios ** rm -Rf / 'nome do diretório'/ 

 ** Excluir os usuários ** 
  * Checar os usuários * cat /etc/passwd
  * Remover os usuários * userdel -r 'usuário'

 ** Excluir os grupos ** 
  * Checar os usuários * cat /etc/group
  * Remover os usuários * userdel 'grupo'

 
 SEGUNDO PASSO: Criar um Script
 * criar o diretório scripts: mkdir scripts
 * criar um novo script: nano script.sh
     
     ** #!/bin/bash 
      
    -- criar os diretórios -- mkdir /'diretorio'
    
    -- criar grupos -- groupadd GRP_'GRUPO'
    
    -- criar usuários e adicionar aos grupos -- useradd 'usuario' -m -s /bin/bash -p $(openssl passwd -crypt 'senha') -G 'grupo'
    
    -- permissões nos diretórios -- 
    
    chown (define o dono) - chown 'usuario': 'grupo' /'diretorio'
    
    chmod (define as permissões de rwx)  xxx /'diretorio' 
    
