## Comandos docker

docker ps: Listar os containers existentes na máquina.

docker ps -a: Listar os containers em execução e parados.

docker images: Listar as imagens existentes.

docker pull <image:tag>: Baixar uma imagem do docker hub. Se não especificar a tag, será baixada a tag padrão "latest".

docker push <nomeUsuario/nomeImagem:tag>: Enviar uma imagem para o docker hub.

docker run: Instanciar uma imagem. (Se a imagem não estiver baixada, será baixada automaticamente do docker hub).

docker run -it: Instanciar a imagem liberando o terminal.

docker start <containerId>: Iniciar um container informando o seu id.

docker attach <containerId>: Acessar o container em execução a partir do seu id.

docker stop <containerId>: Parar um container a partir do seu id.

docker log -f <idContainer>: Consultar os logs de um container de maneira constante.

docker ps --size: Com um container em execução, exibe o tamanho que ele ocupa em disco.

docker system df: Exibir um relatório informando a quantidade de imagens, containers, quantos ativos, o tamanho de cada um.

docker rm <idContainer>: Remover um container pelo id.

docker rmi <idImagem>: Remover uma imagem pelo id.

docker rm -v <containerId>: Remover container e seus volumes.

docker volume rm <volumeName>: Remover um volume. (O volume não pode está vinculado a nenhum container).

docker login docker.io: Fazer login no docker hub.

docker tag <nomeImagem:tag> <usuario/nomeImagem:tag>: Copiar uma imagem incluíndo o nome do usuário ao nome da imagem.


docker run -p 5433:5432 --name meu-container-pg12 -e POSTGRES_PASSWORD=1234567 -e POSTGRES_DB=minha_base postgres:12-alpine

	- flag -p permite mapear uma porta diferente da porta original da imagem. A porta a esquerda é a porta desejada para a aplicação rodar,
		e separado por " : " a imagem original configurada na imagem;
	
	- flag --name permite dá um nome personalizado ao container;
	
	- flag -e especificar valores para variáveis de ambiente. (nas documentações das imagem é possível ver quais as variáveis de ambiente disponíveis);
	