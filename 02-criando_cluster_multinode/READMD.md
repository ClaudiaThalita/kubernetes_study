primeiramente vamos dar o comando:

kind create cluster --config=config=k8s/kind.yaml

caso você queria dar um nome ao seu cluster, para não ficar igual à kind, você pode fazer assim:

kind create cluster --config=kind.yaml --name=supernova


ele irá imprimir o seguinte :

Creating cluster "supernova" ...
 ✓ Ensuring node image (kindest/node:v1.27.1) 🖼
 ✓ Preparing nodes 📦 📦 📦 📦  
 ✓ Writing configuration 📜 
 ✓ Starting control-plane 🕹️ 
 ✓ Installing CNI 🔌 
 ✓ Installing StorageClass 💾 
 ✓ Joining worker nodes 🚜 
Set kubectl context to "kind-supernova"
You can now use your cluster with:

kubectl cluster-info --context kind-supernova

Have a question, bug, or feature request? Let us know! https://kind.sigs.k8s.io/#community 🙂


se você der um docker ps, vc verá que terão 4 conteinars rodando

e se você der um kubectl get nodes, você verá que tem 4 nodes rodando, todos ready, mas 1 deles será master.
