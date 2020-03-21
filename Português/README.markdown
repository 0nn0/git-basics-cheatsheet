# Git Cheatsheet (Fundamentos)

Esta cheatsheet é uma lista dos comandos Git mais usados por nós, além de conter informações úteis para quem está começando.

*Quer aprender mais sobre o terminal? Há uma lista dos comandos e atalhos mais usados por nós no [Terminal do macOS](https://github.com/0nn0/terminal-mac-cheatsheet/tree/master/Português).*

## Glossário

| Palavra-chave              | Descrição                                                                                                |
| -------------------------- | -------------------------------------------------------------------------------------------------------- |
| git                        | Sistema de controle de versão distribuída de código aberto usado para armazenar código em repositórios   |
| GitHub, GitLab e Bitbucket | Plataformas para hospedagem de repositórios Git                                                           |
| staging                    | Arquivos ou diretórios que você deseja *commitar*                                                        |
| commit                     | Salva todos os arquivos ou diretórios *staged* no seu repositório local                                  |
| branch                     | Ramifica o desenvolvimento de forma independente para que recursos possam ser desenvolvidos isoladamente |
| clone                      | Clona os *commits* e as *branches* da versão remota do repositório para uma nova versão local            |
| remote                     | Versão remota e comum a todos os colaboradores                                                           |
| fork                       | Copia um repositório pertencente a outro usuário gerando um repositório em seu nome                      |
| pull request               | Solicita a fundição de suas contribuições a um repositório                                               |
| HEAD                       | Sua posição no diretório de trabalho atual                                                               |

## Configuração

| Comando                                   | Descrição                                                              |
| ----------------------------------------- | ---------------------------------------------------------------------- |
| `git config --global user.name [nome]`    | Define o nome do autor a ser usado em todas as *commits*               |
| `git config --global user.email [e-mail]` | Define o endereço de e-mail do autor a ser usado em todas as *commits* |
| `git config color.ui true`                | Altera a cor da UI do terminal                                         |

## Comandos Principais

| Comando                      | Descrição                                                                                 |
| ---------------------------  | ----------------------------------------------------------------------------------------- |
| `git init [diretório]`       | Cria um novo repositório local                                                            |
| `git clone [repo]`           | Cria uma cópia local do repositório remoto                                                |
| `git add [diretório]`        | Prepara o diretório para o *commit*                                                       |
| `git add [arquivo]`          | Prepara o arquivo para o *commit*                                                         |
| `git add -A`                 | Prepara todos os arquivos alterados para o *commit*                                       |
| `git add .`                  | Prepara os arquivos novos e os com modificação e ignora os deletados para o *commit*      |
| `git add -u`                 | Prepara os arquivos deletados e os com modificação e ignora os novos para o *commit*      |
| `git commit -m "[mensagem]"` | *Commita* todos os arquivos e diretórios que foram preparados para o *commit*             |
| `git status`                 | Mostra o status dos arquivos ou diretórios como não rastreados, modificados ou preparados |

## Sincronização de Alterações

| Comando     | Descrição                                                                          |
| ----------- | ---------------------------------------------------------------------------------- |
| `git fetch` | Baixa todo o histórico das *branches* remotas                                      |
| `git merge` | Anexa a *branch* remota na *branch* local                                          |
| `git pull`  | Atualiza a *branch* local com os novos *commits* da *branch* remota correspondente |
| `git push`  | Envia todos os *commits* locais para o repositório remoto                          |

*Dica: `git pull` é a combinação de `git fetch` com `git merge`*

## Desfazer Alterações

| Comando                     | Descrição                                                                 |
| --------------------------- | ------------------------------------------------------------------------- |
| `git checkout -- [arquivo]` | Substitue o arquivo pelo conteúdo da *HEAD*                               |
| `git revert [commit]`       | Cria um novo *commit* que desfaz as alterações feitas em [commit]         |
| `git reset [arquivo]`       | Remove o [arquivo] da área de preparação                                  |
| `git reset --hard HEAD`     | Remove todas as alterações locais no diretório de trabalho atual          |
| `git reset --hard [commit]` | Redefine o *HEAD* para o *commit* anterior e descarta todas as alterações |

## Branches

| Comando                    | Descrição                                  |
| -------------------------- | ------------------------------------------ |
| `git branch [branch]`      | Cria uma nova *branch*                     |
| `git checkout [branch]`    | Vai à *branch*                             |
| `git checkout [branch] -b` | Cria e vai à nova *branch*                 |
| `git merge [branch]`       | Anexa a *branch* [branch] à *branch* atual |
| `git branch -d [branch]`   | Deleta a *branch*                          |
| `git push origin [branch]` | Envia a *branch* para o repositório remoto |

## Histórico

| Comando                    | Descrição                                                           |
| -------------------------- | ------------------------------------------------------------------- |
| `git log`                  | Lista o histórico de versões da *branch* atual                      |
| `git log --author=[nome]`  | Lista o histórico de versões da *branch* atual filtrada por autor   |
| `git log --oneline`        | Lista o histórico de versões da *branch* atual de forma compacta    |
| `git show [commit]`        | Lista os metadados e alterações feitas em um *commit* específico    |
| `git blame [arquivo]`      | Mostra quem fez alterações em um arquivo e quando elas foram feitas |         |

## Gitignore

Adicionar o arquivo reservado para o sistema `.gitignore` ao seu diretório permite que você opte pela exclusão de certos arquivos de futuros *commits*. Este arquivo deve ficar sempre na raiz do seu repositório.

Nota-se que muita gente costuma excluir caches de dependência, como o `node_modules`, arquivos de sistema, como o `.DS_Store`, entre diversos outros.

Você pode ver o `.gitignore` [deste repositório](https://github.com/0nn0/git-basics-cheatsheet/blob/master/.gitignore) ou [mais exemplos](https://github.com/github/gitignore) do GitHub.

## Plataformas

As plataformas abaixo são exemplos que podem ser usados para hospedar seus repositórios.

| Plataforma                         | Preço  |
| ---------------------------------- | ------ |
| [GitHub](https://github.com)       | Grátis |
| [GitLab](https://gitlab.com)       | Grátis |
| [Bitbucket](https://bitbucket.org) | Grátis |

## Cliente de Interface do Usuário (GUI)

O terminal não é sua praia? Use um dos clientes abaixo.

| Cliente                                     | Sistema Operacional | Preço     |
| ------------------------------------------- | ------------------- | --------- |
| [GitHub](https://desktop.github.com)        | macOS e Windows     | Grátis    |
| [Sourcetree](https://www.sourcetreeapp.com) | macOS e Windows     | Grátis    |
| [Tower](https://www.git-tower.com)          | macOS e Windows     | $69 a $99 |
