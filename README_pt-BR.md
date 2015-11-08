# How To Git / GitHub (Português)
=================================

Como criar um repositório local?
---------------------------------

- criar uma pasta local:

<!-- language: lang-bash -->

    $ mkdir <directory>
    $ cd <directory>

- Inicializar o repositório:

<!-- language: lang-bash -->

    $ git init

- Configuração:

<!-- language: lang-bash -->

    $ git config --global user.name “Nome Sobrenome”
    $ git config --global user.email “user@server.com”

Como gerar as chaves SSH?
--------------------------

- Comprovar se existe alguma chave no PC:

<!-- language: lang-bash -->

    $ cd ~/.ssh

- Gerar uma nova chave SSH:

<!-- language: lang-bash -->

    $ ssh-keygen -t rsa -C "user@server.com"

Como pegar a chave SSH para vincular ao GitHub
-----------------------------------------------
<!-- language: lang-bash -->

    $ cat ~/.ssh/id_rsa.pub

Como clonar um repositório GitHub?
-----------------------------------

<!-- language: lang-bash -->

    $ git clone [url]

- Exemplo:

<!-- language: lang-bash -->

    $ git clone git://github.com/user/repo.git <directory>
    $ cd <directory>
    $ ls -a
    $ ls .git

Como vincular um repositório local e um outro remoto?
------------------------------------------------------

<!-- language: lang-bash -->

    $ git remote add origin git://github.com/user/repo.git

- Se os nossos dados são locais (estão no PC):

<!-- language: lang-bash -->

    $ git push -u origin master

- Se os nossos dados são remotos (estão no servidor):

<!-- language: lang-bash -->

    $ git pull origin master

Como atualizar o repositório local quando o seu origin é um fork?
------------------------------------------------------------------

- Configurar o upstream (uma vez só)

<!-- language: lang-bash -->

    $ git remote add upstream git@github.com:user/repo.git
    $ git remote -v

- Atualizar as mudanças que tiverem sido feitas no upstream.

<!-- language: lang-bash -->

    $ git fetch upstream
    $ git rebase upstream/master

Como visualizar o estado atual do repositório?
-----------------------------------------------

> o fluxo de trabalho é o seguinte:
> Seguir (Track), Modificar (Edit), Preparar (Stage), Confirmar (Commit).

![Workflow](workflow.png)

<!-- language: lang-bash -->

    $ git status

> O comando status vai dizer se houve mudanças no Diretório de
> Trabalho; se tem arquivos sem seguimento (untracked) ou se tem
> modificações preparadas (staged) para um commit.

Como preparar arquivos (Stage)?
--------------------------------

> Só os arquivos preparados (staged) vão ser adicionados na próxima
> confirmação (commit).

- Todos os arquivos:

<!-- language: lang-bash -->

    $ git add .

- arquivos específicos:

<!-- language: lang-bash -->

    $ git add <file1> <file2>

- Tipos de arquivos:

<!-- language: lang-bash -->

    $ git add *.py

Como remover arquivos preparados (staged) por erro?
----------------------------------------------------

> Pode ser que tenha adicionado arquivos ao Stage que não queria ter preparado.

<!-- language: lang-bash -->

    $ git reset HEAD

- Remover de Stage apenas um ou alguns dos arquivos:

<!-- language: lang-bash -->

    $ git reset HEAD -- <file>

Como desfazer mudanças não preparadas no Diretório de Trabalho (unestaged)?
----------------------------------------------------------------------------

> Se ainda não tem preparado as mudanças, pode desfazê-las e deixar o
> Diretório de trabalho como no último commit.

<!-- language: lang-bash -->

    $ git checkout -- <file>

Como confirmar arquivos (Commit)?
----------------------------------

> Quando estiver pronto, salve o seu trabalho.

<!-- language: lang-bash -->

    $ git commit -m "mensagem de confirmação"

- Para preparar (staged) e confirmar de uma vez:

<!-- language: lang-bash -->

    $ git commit -a -m "mensagem de confirmação"

Como visualizar o histórico de commits?
----------------------------------------

<!-- language: lang-bash -->

    $ git log

- um log com informação resumida:

<!-- language: lang-bash -->

    $ git log --oneline

Como visualizar as mudanças que se tem realizado?
--------------------------------------------------

- Para visualizar as mudanças realizadas desde que preparamos (add) e confirmamos (commit) pela última vez:

<!-- language: lang-bash -->

    $ git diff HEAD

- Para visualizar as mudanças realizadas desde um commit em particular:

> a ordem retrocedendo é: HEAD, HEAD~1, HEAD~2 ...
> HEAD~n pode ser ssubstituído também pelo identificador SHA1 do commit.

<!-- language: lang-bash -->

    $ git diff HEAD~3

- Para visualizar as mudanças entre os commits:

<!-- language: lang-bash -->

    $ git diff HEAD~3 HEAD~1

> As vezes necesitamos saber o que tem mudado desde o último 'git add' que realizamos.

- Para visualizar as mudanças realizadas que ainda não temos preparado (unstaged):

<!-- language: lang-bash -->

    $ git diff

> Antes de se fazer um commit pode ser útil saber que mudanças estaremos
> confirmando.

- Para visualizar as mudanças que já temos preparadas (staged):

<!-- language: lang-bash -->

    $ git diff --cached

- Para visualizar um resumo das mudanças realizadas temos que adicionar a opção
  --stat às instruções anteriores:

Exemplo:

<!-- language: lang-bash -->

    $ git diff HEAD --stat
    HowTo.md | 43 ++++++++++++++++++++++++++-----------------
    1 file changed, 26 insertions(+), 17 deletions(-)

Como desfazer o último Commit e voltar ao último Stage?
--------------------------------------------------------

> Se esquecemos adicionar arquivos o fazer alguma mudança antes de confirmar:

<!-- language: lang-bash -->

    $ git reset --soft HEAD~

Como voltar a um commit em particular e fazer que seja o último?
----------------------------------------------------------------

<!-- language: lang-bash -->

    $ git reset --hard SHA1

Como remover arquivos?
------------------------

<!-- language: lang-bash -->

    $ git rm <file>

Como renomear arquivos?
------------------------

<!-- language: lang-bash -->

    $ git mv <file> <new_file>

Como criar um 'galho' (Branch)?
--------------------------------

<!-- language: lang-bash -->

    $ git branch <branch>

Como selecionar outro 'galho' (Branch)?
--------------------------------------

<!-- language: lang-bash -->

    $ git checkout <branch>

Como mesclar 'branches'(galhos) (Merge)?
----------------------------------------

<!-- language: lang-bash -->

    $ git checkout master
    $ git merge <branch>

Como fusionar um grupo de commits num único commit?
---------------------------------------------------

> A veces, antes de un merge o un push, queremos reorganizar el historial
> de nuestro repositorio. Para eso, ejecutamos un rebase interactivo y editamos
> la lista de commits cambiando pick por squash a partir del segundo commit
> de la lista:

<!-- language: lang-bash -->

    $ git rebase -i HEAD~4

    pick 01d1124 Agregando licencia
    squash 6340aaa Caperucita Roja se comió al Lobo
    squash ebfd367 Jekyll se ha vuelto autoconciente
    squash 30e0ccb Modificando etiquetas

> Los commits de la lista aparecen ordenados de atrás para adelante, es decir,
> el último es HEAD y el primero es HEAD~3. Nótese que HEAD~4 no aparece en la
> lista.
