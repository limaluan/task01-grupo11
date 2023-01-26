<div style="text-align:center" >
<img src="https://www.dbccompany.com.br/app/uploads/2022/11/Saber-evoluir-e-a-grande-revolucao.jpg" />
<h1>Task 1 - Grupo 11</h1>
<h1 style="color:blue">Git Cherry Pick</h1>
<hr />
<h2>Funcionamento</h2>
<p>O <code>git cherry-pick</code> é um comando do Git que permite escolher diferentes commits para carregar no branch selecionado. Ou seja, é a ação de pegar um commit de uma branch e aplicar em outra.</p>
<p><code>git cherry-pick</code> pode ser útil para desfazer mudanças, mas nem sempre é uma boa prática, pois pode causar commits duplicados. Esse comando não deve substituir o <code>git merge</code> e <code>git rebase</code>.</p>
<hr />
<h2>Sintaxe</h2>
Pega apenas um commit:<br/>
<code>git cherry-pick "commitID"</code><br/>
Pega um intervalo de commits:<br/>
<code>git cherry-pick 1..3 //Pega o commit 2 e 3 ignorando o 1</code><br/>
<code>git cherry-pick 1^..3  //Pega todos os commits do 1-3</code><br/>
Pega todos os commits da branch:<br/>
<code>git cherry-pick "nomeBranch"</code><br/>
<hr />
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
</p>
<hr />
<h1 style="color:blue">Referências</h1>
<li>https://git-scm.com/doc</li>
<li>https://www.atlassian.com/br/git/tutorials/cherry-pick#:~:text=O%20git%20cherry-pick%20%C3%A9,ser%20%C3%BAtil%20para%20desfazer%20altera%C3%A7%C3%B5es.</li>
<li>https://blog.geekhunter.com.br/git-cherry-pick-o-que-e-quando-usar/</li>
<li>https://coodesh.com/blog/candidates/aprenda-o-que-e-cherry-pick-do-git-e-como-aplicar-para-agilizar-seus-projetos/</li>
<hr />
</div>
