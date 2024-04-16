# pratica-git
repositório para praticar comandos do git

~~~bash
git config --global core.editor"code --wait"
~~~
o comando acima define o visual studio code como o editor padrao das mensagens de commit

~~~bash
git commit --allow-empty
~~~
o parametro `--allow-empty` permite a criaçao de um commit vazio,para fins de testes e praticas do git.

~~~bash
git commit -a
~~~
o parametro`a` adiciona todos os arquivos modificados ou nao ignorados ao commit atual.

~~~bash
git checkout -b novobranch
~~~
o parametro `-b` alterna para `novobranch`criando o branch . o mesmo acontece com o comando `git switch` com o parametro`-c`.

~~~bash
git branch -d nomebranch
git push --delete origin nomebranch
~~~
para apagar um branch e preciso apaga-lo localmente e depois propagar a deleçao para o repositorio remoto.(segundo comando).

~~~bash
git log --graph --oneline
~~~
o comando `log` exibe o historico de commits em detalhes . com as flags `--graph` e `--oneline` exibe o historico em um formato mais compreensivel, atraves de um graph
### rebase interativo
para alterar o autor de um commit, você pode utilizar o rebase interativo e o comando `commit --amend`.
antes porem,verifique se o editor de mensagens de commits esta configurado para o editror do proprio vscode
~~~bash
git rebase -i <referencias>
~~~
a referencia do commit deve ser sempre para o commit anterior ao commit que deve ser alterado.


no editor de commits ,altere a instruçaodo commit desejado  de `pick`
para `edit`.em seguida grave e feche o editor.

o rebase fara uma pausa para que voce altere as informaçoes do autor .

~~~bash
git commit --amend --reset-author --no-edit
~~~
caso voce queira especificar o autor,utilize a flag `--author-"nome do autor <email>"`, nesse nesse exato formato

caso seu commit seja vazio acrescente ainda a flag `--allow-empty`

apos o reparo do commit, continue o processo do rebase com o comando abaixo.

~~~bash
git rebase --continue
~~~
finalmente ,**confira o novo usuario**

