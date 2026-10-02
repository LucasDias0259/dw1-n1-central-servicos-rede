# Central de Serviços de Rede

Projeto avaliativo da disciplina **Desenvolvimento Web I** (N1).
Site de uma central de chamados técnicos, com três páginas, feito apenas com HTML e CSS.

- **Autor:** SEU NOME
- **Instituição:** NOME DA INSTITUIÇÃO
- **Repositório:** `dw1-n1-central-servicos-rede`
- **GitHub Pages:** https://SEU-USUARIO.github.io/dw1-n1-central-servicos-rede/

## Páginas

| Arquivo | Descrição |
|---|---|
| `index.html` | Página inicial com apresentação, botão de suporte e 4 cartões de serviços |
| `chamados.html` | Indicadores, formulário de pesquisa e listagem de 6 chamados fictícios |
| `abrir-chamado.html` | Formulário completo de abertura de chamado, com validações nativas |

## Estrutura

```
dw1-n1-central-servicos-rede/
├── index.html
├── chamados.html
├── abrir-chamado.html
├── README.md
└── assets/
    ├── css/ (reset, global, index, chamados, abrir-chamado)
    └── img/ (imagens SVG dos cartões)
```

## Tecnologias e conceitos aplicados

- HTML semântico (`header`, `nav`, `main`, `section`, `article`, `fieldset`, `footer`)
- CSS separado por responsabilidade (reset, global e um arquivo por página)
- Flexbox para menu, cartões, indicadores, listagem e formulários
- Box Model com `box-sizing: border-box`
- Medidas relativas (`rem`, `%`), contêiner fluido (`width: 92%` + `max-width`)
- Imagens adaptáveis (`max-width: 100%`) com texto alternativo
- Media queries (≈ 1024px, 768px e 640px) para telas médias e celulares
- Formulários com `label`, `id`, `name`, tipos adequados e validações nativas (`required`, `minlength`, `maxlength`, `pattern`, `accept`)
- Menu igual nas três páginas, com a página atual destacada via `aria-current="page"`
- Status dos chamados identificados por **cor e texto**

## Como executar

Basta abrir o `index.html` no navegador. Não há JavaScript, banco de dados nem servidor.

## Publicação (Git e GitHub Pages)

```bash
git init
git add .
git commit -m "Primeira versão da Central de Serviços de Rede"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/dw1-n1-central-servicos-rede.git
git push -u origin main
```

Depois: **Settings → Pages → Deploy from a branch → `main` / `(root)` → Save**.

## Dificuldades encontradas

Descreva aqui, com suas palavras, as dificuldades que teve (ou "nenhuma").
