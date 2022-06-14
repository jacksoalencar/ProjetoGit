Conceitos

git - é uma sistema de versionamento capaz de suportar vários desenvolvedores 
      trabalhando no mesmo projeto. 

branch
    - é o conceito central para entendermos como trabalhar com git.
    - branch é um ramo, filial, sucursal, agência etc. 
    - exemplo: main, Master, Develop, meuProjeto etc. 


--- Master -----------o--------------------------------
   -
    -                                 
      - Develop -----o--------o-------
        -
          - minha-tela ----------------o   
            -
              ------- nova-funcionalidade ---------------


merge 
   - junção da branchs 

remote 
   - faz a ligação do meu repositório local, o repositório da minha 
     máquina, com o repositório do github 

push
   - empurra o que você fez na sua máquina para repositório 

pull
   - puxa o que esta no repositório para a sua máquina 

Histório do momento de cada comando


Você esta trabalhando no seu computador e salvando nos seus arquivos. 
   - file / save all 
          / save as 
          / save  

Você esta trabalhando no seu computador e vai transferir sua funcionaliade 
para uma Branch. Para criar uma Branch você precisa do Github. 

Baixar em http://github.com 

Após instalar: ver a versão no terminal do git com:
>git --version 
 
Vai aparecer algo parecido com:
PS C:\Users\Jackson Borges\Documents\ProjetoGit> git --version
git version 2.34.0.windows.1
PS C:\Users\Jackson Borges\Documents\ProjetoGit> 

Agora vamos criar a nome da Branch que onde você vai trabalhar:

>git init nome-da-branch 

Exemplo:

>git init desenv

Vai aparecer algo parecido com:
PS C:\Users\Jackson Borges\Documents\ProjetoGit> git init desenv
Initialized empty Git repository in C:/Users/Jackson Borges/Documents/ProjetoGit/desenv/.git/
PS C:\Users\Jackson Borges\Documents\ProjetoGit> 

Agora vamos ver onde estamos de fato trabalhando:

git status
   - para ver em qual branch você esta
   - aqui vai mostrar que eu estou na branch main


   - ..... inicio 
   - ::::: fim 
.................................................................
Jackson Borges@DESKTOP-BMQR85M MINGW64 ~/Meus Documentos/ProjetoGit (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")
:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

O comando git status mostra que Jackson esta na branch main, ele deu 
este nome para a branch.
A origem é a origin e vai para main. 
Tem um arquivo modificado que é o README.md
O github mostra que podemos add adicionar nossas modificações na branch main.
Como eu fiz alterações no arquivo README.md eu posso fazer uma commit na main.
Primeiro eu vou salvando as alterações na minha máquina.
Depois de uma periodo que achar apropriado eu faço o commit na main.
Deixando a main estável. 

Para mudar o nome da Branch para Develop:
>git branch -M "Develop"

Então temos o primeiro momento concluido. Eu faço as alterações no meu código 
e salvo na minha máquina e depois de um período eu faço commit -m na minha 
branch.  

Agora devemos fazer nossa conta no github e criar o repositório. 
Vamos agora fazer a conexão entre o minha máquina e o github.

>git remote add origin https://github.com.br/jacksonalencar/ProjetoGit

Pronto a conexão esta pronta. 

Agora vou adicionar todas os arquivos alterados:
E vou verificar com git status.
>git add .
..........................................................
PS C:\Users\Jackson Borges\Documents\ProjetoGit> git add .
PS C:\Users\Jackson Borges\Documents\ProjetoGit> git status 
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
Vemos que estamos na Branch main, que é nossa origem e 
que tem mudanças para serem comitadas. Com um arquivo 
alterado, Readme.md 

Agora vou passar para a main propriamente:

>git commit -m "texto mais completo" 

......................................
PS C:\Users\Jackson Borges\Documents\ProjetoGit> git commit -m "texto mais completo"
[main b2790e3] texto mais completo
 1 file changed, 52 insertions(+), 5 deletions(-)
PS C:\Users\Jackson Borges\Documents\ProjetoGit> 
::::::::::::::::::::::::::::::::::::

Este processo pode ser repetido sempre que sua 
versão for evoluindo. Por exemplo, depois de duas 
semanas já esta pronto então você pode fazer o 
git commit -m e depois empurrar para o repositório
principal com o comando push:

>git status 
>git commit -m "texto alterado " 
>git push -u origin main 

.........................................
PS C:\Users\Jackson Borges\Documents\ProjetoGit> git push -u origin main 
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 2.27 KiB | 581.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
To https://github.com/jacksonalencar/ProjetoGit.git
   e6b5851..580fff9  main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
PS C:\Users\Jackson Borges\Documents\ProjetoGit>
:::::::::::::::::::::::::::::::::::::::::::

Outros comandos importantes:

merge 
   - junção de duas Branch 

pull 
   - puxa o que esta no repositório do github para a sua máquina 

git checkout -b "nome-da-Branch" 
   - cria uma Branch 

pull request 
   - manda para uma Branch de um participante do githuh uma solicitação 
     que pode ou não ser aceito 

fork 
   - puxa para sua máquina publicações no github 

