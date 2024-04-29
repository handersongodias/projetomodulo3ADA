# Projetomodulo3ADA - Orquestração realizado no modulo 3
> A aplicação tem como objetivo simular transações de credito que utilizam o RabbitMQ , Redis, Minio, para envio, cache e controle das mensagens enviadas, que são coletadas de um arquivo .json, e analisadas pela aplicação que verifica o valor solicitado e o comportamento de valores anteriores. Caso seja identificado a possivel fraude , a mensagem é registrada e nao é realizada a transação.
>
- Configuração:
- - Instalar o Docker Desktop e o MiniKube
  - Iniciar o Docker Desktop

- - Fazer o download dos arquivos ou realizar o clone
    
- - Abrir o terminal (sugestão o vscode)
  - Acessar o diretorio onde foram salvos/clonados os arquivos .yaml

Dentro do terminal iniciar o minikube 

    $minikube start

Configurar o namespace padrão com "default"

    $ kubectl config set-context --current --namespace=default

Executar o comando para iniciar as aplicações e serviços

    $ kubectl apply -f .

Visualizar o dashboard, utilizar o comando:

    $ minikube dashboard

Acessar os serviços externamente, serão disponibilizados os links para acessos a todos os serviços configurados no namespace default
    
    $ minikube service --all

Comandos para deletar o ambiente

    $ kubectl delete -f . 
    $ minikube stop
