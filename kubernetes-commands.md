# Comandos Kubernetes

kubectl get deployments: Listar as implantações no namespace atual. Exisbe o nome das aplicações existentes.

kubectl get services: Listar os serviços no namespace atual. É possível visualizar o nome das aplicações, endereços de IP's e portas.

kubectl get pods: Visualizar os pods dentro de um namespace.

kubectl get pods -o wide: Alterar a visualização dos pods.

kubectl describe pod <nomeDoPodDaAplicação>: Mostrar informações detalhadas sobre um pod específico. Exibe IP, versão da imagem docker, porta, status de execução, node, id do container e etc.

kubectl describe deployment <nomeDaAplicação>: Descrever informações de deploy da aplicação.

watch -n 1 kubectl get pods: Assistir atualização do pods.

kubectl logs --tail 100 <nomeDoPodDaAplicacao>: Verificar logs da aplicação.

kubectl logs -f <nomeDoPodDaAplicacao>: Mostrar os logs da aplicação em tempo real.

kubectl get pods --namespace <nomeDoNamespace>: Verificar pods em um determinado namespace.

kubectl exec -it <nome-do-pod> -- env: Visualizar variáveis de ambiente em um pod.

kubectl config set-context --current --namespace=NOME_DO_NAMESPACE: Alterar para um determinado namespace do kubernetes.

kubens <nomeDoNameSpace>: Visualisar e alterar o namespace do kubernetes.

kubectx: Exibir os contextos do k8s configurados na máquina.
