<div style="text-align:center" >
<img src="https://www.dbccompany.com.br/app/uploads/2022/11/Saber-evoluir-e-a-grande-revolucao.jpg" />
<h1>Task 1 - Grupo 11</h1>
<h1 style="color:blue">Git Rebase</h1>
<h2>• Funcionamento</h2>
<p>→ O <code style="color:red">git rebase</code> de uma branch no Git é uma maneira de <b>mover toda uma branch</b> para outro ponto da árvore, isto é, ele "pega" os commits de uma branch de origem e enfileira com os commits da branch de destino.
</p>
<hr />
<h2>• Sintaxe</h2>
<code>git rebase nome_da_branch</code>
<hr />
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
<!-- <code>Colocar aplicação aqui</code> -->
<hr />
</div>
