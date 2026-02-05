# Documentação Quartz Wiki

Este repositório contém uma wiki/documentação criada com **Quartz 4** e **Obsidian**, permitindo que você organize suas notas em Markdown e publique um site estático automaticamente usando **GitHub Pages** e **GitHub Actions**.

---

## Estrutura do Repositório

Documentacao/
├─ content/                # Conteúdo da wiki (Markdown e imagens)
├─ public/                 # Site gerado pelo Quartz (não versionado)
├─ quartz.config.ts        # Configuração do Quartz
├─ package.json            # Dependências do projeto
├─ .github/workflows/      # GitHub Actions para deploy automático
└─ README.md               # Este arquivo

---

## Como usar localmente

1. Clone o repositório:

```bash
git clone git@github.com:GuilhermeMillares/documentacao.git
cd documentacao
