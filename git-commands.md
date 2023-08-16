**Git - Principais comandos**

Antes de qualquer interação com o git, você precisa informar quem é você para que ele armazene corretamente os dados do autor de cada uma das alterações no código.

git config --local user.name "Seu nome aqui": (Parâmetro --local faz as alterações apenas para um projeto, o paramâmetro --global faz as alterações para o computador).

git config --local user.email "seu@email.aqui"

**Comandos Git**

git init: Inicia um repositório no git. Para isso é necessário está dentro da pasta do projeto.

git init --bare: diretorio/repositório que armazenará apenas as alterações do projeto

git status: Exibe o estado do repositório, se algum arquivo foi alterado ou se precisa salvar.

git add nomeDoArquivo, ou git add . (todos os arquivos): Faz com que o git monitore as mudanças dos arquivos desejados, e adiciona a modificação na área de staging para serem versionados.

git commit -m "mensagem descrivas sobre a mudança no arquivo": Commita os arquivos na área de staging com uma mensagem descritiva das alterações.

git log: Mostra histórico de alterações no projeto.

git log --oneline: Mostra histórico de alterações no projeto de forma resumida.

git log -p: Mostra histórico de alterações no projeto de forma mais completa.

git log --graph: Mostra logs por linhas de desenvolvimento específicas. 


	{
	.gitignore - arquivo usado para dizer ao git quais arquivos não devem ser monitorados.
				Se for arquivo, inserir o nome do arquivo no .gitignore, ex: arquivo.html
				Se for pasta, inserir o nome da pasta no .gitignore, ex: nomePasta/

	git add .gitignore
	git commit -m "Adicionaodo git Ignore"
	}

git remote add nomeArbitrarioParaServidor enderecoDoRepositorio (pode ser uma pasta local, um pasta do outro PC em rede, url de um servidor pela internet).

git remote: Lista todos os repositórios ativos.

git remote -v: Mostra o endereço do servidor.

git push -u nomeDoServidor nomeDaBranch: Envia os arquivos do projeto para um repositório remoto.

git pull nomeDoServidor nomeDaBranch: Baixa os arquivos do projeto que estão em um servidor.

git clone linkDoRepositório: Clona um projeto que já existe no Github.

git fetch: Obtem informações atualizadas do repositório remoto. Serve para baixar branches remotas ainda não existentes localmente.

*O que é uma branch? - uma linha de desenvolvimento que permite usuários compartilharem o mesmo projeto simultaneamente.
São utilizados para desenvolver funcionalidades isoladas umas das outras.*

git branch -M "main": Trocar a branch atual para a branch main.

git branch: Visualizar as branchs ativas no projeto.

git branch nomeBranch: Criar uma nova branch.

git branch -D nomeDaBranch: Deletar uma branch (Tem que está fora dela).

git checkout -b nomeBranch: Criar uma nova branch baseada na branch atual, e altera para ela em um único comando (equivale aos dois comandos anteriores).

git checkout nomeBranch: Alterar para outra branch.

git merge nomeDaBranchASerMesclada: Unir uma branch secundária com a atual.

git rebase nomeDaOutraBranch: Pega todos commits da branch em questão, e atualiza a branch master principal, sem criar um novo commit. O commit do rebase permanece sendo o último.

git checkout --nomeDoArquivo: Desfazer alterações em arquivos que não foram adicionados e comitados.

git reset HEAD nomeDoArquivo: Desmarcar algum arquivo alterado para commit. (git add marca o arquivo para commit).

git revert codigoDoHashDoCommitASerDesfeito: Desfazer um commit (git log para visualizar os hashs dos commits feitos).

git stash: Salvar alterações de maneira temporária para depois retornar.

git stash list: Listar todas as mudanças salvas temporariamente.

git stash pop: Recuperar as alterações do stash atual e une com as alterações atuais do projeto, e remove essa stash automaticamente.

git checkout hashDoCommit: Voltar ao tempo, sendo possível visualizar o projeto no estado de um commit especifico.
	Qualquer alteração feita nesse momento estará desconexa com o projeto principal.
	Para anexar os commits a serem feitos ao projeto, criar uma nova branch git checkout -b nomeBranch
	
git diff hashDeUmCommit.. hashDeOutroCommit: Visualizar a diferença entre o projeto no intervalo entre dois commits.

git tag -a nomeDaTag -m "Comentário": Versionamento do código, o comentário é opcional.