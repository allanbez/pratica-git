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