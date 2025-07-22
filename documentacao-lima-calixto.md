# 📘 Documentação Técnica — Lima Calixto Personalizados

Projeto de catálogo digital com vitrine responsiva, galeria interativa, zoom em imagens, depoimentos com foto e botões de contato via WhatsApp. Este guia documenta cada seção do código para facilitar manutenção futura.

---

## 🗂️ Sumário

1. [Informações do `<head>` e Metadados](#1-informações-do-head-e-metadados)
2. [Estilos CSS Globais](#2-estilos-css-globais)
3. [Cabeçalho do Site (`<header>`)](#3-cabeçalho-do-site-header)
4. [Seção Sobre a Empresa](#4-seção-sobre-a-empresa)
5. [Galeria com Carrossel e Zoom](#5-galeria-com-carrossel-e-zoom)
6. [Vitrine de Produtos (Cards)](#6-vitrine-de-produtos-cards)
7. [Depoimentos com Imagem](#7-depoimentos-com-imagem)
8. [Rodapé com Links Sociais](#8-rodapé-com-links-sociais)
9. [Script do Carrossel](#9-script-do-carrossel)
10. [Considerações Finais](#10-considerações-finais)

---

## 1. 📌 Informações do `<head>` e Metadados

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Catálogo Lima Calixto Personalizados - presentes únicos e afetivos." />
  <title>Lima Calixto Personalizados</title>
  <link rel="preload" href="fundo-decorativo.png" as="image" />
</head>
```

- Define codificação, responsividade e descrição para SEO.
- Pré-carrega imagem de fundo decorativa para melhor performance.

---

## 2. 🎨 Estilos CSS Globais

- Definem aparência geral da página, seções, componentes, botões e comportamento em dispositivos móveis.
- Incluem `body`, `.topo`, `.sobre`, `.produto`, `.catalogo`, `.whatsapp-btn`, `.galeria`, `.depoimentos`, `.card-zoom`, `.foto-zoom`, `.rodape` e media queries.

---

## 3. 🖼️ Cabeçalho do Site `<header>`

```html
<header class="topo">
  <img src="logo-lima-calixto.png" alt="Logo Lima Calixto" />
  <h1>Lima Calixto Personalizados</h1>
  <p class="slogan">Personalize com emoção. Fale com a gente!</p>
</header>
```

---

## 4. 💬 Seção Sobre a Empresa

```html
<section class="sobre">
  <h2>Sobre a Lima Calixto</h2>
  <p>Transformamos lembranças em presentes afetivos com carinho, criatividade e atenção aos detalhes.</p>
</section>
```

---

## 5. 🖼️ Galeria com Carrossel e Zoom

```html
<section class="galeria">
  <h2>Galeria de Fotos</h2>
  <div class="carrossel">
    <button class="seta esquerda">←</button>
    <div class="faixa">
      <div class="foto-zoom">
        <img src="galeria1.jpg" />
        <figcaption>Estilo que emociona 💕</figcaption>
      </div>
      <!-- outras imagens -->
    </div>
    <button class="seta direita">→</button>
  </div>
</section>
```

---

## 6. 🛍️ Vitrine de Produtos (Cards)

Cada card possui:

- Imagem com zoom (`.card-zoom`)
- Nome do produto `<h2>`
- Preço destacado `<p class="preco">`
- Descrição afetiva
- Botão de WhatsApp com link pré-formatado

Exemplo:

```html
<div class="produto">
  <div class="card-zoom">
    <img src="camiseta-crista.jpg" alt="Camiseta cinza com estampa MEU ALVO É CRISTO" />
  </div>
  <h2>Camiseta Cinza - Meu Alvo é Cristo</h2>
  <p class="preco">R$ 45,00</p>
  <p>Estampa que une fé e estilo...</p>
  <a class="whatsapp-btn" href="https://wa.me/SEUNUMERO">Fale no WhatsApp</a>
</div>
```

---

## 7. 💬 Depoimentos com Imagem

```html
<section class="depoimentos">
  <h2>Depoimentos de Clientes</h2>
  <div class="depoimento">
    <img src="cliente1.jpg" alt="Foto da Juliana" />
    <div class="texto">
      <p>“Fiquei emocionada com o cuidado em cada detalhe. Super recomendo!”</p>
      <cite>– Juliana, RJ</cite>
    </div>
  </div>
</section>
```

---

## 8. 📫 Rodapé com Links Sociais

```html
<footer class="rodape">
  <p>© Lima Calixto Personalizados - Todos os direitos reservados</p>
  <p>
    <a href="mailto:limacalixtopersonalizados@gmail.com">📧 E-mail</a> |
