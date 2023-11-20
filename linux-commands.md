## Comandos de arquivos:

ls - listar conteúdo de um diretório.

ls -l - mostrar informações completas (com permissões, tamanhos...).

ls -h - mostrar tamanho em formato legível.

ls -a - mostrar arquivos ocultos.

ls -al - listar conteúdo de um diretório com arquivos ocultos e formatados.

cp <origem> <destino> - copiar arquivo de uma orgim para um destino.

cp  -f <origem> <destino> - copiar sobrescrevendo os arquivos de destino, caso existam.

cp -i <origem> <destino> - copiar os arquivos solicitando confirmação para sobrescrever os arquivos de destino.

cp -R <origem> <destino> - copiar diretórios de forma recursiva.

cd <diretório> - navegar para o diretório informado.

cd - navegar para a home.

pwd - mostrar o dirtório atual.

mkdir <diretório> - criar um novo diretório com o nome informado.

rm <nomeDoArquivo> - deletar um arquivo.

rm -r <diretório> - deletar um diretório informado recursivamente.

rm -f <nomeDoArquivo> - forçar a remoção de um arquivo.

rm -rf <diretório> - forçar a remoção de um diretório de maneira recursiva.

rm -i <diretorio> - deletar arquivo e solicitar confirmação para deleção.

rm -v <diretorio> - deletar arquivo e mostrar o nome do arquivo deletado.

cp <arquivo1> <arquivo2> - copiar um arquivo para o outro.

mv <arg1> <arg2> - mover arquivos ou diretórios para o destino informado.

mv -f <arg1> <arg2> - mover arquivos ou diretórios sem oferecer confirmação para remoção.

mv -i <arg1> <arg2> - mover arquivos ou diretórios solicitando confirmação para sobrescrever arquivos.

mv -v <arg1> <arg2> - mover arquivos ou diretórios exibindo o nome dos arquivos movidos.

mv <arquivo> <novoNome> - renomear um arquivo.

touch <arquivo> - criar um arquivo.

touch -t <datahora> <diretorio> - atualiza a data de criação do diretório.

cat <arquivo> - listar conteúdo de um arquivo.

cat -b <arquivo> - listar conteúdo de um arquivo numerando todas as linhas, exceto linhas em branco.

cat > <arquivo> - digitar texto no terminal e enviar para um arquivo.

cat -n <arquivo> - mostrar conteúdo do arquivo com os números das linhas.

more <arquivo> - exibir o conteúdo de um arquivo na saída padrão. Se o tamanho do arquivo não couber na tela, pressionar enter, tab ou espaço para continuar a exibição.

less <arquivo> - exibir o conteúdo de um arquivo, permitindo a negação utilizando as setas do teclado.

head <arquivo> - exibir as primeiras dez linhas de um arquivo.

tail <arquivo> - exibir as últimas dez linhas de um arquivo.

tail -f <arquivo> - exibir o conteúdo de um arquivo na medida que o mesmo cresce.

file <nomeDoArquivo> - descrever informação sobre o tipo do conteúdo do arquivo.

find <diretorioDePartida> -name <nomeDoArquivoASerProcurado> - fazer uma busca por um arquivo. 

find <diretorioDePartida> -name *.txt - fazer uma busca por um arquivo que termina com .txt.

find <diretorioDePartida> -name *txt* - fazer uma busca por um arquivo que contenha "txt" no nome.

find <diretorioDePartida> -name ewe* - fazer uma busca por um arquivo que comece com "ewe".


## Comandos de Rede e Internet:

ping <host> - verificar se o host desejado está respondendo.

ping -v <Ip> - verificar disponibilidade de endereço ip.

ping -c 3 <host> - comando ping com envio de três pacotes.

dig <dominio> - informar o DNS do domínio desejado.

host www.google.com - exibir IP do host informado.

wget <arquivo> - baixar um arquivo da internet.

dpkg -i <arquivoBaixado> -> Instala software a partir de arquivo baixado da internet.

wget -c <arquivo> - continuar baixando um arquivo pausado anteriormente.

ifconfig - visualisar informações das interfaces de rede do host.

ifconfig <interfaceDeRede> - exibir o configuração de uma placa de rede.

ip link set <interfaceDeRede> up - ativar a interface desejada.

ip link set <interfaceDeRede> down - desabilitar a interface desejada.

ifconfig <interfaceDeRede> up - ativar a interface desejada.

ifconfig <interfaceDeRede> down - desabilitar a interface desejada.

iwlist <interfaceDeRedeSemFio> scan - exibir as redes sem fio disponíveis.

netstat -i <interfaceDeRede> - mostrar estatísticas da interface de rede.

dnsdomainname - exibir o nome do domínio.

hostname - ver o nome do pc na rede.

