# Repo Imagem Docker GCC-GSL-GLOBES-DUNE 
> Disponível em: [Docker Hub: EinCodes/GCC-GSL-GLOBES-DUNE](https://hub.docker.com/r/eincodes/gcc-gsl-globes-dune)

[English Version](/readme_english.md)

Receita da imagem docker para criação de containers contendo as dependências necessárias para experimentos do DUNE, feita para auxiliar alunos da UTFPR e afins.

## [TL;DR](https://en.wikipedia.org/wiki/Wikipedia:Too_long;_didn%27t_read)

#### Criação do container: 
1. Instalar o Docker Desktop (https://www.docker.com/products/docker-desktop/) (Verificar os requesitos mínimos)
2. Inicializar o executavel do Docker Desktop (Isto precisa estar executando para que os comandos docker funcionem)
3. Baixar esta imagem através do terminal usando o comando `docker pull eincodes/gcc-gsl-globes-dune`
4. Criar um container desta imagem através do terminal usando o comando `docker create --name dune -it eincodes/gcc-gsl-globes-dune`

#### Operação do container através do Visual Studio Code (VSCode):
O VSCode é um editor de código fonte que possui diversas ferramentas para edição e execução de códigos em diversas linguagens de programação. Através dele é possível interagir com o ambiente criado pelo container, além de editar arquivos e executar comandos no terminal.

- Instalação:
    1. Instalar o Visual Studio Code (https://code.visualstudio.com/)
    2. Inicializar o executavel do Visual Studio Code
    3. Instalar as seguintes extensões:
        - [Visual Studio Code Marketplace • C/C++ Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack)
        - [Visual Studio Code Marketplace • Remote Explorer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.remote-explorer)
        - [Visual Studio Code Marketplace • Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
        - [Visual Studio Code Marketplace • Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)
        </br> ![VSCode aba de extensões](./assets/sample-01.png)

- Operação:
    1. Inicializar o executavel do Docker Desktop
    2. Instalar o Visual Studio Code
    3. Acessar na aba lateral esquerda o botão [Remote Explorer](./assets/sample-03.png)
    </br> ![VSCode aba de extensões](./assets/sample-02.png) 
    4. Clicar no botão `Attach In New Window` ao lado do container dune para abrir o container em uma nova janela
    </br> ![VSCode aba de extensões](./assets/sample-04.png)
    5. Na nova janela, clicar em `Open Folder` para abrir uma pasta de trabalho (ex: `/usr/src/user/`)
    </br> ![VSCode aba de extensões](./assets/sample-05.png)

#### Operação do container através da linha de comando:
É possível interagir com o ambiente criado pelo container em qualquer terminal, porém sem auxílio de nenhuma interface gráfica. Após inicializar o container em modo interativo, é possível editar, compilar e executar programas usando apenas a linha de comando, caso possua experiência.

1. Para inicializar o container usar o comando `docker start -i dune` (após isso será possivel usar a linha de comando do ambiente)
2. Para interromper o container, **através  da linha de comando do ambiente**, usar o comando `exit` 
3. Para interromper o container usar o comando `docker stop dune`

## Diretório Uteis
- /usr/src/user/examples/globes (ex: `/usr/src/user/examples/globes/example1.sh`)
- /usr/src/user/dune (ex: `/usr/src/user/dune/dune_globes/DUNE_GLoBES.glb`)

## Dependências:
- GCC: 13.2.0
- GSL: 2.7.0
- GLOBES: 3.2.18

## Testado em:
Desktop:
- Processador Intel Core i7-10700 2.90 GHz
- 32GB Memória RAM DDR5 & 2TB SSD M2
- Windows 11 Pro x64 (64 Bits)

Notebook:
- Processador Intel Celeron N4000 1.10/2.60 GHz
- 4GB Memória RAM DDR4 & 256GB SSD M2
- Windows 11 Home Single Language x64 (64 Bits)

## Licença
O código-fonte do está licenciado sob a licença MIT, que você pode encontrar no arquivo MIT-LICENSE.txt
[MIT-LICENSE.txt](/MIT-LICENSE.txt)
