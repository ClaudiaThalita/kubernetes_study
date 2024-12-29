# kubernetes_study

INSTALAÇÃO DO KIND

# Instalação do Kind

Este guia descreve os passos necessários para instalar o **Kind** (Kubernetes IN Docker), uma ferramenta que permite criar clusters Kubernetes localmente utilizando containers Docker.

## Pré-requisitos

- Sistema operacional baseado em Linux (a instalação pode ser adaptada para outras plataformas, consulte a documentação oficial do Kind).
- `curl` e `chmod` devem estar instalados no seu sistema.

## Passos para Instalação

### Passo 1: Baixar o Kind usando o `curl`

1. Abra o terminal no seu sistema.
2. Execute o comando abaixo para baixar a versão mais recente do Kind para Linux:

   ```bash
   curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.19.0/kind-linux-amd64

### Passo 2: Torne o arquivo executável

3. Torne o arquivo baixado executável:


   ```bash
   chmod +x ./kind

### Passo 3: Mover o kind para o diretório bin

4. Mova o binário para um diretório que esteja no seu caminho de execução ($PATH):


   ```bash
   sudo mv ./kind /usr/local/bin/kind

### Passo 4: Verificar a instalação

5. Verifique se o kind foi instalado corretamente executando:


   ```bash
   kind --version