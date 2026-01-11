# Portfolio Website ✨

[EN](#en) | [PT-BR](#pt-br)

---

## EN

### Overview
This repository contains a static portfolio website (HTML + Tailwind CDN + JavaScript) featuring:
- Modern dark theme layout
- Custom glowing cursor
- Sections: Home, About, Skills, Projects, Design and Contact
- Language switcher (PT, EN, ES, FR, IT)
- Simple visit tracking and form submission to Google Sheets via Google Apps Script

### Tech stack
- HTML5
- Tailwind CSS (CDN)
- JavaScript (Vanilla)
- Google Apps Script (Web App) + Google Sheets

### Run locally
1. Clone the repository.
2. Open `index.html` in your browser.

Tip: Using a local server (like VS Code Live Server) gives a more realistic environment.

### Deploy with GitHub Pages
1. Go to **Settings** > **Pages**.
2. Under **Build and deployment**, choose:
   - Source: `Deploy from a branch`
   - Branch: `main` (or `master`) and folder `/root`
3. Save. GitHub will provide the site URL.

### Languages
The language button is in the top navigation. It updates:
- Text nodes using `data-i18n`
- Placeholders using `data-i18n-placeholder`

Translations live in the `translations` object inside `index.html`.

### Contact form
The contact form is located in `#contato`. To send form data to Google Sheets, inputs should include `name`, for example:
- `name="name"`
- `name="email"`
- `name="message"`

Submission is handled by JavaScript and sent to a Google Apps Script Web App.

---

## Tracking and analytics

This project includes two tracking layers:

### 1) LocalStorage Analytics (visible in the console)
The site stores basic analytics data in the visitor browser `localStorage`, for example:
- timestamp
- page
- referrer
- language
- screen size
- user agent
- timezone

It also exposes a console helper:

- `getVisitorStats()`

This is intentional in this project. Anyone can open the browser console and inspect what is stored locally in their own browser.

Important note:
- This does not show other users data.
- It only shows what exists in that browser/device localStorage.

### 2) Google Sheets Tracking (Apps Script)
In addition to local storage, the site can send data to Google Sheets via a Google Apps Script Web App, writing into tabs such as:
- `visits` (page visits)
- `leads` (contact form submissions)
---
### License

All rights reserved

---

## PT-BR

### Visão geral
Este repositório contém um site de portfólio estático (HTML + Tailwind CDN + JavaScript) com:
- Layout moderno em tema escuro
- Cursor personalizado com efeito glow
- Seções: Home, Sobre, Habilidades, Projetos, Design e Contato
- Seletor de idioma (PT, EN, ES, FR, IT)
- Rastreamento simples de visitas e envio de formulário para Google Sheets via Google Apps Script

### Tecnologias
- HTML5
- Tailwind CSS (CDN)
- JavaScript (Vanilla)
- Google Apps Script (Web App) + Google Sheets

### Como rodar localmente
1. Clone o repositório.
2. Abra o arquivo `index.html` no navegador.

Dica: para simular melhor um ambiente de site, você pode usar um servidor local (ex.: extensão Live Server do VS Code).

### Publicar no GitHub Pages
1. Vá em **Settings** > **Pages**.
2. Em **Build and deployment**, selecione:
   - Source: `Deploy from a branch`
   - Branch: `main` (ou `master`) e a pasta `/root`
3. Salve. O GitHub vai gerar a URL do site.

### Idiomas
O botão de idioma fica no topo do site. Ele troca:
- Textos com `data-i18n`
- Placeholders com `data-i18n-placeholder`

As traduções ficam no objeto `translations` dentro do `index.html`.

### Formulário de contato
O formulário está em `#contato`. Para enviar os dados para o Google Sheets, os campos precisam ter `name`, por exemplo:
- `name="name"`
- `name="email"`
- `name="message"`

O envio é feito via JavaScript para um Web App do Google Apps Script.

---

## Rastreamento e analytics

Este projeto tem dois tipos de rastreamento:

### 1) LocalStorage Analytics (visível no console)
O site registra algumas informações no `localStorage` do navegador do visitante (no próprio dispositivo), por exemplo:
- timestamp
- página
- referrer
- idioma
- tamanho de tela
- user agent
- timezone

E expõe uma função no console:

- `getVisitorStats()`

Isso é intencional neste projeto. Qualquer pessoa pode abrir o console do navegador e ver os dados coletados no próprio navegador dela.

Observação importante:
- Isso não mostra os dados de outras pessoas do site.
- Isso mostra apenas o que está no `localStorage` daquele navegador/dispositivo.

### 2) Google Sheets Tracking (Apps Script)
Além do `localStorage`, o site pode enviar dados para uma planilha no Google Sheets via Google Apps Script Web App, gravando em abas como:
- `visits` (visitas)
- `leads` (envios do formulário)
  
---
### Licença

Todos os direitos reservados