/etc/network/interfaces - arquivo para configuração estática de interfaces de rede.

/etc/resolv.conf - arquivo para configuração de DNS.


## Comandos do Sistema:

uname - informações do kernel.

who -b - mostrar o horário de último boot do sistema.

date - exibit a data atual.

cal - exibir o calendário do mês atual.

uptime - exibir informações sobre quanto tempo o sistema está em execução, e fornecer dados sobre a carga média do sistema durante um período de tempo recente.

whoami - mostrar nome do usuário logado.

w - mostrar quem está conectado.

cat /proc/cpuinfo - mostrar informações do cpu.

cat /proc/cmeminfo - mostrar informações da memória.

man - mostrar manual de comandos.

info <comandoDesejado> - exibir informações sobre um comando desejado.

df - mostrar uso do disco.

df -h - mostrar informações do disco.

du - mostrar espaço usado no diretório.

du -dh - mostrar tamanho em GB de maneira legível por humanos.

du -m - mostrar espaço ocupado em MB.

free - mostrar memória e uso de swap.

free -t - mostrar total de memória.

fdisk -l - identificar dispositivos.

whereis <nomeApp> - mostrar possível localização de uma aplicação.

shutdown -h now - desligar o sistema.

shutdown -h 10 - desligar o sistema em 10 minutos.

shutdown -r now - reiniciar o sistema.

logout - fechar sessão.

clear - limpar a tela do terminal.


## Comandos de Gerência de usuários

cat /etc/group - arquivo que armazena informações sobre grupos do usuários do sistema.

    - nome do grupo;
    - senha criptografada;
    - GID do grupo;
    - lista de membros (separados por ,).

cat /etc/passwd - arquivo que armazena informações sobre os usuários do sistema.

    - nome de login;
    - senha criptografada;
    - UID do usuário;
    - GID do grupo padrão;
    - infos do usuário;
    - home do usuário;
    - shell.

cat /etc/shadow - arquivo que armazena informações sobre senhas dos usuários.

    - nome de login, senha criptografada;
    - data da última mudança de senha (dias passados desde 01/01/1970);
    - mínimo de dias com mesma senha (normalmente zero);
    - quantidade de dias para a senha expirar;
    - número de dias anterior a expiração para exibir alerta;
    - número de dias posterior a expiração para bloquear conta;
    - campos reservados para uso futuro.

addgroup / groupadd <nomeDoGrupo> - cria um grupo no sistema.

adduser / useradd <nomeDoUsuario> - adicionar um usuário no sistema.

useradd -G <nomeDoGrupo> <nomeDoUsuario> - criar um novo usuário e já incluí-lo em um grupo.

deluser / userdel <nomeDoUsario> - remover um usuário.

delgroup / groupdel <nomeDoGrupo> - remover um grupo.


## Comandos de Permissões

t usuário | grupos | outros

d rwx rwx rwx

U = Owner/User
G - Group
O = Other

chmod <codigoDaPermissao> - alterar permissões de um arquivo.


## Comandos Repositórios

apt install <nomeDoPacote> - instalar um pacote específico.

apt update - atualizar a lista do repositório.

apt upgrade - atualizar pacotes.

apt dist-upgrade - atualizar a distribuição.

apt-cache show <nomeDoPacote> - mostrar informações sobre  o pacote.

apt-cache depends <nomeDoPacote> - exibir dependências de um pacote.

apt-get remove --purge <nomeDoPacote> - desinstalar completamente um pacote de software, incluindo todos os seus arquivos de configuração e dados associados.

cat /etc/sources.list - exibir a lista de repositórios existentes no sistema.

apt autoclean - apagar os pacotes que não existem mais.

apt autoremove - apagar pacotes abadonados.

apt remove <nomeDoPacote> - remover um pacote específico.


## Comandos de Processos

ps aux - mostrar processos em execução com percentual de memória e CPU ocupados, dono, PID, estado.

ps lax - mostrar processos em execução e outras informações técnicas, como PID, PPID, nice, estado.

ps -eo command,ppid,pid - mostrar o comando, o PPID e o PID, nesta ordem.

top - mostrar processos de maneira dinâmica.

top -d 30 - atualizar o top a cada 30 segundos.

pstree - mostrar processos em formato de árvore.

ps -u - mostrar os processos em execução com o usuário e hora de início da execução.

kill -9 <pidDoProcesso> - parar a execução de um processo a nível de kernel.

kill -stop <pidDoProcesso> - parar o processo informado.

kill -cont <pidDoProcesso> - continuar o processo informado.

kill -stop -1 - parar todos os processos.

killall <nomeDoProcesso> - matar um processo pelo nome.

jobs - listar os processos parados ou em background.

fuser -v <diretório> - exibir e acessar o processo que utiliza determinado arquivo ou diretório.