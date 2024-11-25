# "PROVISIONANDO EC2 na AWS"

Este foi um desafio proposto no Curso Preparatório da PROZ para a certificação AWS Certified Solutions Architect - Associate, no módulo Redes e Linux Essentials para AWS.

Desafio: Provisionar uma EC2-AWS para atender as demandas da Banda, onde o prposito foi focado no aprendizado e organizaçao da documentação e dos arquivos da banda.
Então a banda teve interesse de crescer de forma organizada e estrutuda utilizando os serviços em cloud, pensando nisso eles também conheceram o Amazon Linux, que é
uma distribuição otimizada para a nuvem, sendo uma opção excelente para as instâncias EC2. Os membros da banda estão empolgados para testar essa tecnologia e começar
a armazenar e gerenciar os seus documentos e arquivos na nuvem. Neste exercício iremos irei ajudar como poderemos iniciar nesta demanda.


# Tipo de serviço 

EC2 - AWS 

# Requisito da EC2
- imagem: Amazon Linux 2
- Tipo: T2.micro
- Armazenamento: 1º volume com 8gb para S.O e 2º volume com 30GB para armazenamento de dados 
- Acesso remoto via SSH com chave privada e gerada pelo próprio portal

# Para instalação basta seguir esse Playbook em 10x Passos
1- Primeiramente você precisa ter uma conta da AWS, acessar a console e seguir os passos abaixo:
Para criar a conta segue o link : https://repost.aws/pt/knowledge-center/create-and-activate-aws-account

2- Acessar o portal e selecionar o serviço conforme a imagem abaixo

![image](https://github.com/user-attachments/assets/15e59ad2-5518-4954-80a8-866662a03d5c)

3- Você deve ar um nome para sua instância para ficar identificado

![image](https://github.com/user-attachments/assets/5d64bac5-7930-43c0-8111-4ada5255021b)

4- selecionar a imagem e o tipo da instância 

![image](https://github.com/user-attachments/assets/030e91d3-5e1a-4fb6-9c94-f6ac418683a2)
![image](https://github.com/user-attachments/assets/2ffc53da-1545-44c8-bac2-81ee6fbfab6f)

5- Selecione também o tipo de Instância 

![image](https://github.com/user-attachments/assets/6c608727-6d89-4aeb-aeb9-b9816bccceaa)

6- Criar um par de chave para tornar acessível de forma segura através da internet, aqui eu criei uma com o nome chamado ChaveAWSEC2
bastando apenas clicar do lado para criar a sua prórpria chave, detalhe salve esse arquivo de forma segura. 

![image](https://github.com/user-attachments/assets/107a9d0c-a242-4287-8d6d-0fc4b2933360)

7- Em configuração de redes, você deve seguir esses passos, caso queira liberar apenas um acesso remoto para um determinando endereço 
você deve especificar ondem tem "Qualquer lugar 0.0.0.0/0" e colocar personalizado ou o IP que está aparecendo.

![image](https://github.com/user-attachments/assets/72ca1447-a12b-4a93-9d14-3662c7bf3209)

8- No quesíto de armazenamento, você deverar escolher um segundo volume como adicional, sendo do tipo EBS, conforme a imagem abaixo, pois o primeiro se
trata do volume do sistema operacional, após a seleção basta clicar no botão, executar instância e aguardar ela subir.

![image](https://github.com/user-attachments/assets/9d2be222-f818-46da-bc3d-2e451bc53a14)

9- Executando o acesso remoto, conforme as informações
Você vai voltar para a guia de instância no próprio console e selecionar a instância provisionada e clicar em "Conectar" como mostra na imagem

![image](https://github.com/user-attachments/assets/cbb24c17-4317-4349-807e-4f5d77ee4876)

você deve selecionar a guia Cliente SSH e executar os passos para se conectar de forma remota e segura via SSH


![image](https://github.com/user-attachments/assets/1d5be1f0-f3bc-4a26-9cec-425ebd7e4f59)
Aqui eu utilizei um próprio servidor meu, interno de LAB, onde a sintaxe do comando foi como essa abaixo: 

![image](https://github.com/user-attachments/assets/3c701381-3c29-43ad-a928-65da90b9b00b)

Uma vez logado na console do hosts remoto, basta seguir o ultimo passo para brincar na Console


10-Neste Passo eu dediquei a montar um segundo volume conforme o proposto, utilizando ele para criar arquivo e salva neste diretório.
Neste passo eu utilizanei os comandos cat, dh -h, fdisk -l, vim e touch para manipular meu arquivo e dados.

Adiconar no arquivo "fstab" a montagem de forma automática 

![image](https://github.com/user-attachments/assets/7bb0a80d-b31d-4291-b041-b39ef6889a7d)

Aqui detalhei em único print os comandos que utilizei 

![image](https://github.com/user-attachments/assets/3d9a4dfc-4de6-44b1-8ec7-b26fd608597c)


# Explicação

Neste desafio mostra que é possível subir uma instância EC2 para atender a necessidade e aprendizado da equipe da banda, Pensando assim
os requisitos do desafio proposto foi atendido 

# Autor
ALmir ALves 




























