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
<br/>
<h1 style="color:blue">Git Revert</h1>
<hr />
<h2>Funcionamento</h2>
<p>O comando <code>git revert</code> é usado para desfazer alterações ao histórico de commits do repositório. Outros comandos de "desfazer", como o <code>git checkout</code> e o <code>git reset</code>, movem os indicadores de referência do HEAD e do branch para commits especificados. O <code>git revert</code> também pega o commit específico; no entanto, o <code>git revert</code> não move os indicadores de referência para esse commit. A operação de reversão vai pegar o commit especificado, inverter as alterações dele e criar um "commit de reversão" novo. Os indicadores de referência são então atualizados para apontar para o commit de reversão novo, tornando o commit na ponta do branch.</p>
<hr />
<h2>Sintaxe</h2>
<code>git revert "Commit Desejado"</code>
<p>Desfazer commits em um branch público</p>

<hr />
<h2>Aplicação</h2>
<p>O comando <code>git revert</code> pode ser considerado um comando do tipo "desfazer"; no entanto, ele não é uma operação tradicional de desfazer. Em vez de remover o commit do histórico do projeto, ele descobre como inverter as alterações introduzidas pelo commit e anexa um commit novo com o conteúdo resultante. Assim, ele evita que o Git perca o histórico, o que é importante para a integridade do histórico de revisão e para uma colaboração confiável.
O comando git revert pode ser considerado um comando do tipo "desfazer"; no entanto, ele não é uma operação tradicional de desfazer. Em vez de remover o commit do histórico do projeto, ele descobre como inverter as alterações introduzidas pelo commit e anexa um commit novo com o conteúdo resultante. Assim, ele evita que o Git perca o histórico, o que é importante para a integridade do histórico de revisão e para uma colaboração confiável.

O processo de reversão deve ser usado quando você quer aplicar o inverso do commit do histórico do projeto. Isso pode ser útil, por exemplo, se você estiver acompanhando um bug e descobrir que ele foi introduzido por um único commit. Em vez de ir até ela por conta própria, corrigir e confirmar um novo snapshot, você pode usar o <code>git revert</code> para fazer tudo isso na hora.</p>
<hr />
</div>
