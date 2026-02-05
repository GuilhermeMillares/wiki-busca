# Contribuindo para a Wiki Quartz

Obrigado por querer contribuir! Seguindo este fluxo, você poderá criar novas documentações, adicionar imagens e enviar um **Pull Request** para revisão. Depois que o PR for aprovado, o site será atualizado automaticamente.

---

## 1️⃣ Preparando o repositório

- Crie branch de desenvolvimento (`producao`) se quiser organizar PRs:
```bash
git checkout -b producao
git push -u origin producao
```
- Configure a branch protegida para exigir revisão de PRs.

---

## 2️⃣ Clonar o repositório
```bash
git clone https://github.com/GuilhermeMillares/wiki-busca.git
cd wiki-busca
```
---

## 3️⃣ Criar uma branch para a contribuição
```bash
git checkout -b minha-nova-documentacao
```
> Use nomes claros, ex: `adicionar-fluxo-deploy`.

---

## 4️⃣ Adicionar novas notas ou imagens

- Crie arquivos `.md` em `content/`.  
- Adicione imagens em `content/images/`.  
- Linke páginas com `[[Nome-da-Página]]`.

---

## 5️⃣ Comitar alterações
```bash
git add content/NovaPagina.md content/images/nova-imagem.png
git commit -m "Adiciona documentação sobre XYZ"
```
---

## 6️⃣ Subir a branch para o GitHub
```bash
git push origin minha-nova-documentacao
```
---

## 7️⃣ Criar Pull Request

1. No GitHub, clique em **Compare & pull request** na branch criada  
2. Escolha a branch de destino: `main`  
3. Adicione descrição explicando suas alterações  
4. Clique em **Create Pull Request**

---

## 8️⃣ Revisão e Merge pelo mantenedor

- Revisar o PR  
- Solicitar alterações, se necessário  
- Fazer merge quando aprovado  

> O GitHub Actions irá rebuildar o site automaticamente.

---

## Dicas

- Sempre crie **branches novas** para alterações.  
- Mantenha a **estrutura da pasta `content/`**.  
- Use nomes de arquivos **sem espaços**.  
- Links entre páginas devem usar **`[[Nome-da-Página]]`**.
