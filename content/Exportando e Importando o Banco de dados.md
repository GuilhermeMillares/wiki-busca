Após verificar a propagação do DNS acesse: `dominiodocliente.com.br/phpmyadmin` ao acessar a tela insira os dados que foram colocados nas variáveis *'USER' e 'PASS'* que estão no código.

Acesse também deploy.buscaclientes.com.br e insira as informações que está um pouco mais acima das anteriores no código, elas está abaixo da linha comentada escrito // DEPLOY.

Após inserir irá receber alguns avisos, clique em ignorar tudo (todas as vezes que aparecer). 

Dentro do deploy.buscaclientes clique no banco existente, ele vai estar abaixo de "Novo BD" após selecionar, clique em "EXPORTAR" igual abaixo:![[Pasted image 20260116173039.png]]
Clique em ignorar tudo e Executar novamente para realizar o download do banco.

Após realizar o Download do banco acesse dominiodocliente.com.br/phpmyadmin insira as credenciais para fazer o acesso e repita o processo porém dessa vez não clique em "EXPORTAR" mas clique em *IMPORTAR*![[Pasted image 20260116173305.png]]
>[!IMPORTANTE]
>Selecione o banco do cliente que estará abaixo do botão Novo

Selecione o arquivo do banco, desça tudo e clique em *Importar* e pronto banco de dados importado.
