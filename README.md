# Avaliação Prática N1 — Central de Serviços de Rede
 
**Estudante:** LUCAS DIAS
**Disciplina:** Desenvolvimento Web I  
**Curso:** Tecnologia em Redes de Computadores  
**Instituição:** IFC - INSTITUTO FEDERAL CATARINENSE  
**Data:** 2 de outubro de 2026  
**Modalidade:** Individual  
**Repositório:** https://github.com/LucasDias0259/dw1-n1-central-servicos-rede  
**GitHub Pages:** https://lucasdias0259.github.io/dw1-n1-central-servicos-rede/
 
## Contexto
 
Este projeto é uma interface Web para apresentar os serviços de infraestrutura de uma empresa, consultar solicitações técnicas e permitir a abertura de novos chamados.
 
A aplicação se chama **Central de Serviços de Rede** e foi desenvolvida com os conhecimentos de HTML e CSS do primeiro ciclo da disciplina.
 
A aplicação é composta por três páginas:
 
1. Página principal;
2. Pesquisa e listagem de chamados;
3. Abertura de chamado.
Não foram utilizados JavaScript, banco de dados ou servidor.
 
Os formulários têm finalidade estrutural e didática. A pesquisa e o envio dos chamados não funcionam de maneira dinâmica.
 
---
 
# Objetivos do projeto
 
Neste projeto foram aplicados:
 
- Documentos HTML bem estruturados;
- Elementos semânticos;
- Navegação entre diferentes páginas;
- Conteúdo organizado em seções e artigos;
- Cartões com Flexbox;
- Formulários HTML;
- Associação entre `label`, `for`, `id` e `name`;
- Validações nativas;
- Folhas de estilo organizadas por responsabilidade;
- Classes e seletores CSS;
- Box Model;
- Layout fluido;
- Responsividade com media queries;
- Versionamento com Git;
- Documentação com `README.md`;
- Publicação no GitHub Pages.
---
 
# Tecnologias utilizadas
 
- HTML5 semântico;
- CSS3 (Flexbox, variáveis CSS e media queries);
- Git e GitHub;
- GitHub Pages.
---
 
# Nome do repositório
 
```text
dw1-n1-central-servicos-rede
```
 
---
 
# Estrutura do projeto
 
```text
dw1-n1-central-servicos-rede/
├── index.html
├── chamados.html
├── abrir-chamado.html
├── README.md
├── docs/
│   ├── 01-index.png
│   ├── 02-chamados.png
│   └── 03-abrir-chamado.png
└── assets/
    ├── css/
    │   ├── reset.css
    │   ├── global.css
    │   ├── index.css
    │   ├── chamados.css
    │   └── abrir-chamado.css
    └── img/
        ├── redes.svg
        ├── suporte.svg
        ├── seguranca.svg
        └── monitoramento.svg
```
 
A pasta `docs` guarda as capturas de tela usadas neste README. As imagens dos cartões são SVGs criados para o projeto.
 
---
 
# Navegação entre as páginas
 
As três páginas possuem o mesmo cabeçalho, com:
 
- Nome da aplicação;
- Pequena descrição;
- Menu de navegação (**Início | Chamados | Abrir chamado**);
- Link para a página inicial;
- Link para a listagem de chamados;
- Link para a abertura de chamado.
A página atual é destacada no menu com `aria-current="page"` e uma cor diferente, definida no CSS com o seletor `a[aria-current="page"]`.
 
---
 

 
# 1. Página principal — `index.html`
 
## Cabeçalho
 
O cabeçalho apresenta:
 
- Nome: **Central de Serviços de Rede**;
- Slogan: *Conectividade, segurança e suporte técnico*;
- Menu com as três páginas.
## Seção de apresentação
 
Contém:
 
- Identificação da seção;
- Título principal: *Soluções para manter sua rede conectada*;
- Texto de apresentação;
- Botão **Solicitar suporte**, com link para `abrir-chamado.html`.
## Serviços disponíveis
 
Quatro cartões organizados com Flexbox:
 
| Serviço | Categoria |
| ------- | --------- |
| Configuração de redes | Rede |
| Suporte técnico | Atendimento |
| Segurança | Proteção |
| Monitoramento | Acompanhamento |
 
