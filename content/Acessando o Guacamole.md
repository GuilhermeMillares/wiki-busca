Acesse o [[Guacamole]] e pesquise pelo domínio do cliente, após achar acesse o servidor e rode os comandos abaixo:
```
cd web
cd dominiodocliente.com.br (você pode digitar cd e apertar tab tab, que ele irá completar)
cd public_html
ls (se tiver apenas os arquivos index.html e robots.txt rode o comando abaixo) 
rm * -r
```

Após realizar esse procedimento é necessário gerar a chave SSH para conseguir realizar o Git clone então será necessário rodar os comandos abaixo:
```
ssh-keygen -t rsa -b 4096 -C "contato@buscacliente.com.br" 
(após o comando acima aperte Enter três vezes e sua chave será zerada)
cat ~/.ssh/id_rsa.pub
```

Copie a saída completa do comando cat e acesse novamente o bitbucket e siga o passo a passo abaixo:
![[Pasted image 20260116163724.png]]
![[Pasted image 20260116163807.png]]

Clique em Add Key, no nome você irá colocar o domínio do cliente e no campo Key adicione a saída do seu comando cat, clique em Add Key e pronto. Agora volte ao repositório e clique no botão Clone, troque de HTTPS para SSH copie o comando e no final do comando adicione *public_html* igual abaixo

```
git clone git@bitbucket.org:busca-clientes/dominiodocliente.com.br.git public_html
yes (será solicitado que digite)
```

E cole esse comando no servidor e espere ele finalizar, assim que finalizar pode digitar Exit e voltar para o menu principal.
