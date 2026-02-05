Após realizar o PR será necessário que altere o arquivo geral.php você pode escolher em alterar diretamente no BitBucket ou rodar o comando `git clone https://{dominiodocliente.com.br}` esse comando você consegue pegar no próprio repositório clicando em Clone mudando de HTTPS para SSH.

##### Como editar o código via BitBucket
Clique em "Source" e na barra de pesquisa menor digite "geral.php" clique no arquivo e clique em Edit. A tela irá recarregar desça até achar "Config Final Deploy", você irá alterar apenas as variáveis:

$idProjetoBusca: Número do painel do cliente se não estiver no comentário do salesforce será necessário procurar no [[Painel do Busca Cliente]]
$tagmanager: Iremos gerar a tag mais pra frente
$googleSearchConsole: Iremos gerar a tag mais pra frente
$siteKey: Iremos gerar a tag mais pra frente
$secretKey:  Iremos gerar a tag mais pra frente

##### Criando as chaves do Recaptcha 
Vamos começar pelas variáveis `$siteKey e $secretKey` são as variáveis do Recaptcha abra o navegador que está logado a conta bcrelatorios após fazer o login acesse `https://www.google.com/recaptcha/admin/create`

Insira as informações conforme abaixo: ![[Pasted image 20260116152317.png]]
Após inserir as informações não é necessário nenhuma outra alteração, clique em "Enviar" a tela será recarregada com as duas chaves exatamente na ordem, o primeiro campo com o nome de chave de site será para a variável `$siteKey` e a chave secreta será para a variável `$secretKey`

Pronto, após colar essas informações no código vamos para o próximo passo.

##### Criando a chave do Google Analytics
Acesse o Google Analytics ainda na conta bcrelatorios (caso ainda funcione para criar propriedades consulte o Everton ou responsável na área de Deploy)

No canto inferior esquerdo clique na engrenagem escrito "Administrador" após acessar essa aba clique em Criar e logo após clique em "Propriedade".

Após a tela carregar insira as informações igual abaixo:![[Pasted image 20260116155235.png]]![[Pasted image 20260116155433.png]]![[Pasted image 20260116155506.png]]
Na tela abaixo selecione a plataforma "Web" irá abrir uma tela e você insere o domínio nos dois campos e clique em avançar:
![[Pasted image 20260116155708.png]]
![[Pasted image 20260116155738.png]]

Clique em Criar e Continuar, a primeira tela que abrir você pode fechar e espere a segunda tela com o nome de "Detalhes do stream Web" abrir, assim que abrir significa que o Google Analytics está feito, *Salve o ID da Métrica* vamos usar no Tag Mannager.

##### Criando as chaves do Tag Mannager
Ao abrir o Tag Mannager (https://tagmanager.google.com/?authuser=2#/container/accounts/6254899739/containers/240786148/workspaces/3) Esteja logado na conta bcrelatoriotag

Acesse qualquer domínio, clique em Administrador e no botão de + para criar um novo contêiner ![[Pasted image 20260116160554.png]]
![[Pasted image 20260116160634.png]]

Após criar volte na tela de Administrador e clique em Importar contêiner, utilize o arquivo 0 1 2.json caso não possua o arquivo solicite para o Everton ou para o responsável pela área de Deploy. Desça e clique em "Adicionar o espaço de Trabalho".

Após adicionar clique em "Variáveis" no menu esquerdo.

Selecione a única variável disponível e altere o "Título" e o valor no campo "Configuração de Variável" pelo ID da métrica que foi gerado no Google Analytics. Após realizar a troca clique em "Salvar" e após a tela fechar *Não esqueça de clicar em ENVIAR* se não nada que foi feito estará salvo no domínio. 

Clicou em "Enviar", na tela que aparecer clique em "Publicar", na próxima tela que abrir clique em "Pular" e pronto, o Tag Mannager está feito. 

Agora volte na aba "Espaços de Trabalho" e copie o número selecionado abaixo e coloca ele na variável `$tagmanager` 
![[Pasted image 20260116161500.png]]

Vamos para o Google Search.


##### Criando a Propriedade no Search Console

Acesse o site do google search console com a conta bcrelatorios5, após acessar clique no botão que está mostrando um domínio e clique em adicionar propriedade:
![[Pasted image 20260116162003.png]]

Mude para *Prefixo URL* e insira os dados igual abaixo:

![[Pasted image 20260116162100.png]]

Selecione Tag HTML, copie a tag (<meta>) cole ela dentro de um bloco de notas ou outra aba do Google Chrome e copie apenas o hash dentro do content="*hash*":
![[Pasted image 20260116162341.png]]


Após realizar isso insira a *hash* dentro da variável $googleSearchConsole e realize o commit. Caso esteja fazendo dentro do vscode será necessário rodar os comandos abaixo:

```
git add .
git commit -m "Config Deploy"
git push origin main
```

E pronto o código irá atualizar no repositório.

### Alterando o Client.inc.php
Após o e-mail do TI chegar com nome, usuário e senha você irá inserir:

'USER' = o nome que tiver menos caracteres vai nessa variável
'PASS' = a senha enviada vai aqui
'DBSA' = o nome que tiver mais caracteres vai nessa variável

Após isso realize o commit da mesma forma que fez com o arquivo geral.php
