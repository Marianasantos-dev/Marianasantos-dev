# Portfólio automático

Este repositório também hospeda o portfólio de Mariana Santos.

## Como a sincronização funciona

O `index.html` consulta automaticamente os repositórios públicos de **Marianasantos-dev** pela API pública do GitHub.

- Novo repositório público: aparece automaticamente no portfólio.
- Alteração de nome, descrição, linguagem ou data de atualização: refletida automaticamente.
- Repositórios arquivados, forks e o próprio repositório de perfil são ignorados.
- Se existir `portfolio.json` na raiz do projeto, ele controla a apresentação profissional do case.
- Sem `portfolio.json`, o site cria um card automaticamente usando os metadados do GitHub.

## Modelo de portfolio.json

```json
{
  "title": "Nome do projeto",
  "category": "Projeto acadêmico",
  "summary": "Resumo profissional do projeto.",
  "problem": "Problema ou contexto que motivou o projeto.",
  "solution": "Solução desenvolvida.",
  "technologies": ["Python", "HTML", "JavaScript"],
  "featured": false,
  "status": "Concluído"
}
```

## Publicação

O workflow `.github/workflows/pages.yml` está preparado para GitHub Pages.

Após o GitHub Pages estar configurado para usar **GitHub Actions** como fonte, alterações neste repositório são publicadas automaticamente.

Os demais projetos não exigem novo deploy do portfólio para aparecerem: o site consulta o GitHub quando é aberto.
