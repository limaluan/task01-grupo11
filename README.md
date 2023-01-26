<div style="text-align:center" >
<img src="https://www.dbccompany.com.br/app/uploads/2022/11/Saber-evoluir-e-a-grande-revolucao.jpg" />
<h1 align="center" >Task 01 - Grupo 11</h1>

<h1 style="color:blue">Git Rebase 🔀</h1>
<h2>• Funcionamento</h2>
<p>→ O <code style="color:red">git rebase</code> de uma branch no Git é uma maneira de <b>mover toda uma branch</b> para outro ponto da árvore, isto é, ele "pega" os commits de uma branch de origem e enfileira com os commits da branch de destino.
</p>

<h2>• Sintaxe</h2>
<code>git rebase nome_da_branch</code>

<h3>• Aplicação</h3>
<p>→ O <code style="color:red">git rebase</code> pode ser aplicado caso o desenvolvedor queira alterar o histórico de commits.<br/>
Por exemplo, digamos que temos uma branch que esteja divergente da branch master/main no ponto A:<br/><br/>
<code>
        /o-----o---o--o-----o--------- branch<br/>
--o-o--A--o---o---o---o----o--o-o-o--- master/main
</code> <br/><br/>
Ao fazer o rebase, podemos movê-la com o comando <code  style="color:red">git rebase master/main</code> assim:<br/><br/>
<code>
                                  /o-----o---o--o-----o------ branch<br/>
--o-o--A--o---o---o---o----o--o-o-o master/main
</code>
</p>
<hr/><br/>

<h1 style="color:blue">Git Cherry Pick 🍒</h1>

<h2>Funcionamento</h2>
<p>O <code>git cherry-pick</code> é um comando do Git que permite escolher diferentes commits para carregar no branch selecionado. Ou seja, é a ação de pegar um commit de uma branch e aplicar em outra.</p>
<p><code>git cherry-pick</code> pode ser útil para desfazer mudanças, mas nem sempre é uma boa prática, pois pode causar commits duplicados. Esse comando não deve substituir o <code>git merge</code> e <code>git rebase</code>.</p>

<h2>Sintaxe</h2>
Pega apenas um commit:<br/>
<code>git cherry-pick "commitID"</code><br/>
Pega um intervalo de commits:<br/>
<code>git cherry-pick 1..3 //Pega o commit 2 e 3 ignorando o 1</code><br/>
<code>git cherry-pick 1^..3  //Pega todos os commits do 1-3</code><br/>
Pega todos os commits da branch:<br/>
<code>git cherry-pick "nomeBranch"</code><br/>

<h2>Aplicação</h2>
<p>O <code>git cherry-pick</code> pode ser aplicado em um repositório como o seguinte:

a - b - c - d (main)<br/>
e - f - g  (feature)<br/>

Nesse caso se deseja usar o commit "f" na branch main. Primeiro é preciso estar na branch main:<br/>
<code>git checkout main</code><br/>
Então, executamos o cherry-pick com o seguinte comando:<br/>
<code>git cherry-pick f</code><br/>
Após a execução, o histórico do Git vai se parecer com:<br/>
a - b - c - d - f (main)<br/>
e - f - g  (feature)<br/>
O commit f foi colocado na ramificação principal com sucesso.
</p><hr/><br/>

<h1 style="color:blue">Git Revert ↩️</h1>
<h2>Funcionamento</h2>
<p>O comando <code>git revert</code> é usado para desfazer alterações ao histórico de commits do repositório. Outros comandos de "desfazer", como o <code>git checkout</code> e o <code>git reset</code>, movem os indicadores de referência do HEAD e do branch para commits especificados. O <code>git revert</code> também pega o commit específico; no entanto, o <code>git revert</code> não move os indicadores de referência para esse commit. A operação de reversão vai pegar o commit especificado, inverter as alterações dele e criar um "commit de reversão" novo. Os indicadores de referência são então atualizados para apontar para o commit de reversão novo, tornando o commit na ponta do branch.</p>
<h2>Sintaxe</h2>
<code>git revert "Commit Desejado"</code>
<p>Desfazer commits em um branch público</p>

<h2>Aplicação</h2>
<p>O comando <code>git revert</code> pode ser considerado um comando do tipo "desfazer"; no entanto, ele não é uma operação tradicional de desfazer. Em vez de remover o commit do histórico do projeto, ele descobre como inverter as alterações introduzidas pelo commit e anexa um commit novo com o conteúdo resultante. Assim, ele evita que o Git perca o histórico, o que é importante para a integridade do histórico de revisão e para uma colaboração confiável.
O comando git revert pode ser considerado um comando do tipo "desfazer"; no entanto, ele não é uma operação tradicional de desfazer. Em vez de remover o commit do histórico do projeto, ele descobre como inverter as alterações introduzidas pelo commit e anexa um commit novo com o conteúdo resultante. Assim, ele evita que o Git perca o histórico, o que é importante para a integridade do histórico de revisão e para uma colaboração confiável.

O processo de reversão deve ser usado quando você quer aplicar o inverso do commit do histórico do projeto. Isso pode ser útil, por exemplo, se você estiver acompanhando um bug e descobrir que ele foi introduzido por um único commit. Em vez de ir até ela por conta própria, corrigir e confirmar um novo snapshot, você pode usar o <code>git revert</code> para fazer tudo isso na hora.</p>
<hr/><br/>

<h1 style="color:blue">Git Squash ⏏️</h1>
<h2>Funcionamento</h2>
<p>O squash irá servir para mudarmos o histórico de nossos commits e agrupá-los de uma nova maneira, ou seja, no final podemos ter feito 20 commits, mas aplicando o essa prática, poderemos reduzir o número para 10, por exemplo.</p>
<h2>Sintaxe</h2>
<code>git log --oneline</code> Para ver lista de commits em uma linha</p>
<code>git rebase --interactive</code> Para ver uma lista de interações</P>
<code>comands: s, squash <'commit'></code> Agora basta substituir os commits</p>

<h2>Aplicação</h2>
<p>A combinação por squash permite que você combine vários commits no histórico do seu branch em um único commit. Isso pode ajudar a manter a história do seu repositório mais legível e compreensível.</p><hr/>

<h1 style="color:blue">Referências 📖</h1>
<li>https://git-scm.com/doc</li>
<li>https://www.atlassian.com/br/git/tutorials/cherry-pick#:~:text=O%20git%20cherry-pick%20%C3%A9,ser%20%C3%BAtil%20para%20desfazer%20altera%C3%A7%C3%B5es.</li>
<li>https://blog.geekhunter.com.br/git-cherry-pick-o-que-e-quando-usar/</li>
<li>https://coodesh.com/blog/candidates/aprenda-o-que-e-cherry-pick-do-git-e-como-aplicar-para-agilizar-seus-projetos/</li>
<li>https://blog.betrybe.com/git/git-rebase/</li>
<li>https://www.freecodecamp.org/portuguese/news/o-guia-definitivo-para-git-merge-e-git-rebase/</li>
<li>https://blog.betrybe.com/git/git-rebase/</li>
<li>https://www.atlassian.com/br/git/tutorials/undoing-changes/git-revert#:~:text=O%20comando%20git%20revert%20%C3%A9,do%20branch%20para%20commits%20especificados</li>
<hr />

Made by ❤️ by [Luan Lima](https://github.com/limaluan), [Mariana Machado](https://github.com/marimaccos) and [Marcklen](https://github.com/marcklen).
</div>
