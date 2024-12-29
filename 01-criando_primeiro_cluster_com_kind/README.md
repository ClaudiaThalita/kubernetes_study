
### Passo 1: Primeira coisa que faremos é usar o comando `kind` para criar um Cluster
1. Abra o terminal no seu sistema.
2. Execute o comando abaixo para baixar a versão mais recente do Kind para Linux:

   ```bash
   kind

Executando o comando acima o seguinte texto aparece:

# Usage:
  kind [command]

## Available Commands:
- **build**       Build one of [node-image]
- **completion**  Output shell completion code for the specified shell (bash, zsh or fish)
- **create**      Creates one of [cluster]
- **delete**      Deletes one of [cluster]
- **export**      Exports one of [kubeconfig, logs]
- **get**         Gets one of [clusters, nodes, kubeconfig]
- **help**        Help about any command
- **load**        Loads images into nodes
- **version**     Prints the kind CLI version

## Flags:
- `-h, --help`              help for kind
- `--loglevel string`       DEPRECATED: see `-v` instead
- `-q, --quiet`             silence all stderr output
- `-v, --verbosity int32`   info log verbosity, higher value produces more output
- `--version`               version for kind

Use `kind [command] --help` for more information about a command.


# Tutorial: Gerenciamento de Clusters com Kind

## 1 - Criando um Cluster

1. Para criar um novo cluster com o Kind, use o seguinte comando:


   ```bash
   curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.19.0/kind-linux-amd64

## 2 - Listando Clusters

3. Para listar todos os clusters disponíveis, execute o comando:


   ```bash
   kind get clusters

## 3 - Deletando um Cluster

3. Para deletar um cluster específico, utilize:
4. Substitua [nome] pelo nome do cluster que deseja excluir.


   ```bash
   kind delete cluster [nome]

## 4 - Acessando o Cluster

5. Após criar ou acessar um cluster, você pode usar o comando abaixo para obter informações sobre o cluster:



   ```bash
   kubectl cluster-info --context kind-kind
6. Isso irá fornecer detalhes sobre o servidor/cluster.

## 5 - Verificando Imagens em Execução

7. Para verificar as imagens em execução no Docker, use o comando:

   ```bash
   docker ps
   
## 6 - Visualizando Nodes
8. Se você executar o seguinte comando no kubectl, verá o kind-control-plane listado como um nó (node) em execução:

   ```bash
   kubectl get nodes

9. Isso indicará que o Docker está executando o container como um nó do Kubernetes.



##  - Verificando a Configuração
9. Para verificar a configuração do seu cluster, use o comando:

   ```bash
   ls ~/.kube/

11. Isso mostrará os arquivos de configuração do Kubernetes.