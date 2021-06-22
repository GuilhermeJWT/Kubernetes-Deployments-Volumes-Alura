# Comandos
kubectl get rs --watch = vai aparecer os Pods no Replica Set, vai aparecer o nome, e os numeros de replicas
kubectl get deployments =  vai listar todos os deployments
kubectl rollout history deployment nginx-deployment = vai exibir tipo um controle de versionamento, caso tenha alguma alteração
kubectl rollout undo deployment nginx-deployment --to-revision=2 = vai voltar a versão anterior
kubectl delete deployment nginx-deployment = deleta um deployment

# Replica Set
É uma estrutura que vai encapsular um ou mais Pods
Ele pode gerenciar vários Pods ao mesmo tempo

# Deployments
Quando criamos um Deployments automaticamente criamos um Replica Set
O mais comum é criar os Pods dentro de um Deployment, seria meio que mais recomendado do que criar no Replica Set, mais funcionaria também

# Volume
Volumes possuem ciclos de vida independentes dos containers, Porém são dependentes dos Pods
Se um container morrer ele não morre, mais se o Pod em questão cair ou morrer ele automaticamente morre junto
PersistentVolumes possuem ciclos de vida independentes de Pods
É necessário um PersistentVolumeClaim para acessar um PersistentVolume

# Storage Classes
Storage Classes fornecem dinamismo para criação de PersistentVolumes conforme demanda

# Atributo simples Replica Set nos arquivos YAML
replica: 3  = definimos que será 3 replicas, caso alguma falhe, por padrão é 1
matchLabels: algum-arquivo = ele tem que ser igual a Label lá em cima, se não ele não consegue se achar