Cada cartão apresenta imagem (com texto alternativo), categoria, nome do serviço, pequena descrição e o link **Solicitar atendimento**, que leva para `abrir-chamado.html`.
 
---
 

 
# 2. Pesquisa e listagem — `chamados.html`
 
A página apresenta:
 
1. Resumo dos chamados;
2. Formulário de pesquisa;
3. Listagem das solicitações.
## Resumo dos chamados
 
Três indicadores organizados com Flexbox, coerentes com a listagem:
 
- Abertos: **3**;
- Pendentes: **2**;
- Concluídos: **1**.
## Formulário de pesquisa
 
Filtros disponíveis:
 
- Palavra-chave (`search`);
- Categoria (`select`);
- Prioridade (`select`);
- Status (`select`);
- Data inicial (`date`);
- Data final (`date`);
- Horário (`time`);
- Botão **Pesquisar** (`submit`);
- Botão **Limpar filtros** (`reset`).
Categorias: Rede, Segurança, Hardware e Sistema.  
Prioridades: Baixa, Média e Alta.  
Status: Aberto, Pendente e Concluído.
 
> O formulário não filtra os resultados de verdade. Nesta etapa são considerados a estrutura, os campos, os rótulos, a organização visual e a responsividade.
 
## Listagem dos chamados
 
Seis chamados fictícios, cada um com número, título, categoria, prioridade, solicitante, data (em `<time>`), hora e status:
 
| Número | Título                                | Categoria | Prioridade | Status    |
| ------ | ------------------------------------- | --------- | ---------- | --------- |
| #001   | Laboratório sem acesso à internet     | Rede      | Alta       | Aberto    |
| #002   | Atualização do antivírus              | Segurança | Média      | Pendente  |
| #003   | Impressora da secretaria não imprime  | Hardware  | Média      | Aberto    |
| #004   | Troca de senha do Wi-Fi institucional | Rede      | Baixa      | Concluído |
| #005   | Sistema acadêmico fora do ar          | Sistema   | Alta       | Aberto    |
| #006   | Instalação de ponto de rede na sala 12 | Rede     | Baixa      | Pendente  |
 
## Status dos chamados
 
Cada status possui uma classe específica, uma cor e um texto com símbolo:
 
```html
<span class="status status-aberto">● Aberto</span>
 
<span class="status status-pendente">◓ Pendente</span>
 
<span class="status status-concluido">✓ Concluído</span>
```
 
A situação do chamado nunca é comunicada apenas pela cor: há também o texto, o símbolo e a barra lateral colorida do cartão.
 
---
 

 
# 3. Abertura de chamado — `abrir-chamado.html`
 
Formulário dividido em dois grupos (`fieldset` e `legend`), separados por um divisor.
 
## 1. Dados do solicitante
 
- Nome completo (`text`, obrigatório, mínimo de 5 e máximo de 100 caracteres);
- E-mail (`email`, obrigatório);
- Telefone (`tel`, com `pattern` para o formato brasileiro);
- Data e hora da ocorrência (`datetime-local`, obrigatório).
## 2. Informações do chamado
 
- Categoria (`select`, obrigatório);
- Prioridade (`radio`, obrigatório);
- Anexo (`file`, aceita `.png`, `.jpg`, `.jpeg` e `.pdf`);
- Descrição do problema (`textarea`, obrigatório, de 20 a 500 caracteres);
- Equipamentos ou serviços afetados (`checkbox`: Computador, Impressora, Rede e Sistema);
- Confirmação das informações (`checkbox`, obrigatório).
## Botões
 
1. **Limpar** (`reset`);
2. **Enviar** (`submit`).
## Método de envio
 
O formulário usa:
 
```html
<form class="formulario" action="abrir-chamado.html" method="get">
```
 
O GitHub Pages hospeda apenas arquivos estáticos e não aceita o método `POST` (erro 405). Por isso o método é `get`, e o envio apenas recarrega a página com os dados na barra de endereço.
 
---
 
# Requisitos dos formulários
 
Todos os campos possuem:
 
- Rótulo visível;
- `id`;
- `name`;
- Tipo adequado;
- Associação entre `for` e `id`;
- Validação quando necessária.
Atributos utilizados: `required`, `minlength`, `maxlength`, `pattern`, `accept`, `placeholder` e `autocomplete`.
 
