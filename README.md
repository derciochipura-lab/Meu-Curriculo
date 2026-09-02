
 Meu Currículo — Site Pessoal

**Estudante:** Dércio Filipe Luís Chipura
**Turma:** Programação de Design Web,na universidade licungo
licenciatura em Informática 
  

## Descrição do projeto

Site pessoal de currículo (portfólio), feito apenas com **HTML5 semântico** e **CSS3 puro** — sem frameworks (Bootstrap, Tailwind, etc.) e sem JavaScript. Todo o comportamento visual (menu ativo, cartões, formulário, responsividade) é conseguido só com HTML e CSS.

### Como visualizar

Basta abrir o ficheiro `index.html` num navegador (não precisa de servidor nem de instalação).

## Páginas do site

| Página | Conteúdo |
|---|---|
| `index.html` | Apresentação pessoal, foto, tagline, vídeo e áudio de apresentação, botão de destaque para a página de Contacto |
| `about.html` | Formação académica (lista), experiência, competências técnicas, tabela de línguas |
| `portfolio.html` | Grelha de projetos em CSS Grid, cada um num cartão com imagem, título e descrição |
| `hobbies.html` | Hobbies em cartões organizados com Flexbox |
| `contact.html` | Formulário de contacto completo com validação nativa HTML5 |

## Principais tags e atributos usados

- **`<header>` / `<nav>` / `<main>` / `<section>` / `<article>` / `<footer>`** — landmarks semânticos que substituem "divs genéricas", dando estrutura e significado a cada parte da página.
- **`<figure>` / `<figcaption>`** — usados nas imagens dos projetos (portfolio.html), associando cada imagem à sua legenda.
- **`<video controls poster>` + `<source type="video/mp4">`** (index.html) — vídeo nativo, com imagem de pré-visualização (`poster`) antes do play e controlos do próprio navegador.
- **`<audio controls>` + `<source type="audio/mpeg">`** (index.html) — faixa de áudio nativa, sem plugins.
- **`alt` descritivo em todas as `<img>`** — descreve o conteúdo real da imagem, nunca "imagem" ou vazio.
- **`<table>` com `<thead>`/`<tbody>`** — usada na tabela de domínio de línguas (about.html).
- **`<fieldset>` / `<legend>`** (contact.html) — agrupam campos relacionados do formulário (dados pessoais, detalhes do pedido, preferências, mensagem).
- **`<label for="">`** — associa cada campo ao seu rótulo, essencial para acessibilidade.
- **Tipos de `<input>`**: `text`, `email`, `tel` (com `pattern`), `date`, `number` (com `min`/`max`), `file` (com `accept`), `radio`, `checkbox`; mais `<select>` e `<textarea>` — cada um valida o formato certo diretamente no navegador, sem JavaScript.
- **`required`, `minlength`, `maxlength`, `pattern`, `min`, `max`** — atributos nativos de validação HTML5.

## Principais recursos CSS usados

- **Variáveis CSS (`:root { --cor-... }`)** — centralizam a paleta de cores e os espaçamentos.
- **Flexbox** — usado no menu de navegação e, de forma central, na página `hobbies.html` (`flex-direction`, `flex-wrap`, `justify-content`, `align-items`).
- **CSS Grid** — usado em `portfolio.html` (`grid-template-columns: repeat(auto-fit, minmax(...))`) para a grelha de projetos.
- **`position: sticky`** — o cabeçalho mantém-se visível ao rolar a página. A diferença entre `static`, `relative`, `absolute`, `fixed` e `sticky` está explicada em comentário no início de `css/estilo.css`.
- **Seletores avançados** — descendente (`.navegacao a`), filho direto (`.navegacao > ul`), atributo (`input[type="email"]`).
- **Pseudo-classes** — `:hover`, `:focus`, `:first-child`/`:last-child`, `:nth-child(even)`, `:invalid`.
- **Pseudo-elementos** — `::after` para o traço no link ativo do menu e para o ícone de "check" dos checkboxes personalizados.
- **`transition` e `@keyframes`** — transição nos cartões do portfólio ao passar o rato, e uma animação discreta (`@keyframes pulsar`) no botão de destaque da Home.
- **Gradientes e sombras** — `linear-gradient` no cabeçalho e no botão de destaque; `box-shadow` nos cartões.
- **Responsividade mobile-first** — `css/responsivo.css` parte das regras pensadas para ecrã pequeno e usa `@media (min-width: 30em)` e `@media (min-width: 48em)` para ampliar progressivamente o layout.
- **Unidades relativas e fixas combinadas** — `rem`, `%`/`fr`, `em` nas media queries, `px` só onde faz sentido um valor fixo.

## Estrutura de pastas

```
meu-curriculo/
├── index.html
├── about.html
├── portfolio.html
├── hobbies.html
├── contact.html
├── css/
│   ├── estilo.css
│   └── responsivo.css
├── assets/
│   ├── img/
│   ├── video/
│   ├── audio/
│   └── ficheiros/
└── README.md
```
