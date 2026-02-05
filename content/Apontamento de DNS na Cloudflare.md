Acesse a CloudFlare entre na conta do Growth e clique em *Integrar um domínio*.

Realize a configuração igual abaixo:![[Pasted image 20260116164719.png]]

Clique em Continuar e selecione o plano free, desative o proxy.
![[Pasted image 20260116164810.png]]

Exclua qualquer registro que seja NS e AAAA.

Antes de alterar o IP do domínio verifique se nenhum MX ou outra configuração de webmail esteja apontada para o domínio, caso esteja altere o apontamento de domínio para o IP do domínio (o antigo e não o que o nosso TI te enviou), após verificar e realizar as alterações para que tudo funcione, troque o registro A para o IP que o nosso TI enviou, e adicione um CNAME www @ (pois assim ele irá apontar para o domínio)

>Altere apenas o registro do domínio, caso tenha outro como por exemplo: ftp, não altere o IP dele.

Clique em continuar para a Ativação. 

Agora vá até o registro.br e altere os DNS que estão lá por esses que apareceram na tela após avançar da etapa anterior.

Após alterar, envie o e-mail para o TI realizar a "Ativação de SSL" aguarde o TI enviar que conseguiu realizar a ativação do SSL e verifique a propagação do DNS (se ele já está com o IP que você colocou ou não). Para realizar a verificação acesse o dnschecker.org
