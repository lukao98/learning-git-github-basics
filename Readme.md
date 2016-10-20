#Git
Git é um sistema de controle de versão. Diferente dos outros sistemas, ele atua com o "estado" dos arquivos, com os famosos snapshots.
A empresa BitKeeper guardava todo o codigo do kernel e após uma desavença da BitKeeper com a Linux Foundation, Linus Torvalds ficou decidido em fazer um sistema de versionamento e então o Git nasceu trazendo algumas melhorias, tais como: Maior velocidade, um design mais simples, facilidade para lídar com projetos grandes, etc...

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

- git config --global user.name ""  
- git config --global user.email ""  
- git config --global core.editor ""  
- git config --list  
  
 
- mkdir [nome da pasta] <-- Cria a pasta  
- cd [nome da pasta] <- Acessa a pasta  
- git init <- Repositório  
- ls -la <- infos   
  
  
- git status <- Status do repositório
- git add <- Adiciona arquivos do diretório
- git commit -m <- Commita com uma mensagem
- git diff <- Mostra as mudanças  
- git diff --name only <- Mostra o nome dos arquivos modificados  
- git checkout <- Volta para a versão anterior  
- git reset HEAD(volta para o ponteiro) <- Tira do stage  
- git reset --soft <- Mata o commit, mas o arquivo está pronto para ser commitado  
- git reset --mixed <- Volta para antes do staged(modified)  
- git reset --hard <- Ignora tudo o que foi feito  
- git stash <- Não manda a mudança, guarda ela (ainda trabalhando nela)  
- git config --global alias.s status <- Configuração de hotkey com exemplo  
- git rever [codigo commit] <- Ele volta, mas não perde o commit bugado  
  
Logs  

- git log <- logs  
- git log --decorate <- Informações  
- git log --author "" <- logs por autor  
- git shortlog <- ordem alfabetica dos logs, quais commits e quantos commits  
- git shortlog -sn <- quantos commits e pessoas  
- git show [codigo] <- commits  
  
 
  
  
Acesso remoto   

- git remote add  <- Adiciona endereço remoto
- git remote <- Mostra qual endereço remoto esta
- git remote -v <- Endereço  
- git push -u [pra onde] [branch que estou] <- Manda pro repositório      
- g clone [endereço] [novo nome] <- Clona 
  
 
BRANCHS    
  
- git checkout -b [nome] <- Cria um branch  
- git branch <- Lista os branchs e destaca o que você esta usando  
- git checkout [nome] <- muda para este branch  
- git branch -d <- Deleta o branch  