O `placeholder` não substitui o `<label>`.
 
---
 
# HTML semântico
 
Elementos utilizados:
 
- `<header>`;
- `<nav>`;
- `<main>`;
- `<section>`;
- `<article>` (cartões de serviços e chamados);
- `<form>`;
- `<fieldset>`;
- `<legend>`;
- `<time>`;
- `<footer>`.
O `<div>` foi usado apenas para agrupamentos sem elemento semântico mais adequado. `<figure>` e `<figcaption>` não foram utilizados.
 
---
 
# Organização do CSS
 
## `reset.css`
 
Normaliza os estilos padrões do navegador e aplica `box-sizing: border-box` a todos os elementos.
 
## `global.css`
 
Estilos compartilhados:
 
- Variáveis de cor (`:root`);
- `body` e tipografia;
- Contêiner fluido;
- Cabeçalho e navegação;
- Links e botões;
- Campos de formulário;
- Rodapé.
## `index.css`
 
- Seção de apresentação;
- Cartões de serviços;
- Imagens;
- Categorias.
## `chamados.css`
 
- Indicadores;
- Formulário de pesquisa;
- Listagem e cartões de chamados;
- Badges de status.
## `abrir-chamado.css`
 
- Formulário de abertura;
- Grupos de campos (`fieldset`);
- Radios e checkboxes;
- Área de botões.
Ordem de carregamento em cada página:
 
```html
<link rel="stylesheet" href="assets/css/reset.css">
<link rel="stylesheet" href="assets/css/global.css">
<link rel="stylesheet" href="assets/css/index.css">
```
 
(em `chamados.html` e `abrir-chamado.html`, o terceiro arquivo é o CSS da própria página).
 
---
 
# Flexbox
 
O Flexbox foi usado em:
 
- Menu de navegação;
- Cartões de serviços;
- Indicadores;
- Campos do formulário de pesquisa;
- Informações dos chamados;
- Campos da abertura de chamado;
- Área de botões.
Principais propriedades: `display: flex`, `flex-wrap`, `gap`, `justify-content`, `align-items` e `flex: 1 1 <tamanho>`, que faz os itens crescerem, encolherem e quebrarem de linha conforme o espaço disponível.
 
---
 
# Layout fluido e responsividade
 
Recursos aplicados:
 
- Viewport configurada;
- Medidas relativas (`rem` e `%`);
- Contêiner fluido (`width: 92%` com `max-width: 75rem` e `margin-inline: auto`);
- Flexbox com `flex-wrap` e `gap`;
- Imagens adaptáveis (`max-width: 100%` e `height: auto`);
- Media queries;
- `box-sizing: border-box`.
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
 
Media queries utilizadas:
 
```css
@media (max-width: 64rem) { /* cartões: 4 → 2 por linha */ }
@media (max-width: 48rem) { /* menu, filtros, campos e botões em coluna */ }
@media (max-width: 40rem) { /* cartões: 1 por linha */ }
```
 
Em telas menores:
 
- O menu passa para uma coluna;
- Os cartões mudam de linha;
- Os indicadores mudam de linha;
- Os filtros ficam em uma coluna;
- Os campos da abertura de chamado ficam em uma coluna;
- Os botões ocupam a largura disponível;
- Não há rolagem horizontal.
Teste realizado: as três páginas foram abertas em 320, 375, 768 e 1280 px, e nenhuma apresentou rolagem horizontal.
 
---
 
# Acessibilidade e usabilidade
 
- `lang="pt-BR"`;
- Hierarquia de títulos (`h1`, `h2`, `h3`);
- Textos alternativos nas imagens;
- Rótulos visíveis;
- Associação entre `label` e campo;
- Contraste entre texto e fundo;
- Estado de foco visível em links, botões e campos (`outline`);
- Links com textos compreensíveis;
- Indicação textual dos status;
- Campos obrigatórios marcados com `*`;
- Navegação possível pela tecla `Tab`.
---
 
# Personalização
 
Os wireframes foram seguidos na organização das páginas. Foram personalizados:
 
- **Cores:** paleta verde-azulada, definida nas variáveis `:root` de `global.css`;
- **Fonte:** Trebuchet MS;
- **Imagens:** quatro ilustrações em SVG (Wi-Fi, computador, escudo e gráfico).
---
 
