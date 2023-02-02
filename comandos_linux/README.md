# Comandos para terminal Linux
## Comandos Gerais
* `sudo apt-get nome_do_aplicativo` - Instala o app desejado;
* `sudo apt-get search nome_do_aplicativo` - Pesquisa um aplicativo na loja pelo nome inserido;
* `ifconfig` - Informa o endereço IP da máquina;
## GitHub
### Login por chave ssh
* `ssh-keygen -t ed25519 -C "algum_comentario"` - Gerará uma chave SSH;
* `xclip -sel clip < ~/.ssh/id_ed25519.pub` - Copia a chave SSH gerada;
* Ir ao seu perfil no GitHub no navegador;
* Abrir as configurações;
* Ir até "SSH and GPG keys";
* Selecionar "New SSH key";
* Inserir um título coerente a sua tarefa e no campo abaixo inserir a chave gerada no terminal;
* Ir no terminal e definir seu usuário como global com:
    * `git config --global user.email "emaildeusuariodogit@email.com"`;
    * `git config --global user.name "nomedeusuariodogit"`
### Commits e clone de repositórios 
* `git clone chave_do_repositório` - Clona um repositório do GitHub;
* `git status` - Verifica o status do upload dos arquivos;
* `git add .` - Insere todos os arquivos para upload;
* `git commit -m "alguma mensagem"` - Upload dos arquivos;
* `git push` - Envia as alterações para o repositório;
* `git pull` - Instala as alterações do repositório;
* `git branch` - Lista as branches do repositório no computador;
* `git branch -a` - Lista as branches do repositório remoto;
* `git checkout nome-da-branch` - Troca para a branch informada no comando;


# Comandos gerais no uso do software
* `Super + D` - Mostra todas as guias abertas na área de trabalho;
* `Alt + Tab` - Troca rápida de guia;
* `Super + '` - Troca rápida de guia;
* `Super + T` - Abre um novo terminal;
* `Super` - Amostra resumida das guias abertas;
* `Super + F` - Abre o gerenciador de arquivos;