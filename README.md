# Replica Set
É uma estrutura que vai encapsular um ou mais Pods
Ele pode gerenciar vários Pods ao mesmo tempo

# Comando
kubectl get rs --watch = vai aparecer os Pods no Replica Set, vai aparecer o nome, e os numeros de replicas

# Atributo simples Replica Set nos arquivos YAML
replica: 3  = definimos que será 3 replicas, caso alguma falhe, por padrão é 1
matchLabels: algum-arquivo = ele tem que ser igual a Label lá em cima, se não ele não consegue se achar
