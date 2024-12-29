Primeira coisa que faremos é digitar um comando no kind para criar um cluster:

-- kind create cluster

--  kind get clusters //lista todos os clusters

-- kind delete clusters [nome] // deleta o cluster com nome 
Agora você pode usar o seu cluster com:

kubectl cluster-info --context kind-kind

depois do comando acima, conseguimos ter acesso ao servidor/cluster, e podemos ver qual imagem está sendo executada:

dê um "docker ps" 

veja que tem um conteiner sendo executado, que é o kind-control-plane

se você executar o comando kubectl get nodes, você poderá também ver o kind-control-plane, mas como um node. ( docker em execução)

Para ver a config você pode usar :

ls ~/.kube/