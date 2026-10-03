# Central de Serviços de Rede

Projeto avaliativo da disciplina **Desenvolvimento Web I** (N1).
Site de uma central de chamados técnicos, com três páginas, feito apenas com HTML e CSS.

- **Autor:** Lucas Dias
- **Instituição:** IFC - INSTITUTO FEDERAL CATARINENSE
- **Repositório:** `dw1-n1-central-servicos-rede`
- **GitHub Pages:** https://LucasDias0259.github.io/dw1-n1-central-servicos-rede/

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