# Git e GitHub
 
O projeto foi enviado para um repositório público e publicado com o GitHub Pages (**Settings → Pages → Deploy from a branch → `main` / `(root)`**).
 
Comandos principais:
 
```text
git init
git add .
git commit -m "Cria estrutura inicial do projeto"
git branch -M main
git remote add origin https://github.com/LucasDias0259/dw1-n1-central-servicos-rede.git
git push -u origin main
```
 
---
 
# Como executar
 
Abra o arquivo `index.html` no navegador, ou acesse o link do GitHub Pages. Não é necessário instalar nada.
 
---
 
# Uso de Inteligência Artificial
 
Utilizei uma ferramenta de IA como apoio na geração da estrutura inicial do projeto. Depois revisei o código, testei as três páginas em telas amplas e estreitas e adaptei cores, fonte e imagens. Consigo explicar o funcionamento do HTML e do CSS entregues.
 
---
 
# Dificuldades encontradas
 
- **Erro 405 no GitHub Pages:** o formulário com `method="post"` retornava *405 Not Allowed*, porque sites estáticos não aceitam POST. Resolvi trocando para `method="get"`.
- **Push recusado:** o `git push` foi rejeitado porque o repositório remoto tinha commits que eu não tinha localmente. Resolvi com `git pull --rebase origin main` e um novo `git push`.
- **Espaços vazios no celular:** quando os campos mudavam para coluna, o `flex-basis` virava altura e criava espaços grandes. Corrigi com `flex: 0 0 auto` nos itens em coluna.
---
 
# Possíveis melhorias
 
- Usar JavaScript para filtrar a listagem de verdade;
- Validar o formulário com mensagens personalizadas;
- Enviar os chamados para um servidor ou banco de dados;
- Incluir as categorias Software e Acesso e as opções Wi-Fi e Outro em equipamentos;
- Usar `<figure>` e `<figcaption>` nas imagens dos cartões;
- Criar um tema escuro.
---
 
# Checklist antes da entrega
 
## Estrutura geral
 
- [x] `index.html` criado;
- [x] `chamados.html` criado;
- [x] `abrir-chamado.html` criado;
- [x] Navegação funcionando;
- [x] Página atual destacada no menu;
- [x] Arquivos CSS organizados;
- [x] Imagens armazenadas em `assets/img`.
## Página principal
 
- [x] Seção de apresentação;
- [x] Botão para solicitar suporte;
- [x] Pelo menos quatro serviços;
- [x] Cartões com imagem;
- [x] Categoria;
- [x] Descrição;
- [x] Link para abrir chamado;
- [x] Organização com Flexbox.
## Página de chamados
 
- [x] Indicador de chamados abertos;
- [x] Indicador de chamados pendentes;
- [x] Indicador de chamados concluídos;
- [x] Busca por palavra-chave;
- [x] Filtro por categoria;
- [x] Filtro por prioridade;
- [x] Filtro por status;
- [x] Data inicial;
- [x] Data final;
- [x] Horário;
- [x] Pelo menos seis chamados;
- [x] Badges de status;
- [x] Datas utilizando `<time>`.
## Abertura de chamado
 
- [x] Nome completo;
- [x] E-mail;
- [x] Telefone;
- [x] Data e hora;
- [x] Categoria;
- [x] Prioridade;
- [x] Descrição;
- [x] Equipamentos afetados;
- [x] Seleção de arquivo;
- [x] Confirmação;
- [x] Botão para limpar;
- [x] Botão para enviar;
- [x] Labels associados aos campos;
- [x] Validações nativas.
## Responsividade
 
- [x] Viewport configurada;
- [x] `box-sizing` aplicado;
- [x] Contêiner fluido;
- [x] Flexbox com quebra de linha;
- [x] Imagens adaptáveis;
- [x] Media query;
- [x] Menu adaptável;
- [x] Campos em uma coluna no celular;
- [x] Ausência de rolagem horizontal.
## Entrega
 
- [ ] Nome do estudante no README;
- [x] Commits realizados;
- [x] Código enviado ao GitHub;
- [x] Repositório público;
- [x] GitHub Pages configurado;
- [x] Link público testado.
