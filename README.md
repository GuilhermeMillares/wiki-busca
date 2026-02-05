# Documentação Quartz Wiki

Este repositório contém uma wiki/documentação criada com **Quartz 4** e **Obsidian**, permitindo que você organize suas notas em Markdown e publique um site estático automaticamente usando **GitHub Pages** e **GitHub Actions**.

---

## Estrutura do Repositório

Documentacao/
    content/                # Conteúdo da wiki (Markdown e imagens)
    public/                 # Site gerado pelo Quartz (não versionado)
    quartz.config.ts        # Configuração do Quartz
    package.json            # Dependências do projeto
    .github/workflows/      # GitHub Actions para deploy automático
    README.md               # Este arquivo

---

## Como usar localmente

1. Clone o repositório:
```bash
    git clone git@github.com:GuilhermeMillares/documentacao.git
    cd documentacao
```
2. Instale as dependências:
```bash
    npm install
```
3. Gere o site localmente:
```bash
    npx quartz build
```

4. O site gerado estará na pasta `public/`. Você pode abrir localmente com um servidor estático (ex.: VSCode Live Server).

---

## Fluxo de publicação

Este repositório utiliza **GitHub Actions** para gerar e publicar automaticamente o site Quartz na branch **gh-pages**.

- Toda vez que você fizer push na branch `main`, o workflow irá:
    1. Instalar dependências do projeto
    2. Rodar `npx quartz build` para gerar a pasta `public/`
    3. Publicar o conteúdo de `public/` no GitHub Pages

- O site estará disponível em:

    https://guilhermemillares.github.io/wiki-busca/

---

## Estrutura do conteúdo

- Todos os arquivos de documentação e imagens ficam na pasta `content/`.
- Links entre páginas usam o formato **Obsidian-style** `[[nome-da-página]]`.
- Quartz processa esses links automaticamente no site gerado.

---

## Adicionando novas notas

1. Crie novos arquivos Markdown dentro de `content/`.
2. Adicione links no arquivo `index.md` ou em outras páginas conforme necessário.
3. Commit e push das alterações na branch `main`.
4. O site será atualizado automaticamente via GitHub Actions.

---

## Ignorar arquivos

- A pasta `public/` é gerada pelo Quartz e **não deve ser versionada**.
- O repositório ignora arquivos de configuração do Obsidian (`.obsidian`) e outros arquivos privados.

---

## Referências

- [Quartz 4 Documentation](https://quartz.jzhao.xyz/)
- [Obsidian](https://obsidian.md/)
- [GitHub Pages](https://pages.github.com/)
- [GitHub Actions](https://docs.github.com/en/actions)
