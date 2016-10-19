#Git
Git é um sistema de controle de versão. Diferente dos outros sistemas, ele atua com o "estado" dos arquivos, com os famosos snapshots.
A empresa BitKeeper guardava todo o codigo do kernel e após uma desavença da BitKeeper com a Linux Foundation, Linus Torvalds ficou decidido em fazer um sistema de versionamento e então o Git nasceu trazendo algumas melhorias, tais como: Maior velocidade, um design mais simples, ele consegue lídar com projetos grandes, etc...

##O que é "Github"?
É um serviço web onde são acoplados os projetos que usam o sistema Git.

##Ciclo de vida dos arquivos
-Untracked: Momento em que o arquivo acabou de ser adicionado no repositório.
-Unmodified: O arquivo não sofreu alterações.
-Modified: O arquivo foi modificado.
-Staged: Depois de modificado, você pode jogar esse arquivo em uma área onde você cria uma versão, essa área se chama staged.

##O que é um branch?
Branch é um ponteiro móvel que aponta para um commit. Você tem o principal, que é o "master" e poderá criar outros.

###Merge e Rebase
Suponha-se que você tenha a branch master e mais uma, para você agrupar essa branch nova no master usará um desses comandos.

-Merge: Branch Master com o projeto e Branch Feature com uma nova funcionalidade. Após terminar o desenvolvimento do Feature eu jogo ele no Master, porém no log dará apenas como mais um commit.

-Rebase: Ele faz a mesma coisa que o merge, porém ele reescreve um log da branch, fazendo um commit novo para cada commit ajudando na organização.

#Repositório no Github
1. Clica no "+" do lado da sua foto e em novo repositório
2. De um nome para ele
3. Clica em criar
4. Bom uso

###Forks no github
Você pega a cópia do repositório de alguém, mas o repositório orignial fica intacto. Muito usado para fazer contribuições em projetos.


#Comandos
Por fim, passarei comandos básicos que vocês usarão muito.
*git config --global user.name ""
*git config --global user.email ""
*git config --global core.editor ""
*git config --list


-mkdir git-course <- Cria a pasta
-cd git-course <- Acessa a pasta
-git init <- Repositório
-ls -la <- infos
-cd. git/ <- visualiza


-git status <- como está o repositório
-git add <- adiciona
-git commit -m <- mensagem
-git diff <- mostra as mudanças
-git diff --name only <- mostra o nome dos arquivos modificados
-git checkout <- volta para a versão anterior
-git reset HEAD(volta para o ponteiro) <- tira do stage
-git reset --soft <- mata o commit, mas o arquivo está pronto para ser commitado
-git reset --mixed <- Volta para antes do staged(modified)
-git reset --hard <- Ignora tudo o que foi feito
-git stash <- Não manda a mudança, guarda ela (ainda trabalhando nela)
-git config --global alias.s status <- configuração de hotkey com exemplo
-git rever [codigo commit] <- Ele volta, mas não perde o commit bugado

=====logs======
-git log <- logs
-git log --decorate <- informações
-git log --author "" <- logs por autor
-git shortlog <- ordem alfabetica dos logs, quais commits e quantos commits
-git shortlog -sn <- quantos commits e pessoas
-git show [codigo] <- commits

===============


=====Acesso remoto=======
-git remote add
-git remote <- mostra qual
-git remote -v <- endereço
-git push -u [pra onde] [branch que estou] <- manda pro repositório
-git push [pra onde] [branch que estou] <- manda modificações
-g clone [endereço] [novo nome]

========================

==================BRANCHS

-git checkout -b [nome] <- cria um branch
-git branch <- lista os branchs e destaca o que você esta usando
-git checkout [nome] <- muda para este branch
-git branch -d <- Deleta o branch
