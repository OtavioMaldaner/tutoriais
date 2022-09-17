# Tutorial de preparação de ambiente para trabalhar com React Native
Passo a passo para instalação das ferramentas necessárias para rodar a aplicação<br>
## Passo 1: Ter as permissões para a instalação completa
- Executar o PowerShell como administrador
- Executar o comando `Get-ExecutionPolicy` para verificar as suas permissões para seguir a instalação
    - Caso o retorno do comando seja "Restricted", basta rodar o comando `Set-ExecutionPolicy AllSigned` e ativar a permissão para todos;
## Passo 2: Instalação do choco
- Executar o comando `Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))` para a instalação do choco
    - Para verificar se a instalação foi bem sucedida, basta executar o comando `choco`;
## Passo 3: Instalação do Node.JS
- Executar o comando `choco install nodejs-lts`
- Para verificar se a instalação foi bem sucedida, basta reiniciar a aplicação do PowerShell e executar o comando `node -v`
    - É importante verificar se o gerenciador de pacote "npm" foi instalado corretamente. Para isso, execute o comando `npm -v`;
    - Caso queira, você pode verificar a versão do Java que foi instalada com o comando `java --version`;
- É necessário instalar a dependência "yarn". Execute a linha de comando `choco install yarn` e pressionar a tecla 'a' quando for requisitada a instalação dos demais pacotes
    - Para verificar se a instalação foi concluída com sucesso, basta reiniciar o PowerShell e executar o comando `yarn -v`;
- A dependência "yarn" deve ser global. Execute o comando `yarn global bin`. <br>
**Importante:** Armazene o caminho que aparecerá na execução do comando pois será importante mais tarde
- Execute o comando `choco install openjdk`;
## Passo 4: Alterar as variáveis de ambiente
- Abra o Explorador de Arquivos e vá até `Este Computador\C:` e crie uma pasta chamada "Android"
- Entre na pasta recém criada e crie uma outra pasta chamada "Sdk"
- Entre na pasta "Sdk" e copie o caminho da pasta
- Pressione a tecla "Iniciar" do Windows e digite "Editar as variáveis de ambiente do sistema"
- Selecione a opção "Variáveis de Ambiente..."
- Crie uma variável de ambiente nova no seu usuário com o nome "ANDROID_HOME" e no valor da variável cole o caminho da pasta "Sdk"
- Crie uma variável com o nome "JAVA_HOME" e com o caminho até a pasta "jdk-versão-instalada"
- Entre na vaiável "Path" e vá em editar. Adicione as variáveis:
    - %ANDROID_HOME%\emulator
    - %ANDROID_HOME%\tools
    - %ANDROID_HOME%\tools\bin
    - %ANDROID_HOME%\platform-tools
    - Verifique se o caminho que apareceu na instalação do "yarn" já está é uma variável de ambiente. Caso não seja, cole o caminho que apareceu na instalação da mesma;
    - Clique em Ok e aplique as alterações feitas clicando em Ok novamente na tela de Variáveis de Ambiente;
## Passo 5: Instalação do Android Studio
- Acesse o site do [Android Studio](https://developer.android.com/studio) e clique no botão "Download Android Studio"
- Pode seguir a instalação com todas as configurações padrão do dedsenvolvedor;
- QUando o Android Studio estiver executando:
    - Selecione a opção "Do not import settings";
    - Ao pedir se deseja enviar os dados para análise do Google selecione a opção que desejar;
    - Selecione "next" e em seguida "Custom", para a configuração personalizada do Android Studio;
    - Na janela "Select default JDK Location", selecione a variável "JAVA_HOME", criada anteriormente;
    - Selecione o tema de sua preferência. Recomendo fortemente o uso do tema "Darcula";
    - Na tela "SDK Components Setup" selecione todas as opçõese altere o Location para a pasta criada em `C:\Android\Sdk`;
    - Selecione next, aceite os termos e finalize a instalação;
        - Caso a instalação foi em um computador com processador AMD, assista [este vídeo](https://www.youtube.com/watch?v=Y1WhS2yuF8I) para resolver o problema;
## Passo 6: Instalação do Visual Studio Code
- Acesse o site do [Visual Studio Code](https://code.visualstudio.com) e clique no botão "Download for Windows"
- Aceite os termos e dê next em todas as opções que aparecer e finalize a instalação clicando em "Consluir";
# Conclusão
Tutorial feito com base no vídeo: [Como configurar ambiente React Native no Windows - 2022](https://www.youtube.com/watch?v=4_zDCS2fVAU) <br>
By: Otávio João Maldaner <br>
17/09/2022 <br>
Bom Princípio - RS
