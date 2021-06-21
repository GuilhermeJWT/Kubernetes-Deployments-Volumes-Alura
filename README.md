# Comando
kubectl get rs --watch = vai aparecer os Pods no Replica Set, vai aparecer o nome, e os numeros de replicas
kubectl get deployments =  vai listar todos os deployments
kubectl rollout history deployment nginx-deployment = vai exibir tipo um controle de versionamento, caso tenha alguma alteração
kubectl rollout undo deployment nginx-deployment --to-revision=2 = vai voltar a versão anterior


# Replica Set
É uma estrutura que vai encapsular um ou mais Pods
Ele pode gerenciar vários Pods ao mesmo tempo

# Deployments
Quando criamos um Deployments automaticamente criamos um Replica Set
O mais comum é criar os Pods dentro de um Deployment, seria meio que mais recomendado do que criar no Replica Set, mais funcionaria também

# Atributo simples Replica Set nos arquivos YAML
replica: 3  = definimos que será 3 replicas, caso alguma falhe, por padrão é 1
matchLabels: algum-arquivo = ele tem que ser igual a Label lá em cima, se não ele não consegue se achar
