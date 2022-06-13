Conceitos

git - é uma sistema de versionamento capaz de suportar vários desenvolvedores 
      trabalhando no mesmo projeto. 

branch
    - é o conceito central para entendermos como trabalhar no git.
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
     máquina com o repositório do github 

push
   - commit o que você fez na sua máquina no repositório que você indicar

pull
   - puxa o que esta no repositório do github para a sua máquina 

Histório do momento de cada comando

Você esta trabalhando no seu computador e salvando nos seus arquivos. 
   - file / save all 
          / save as 
          / save  

Você esta trabalhando no seu computador e vai transferir sua funcionaliade 
para a Develop.

git status
   - para ver em qual branch você esta
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


