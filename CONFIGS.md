# Configurações e Uso Local

Este documento contém detalhes sobre a estrutura do repositório, como rodar o Quartz localmente, fluxo de publicação e organização do conteúdo.

---

## Estrutura do Repositório

Documentacao/
    content/                # Conteúdo da wiki (Markdown e imagens)
    public/                 # Site gerado pelo Quartz (não versionado)
    quartz.config.ts        # Configuração do Quartz
    package.json            # Dependências do projeto
    .github/workflows/      # GitHub Actions para deploy automático
    README.md               # Visão geral resumida
    configs.md              # Este arquivo
    CONTRIBUTING.md         # Guia de colaboração

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

- GitHub Actions gera e publica o site automaticamente na branch `gh-pages`.  
- Toda alteração na branch `main` dispara o workflow, rebuildando o site.  

---

## Estrutura do conteúdo

- Todos os arquivos de documentação e imagens ficam na pasta `content/`.  
- Links entre páginas usam **Obsidian-style `[[Nome-da-Página]]`**.  
- Quartz processa esses links automaticamente no site gerado.

---

## Ignorar arquivos

- A pasta `public/` é gerada pelo Quartz e **não deve ser versionada**.  
- O repositório ignora arquivos do Obsidian (`.obsidian`) e arquivos privados.
