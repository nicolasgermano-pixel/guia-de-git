# repositório

Um repositório é a pasta `.git` onde o Git guarda a história inteira do
projeto: todos os commits, todas as referências e todos os objetos.

O diretório de trabalho fica ao lado dela, e não dentro. Ao rodar
`git clone`, é o repositório que é copiado; o diretório de trabalho é
montado a partir dele.

<!-- este arquivo é um exemplo de entrada: pode ser apagado ou mantido -->

aluno@LAB205 MINGW64 ~
$ cd ~/Documents

aluno@LAB205 MINGW64 ~/Documents
$ mkdir receitas

aluno@LAB205 MINGW64 ~/Documents
$ cd receitas

aluno@LAB205 MINGW64 ~/Documents/receitas
$ pwd
/c/Users/aluno.UDICENTRO/Documents/receitas

aluno@LAB205 MINGW64 ~/Documents/receitas
$ printf "protocol=https\nhost=github.com\n\n" | git credential reject

aluno@LAB205 MINGW64 ~/Documents/receitas
$ git clone https://github.com/nicolasgermano-pixel/guia-de-git.git
Cloning into 'guia-de-git'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 6 (delta 0), reused 4 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (6/6), done.

aluno@LAB205 MINGW64 ~/Documents/receitas
$ git config user.name "Nicolas"
fatal: not in a git directory

aluno@LAB205 MINGW64 ~/Documents/receitas
$ guia-de-git
bash: guia-de-git: command not found

aluno@LAB205 MINGW64 ~/Documents/receitas
$ cd guia-de-git

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (main)
$ config user.name "Nicolas"
bash: config: command not found

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (main)
$ git config user.name "Nicolas"

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (main)
$ git config user.email "nicolas.germano@estudante.iftm.edu.br"

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (main)
$ git swith -c nicolas
git: 'swith' is not a git command. See 'git --help'.

The most similar command is
        switch

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (main)
$ git switch -c <Nicolas>
bash: syntax error near unexpected token `newline'

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (main)
$ git switch -c nicolas
Switched to a new branch 'nicolas'

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (nicolas)
$ notepad glossario/commit.md

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (nicolas)
$ git add .

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (nicolas)
$ git commit -m "Acrescenta a entrada clone"
[nicolas be3aa6a] Acrescenta a entrada clone
 1 file changed, 14 insertions(+)
 create mode 100644 glossario/commit.md

aluno@LAB205 MINGW64 ~/Documents/receitas/guia-de-git (nicolas)
$ git push -u origin nicolas
