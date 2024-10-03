MINHA CONTRIBUIÇÃO COM ESTE PROJETO FOI DESENVOLVER:

        - 1 PROMPT PERSONALIZADO (Para gerar um treino mais acertivo para cada situação)
        
        - 1 Interface front-end para o Personal trainer coletar os dados necessários para popular o prompt
                --#A URL dessa aplicação WEB pode ser enviada via Whatsapp para os clientes, proporcionando um serviço personalizado
                   e garantindo mais praticidade e cerelidade através de uma automação.#

SUGESTÕES ADICIONAIS:

        - Para a automação funcionar efetivamente, teria que subir uma arquitetura na Nuvem.
    
    Minha sugestão é a seguinte infra:
        
        1) Utilizar a AWS como Cloud provider.
        2) Rodar a Aplicação WEB em uma instância do type (t2.micro) em uma Public-SubNet.
        3) Criar um TABELA no DYNAMODB para armazenar os dados coletados.
        4) Criar uma função LAMBDA que automatize a segunte função:
                - Toda vez que entrar dados no DynamoDB, a função LAMBDA popule o prompt utilizando o AWS BEDROCK e gerando o treino 
                  personalizado.
                - No output do Bedrock, outra função LAMBDA acione o serviço de SQS e envie o treino por e-mail ao cliente.
        5) Outra função LAMBDA salva o arquivo gerado pelo AWS BEDROCK em um Bucket do S3, para histórico do cliente 
                -utilizar como classe de armazenamento a Intelligent-Tiering para redução automática de custos.
                

#O QUE ACHARAM DA INFRA?
#COMO PODERIAMOS MELHORAR?
#QUAL OUTRA ARQUITETURA SERIA MAIS VIÁVEL PARA ESSE PROJETO?
#TOPA MONTAR ESSA ARQUITETURA?
        #PREPARAR A IMPLEMENTAÇÃO UTILIZANDO TERRAFORM E UTILIZAR A CULTURA DEVOPS?