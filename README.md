# MissionCare Plus: Aplicação Interativa

![Status](https://img.shields.io/badge/status-ativo-success)
![Versão](https://img.shields.io/badge/version-1.0.0-blue)
![Licença](https://img.shields.io/badge/license-MIT-green)

Uma página web interativa e multilíngue desenvolvida para apresentar a iniciativa **MissionCare Plus**, oferecendo uma visão completa sobre seu propósito, funcionalidades e como se envolver.

---

## Tabela de Conteúdos

1.  [Visão Geral](#visão-geral)
2.  [Links Relevantes](#links-relevantes)
3.  [Funcionalidades Principais](#funcionalidades-principais-da-página)
4.  [Tecnologias Utilizadas](#tecnologias-utilizadas)
5.  [Estrutura do Código](#estrutura-do-código)
6.  [Como Executar](#como-executar)
7.  [Contribuição](#contribuição)
8.  [Licença](#licença)

---

## Visão Geral

Este projeto consiste em uma página web interativa de página única (SPA - Single Page Application) desenvolvida para apresentar a iniciativa **MissionCare Plus**. O objetivo é traduzir a mensagem e o propósito do aplicativo MissionCare Plus em uma experiência digital envolvente, informativa e fácil de navegar para um público global, incluindo missionários, agências, doadores e profissionais de saúde.

A página foi construída com um fluxo narrativo que guia o usuário desde a compreensão dos desafios enfrentados pelos missionários até a solução oferecida pelo aplicativo e, finalmente, um chamado à ação para que se envolvam na missão.

## Links Relevantes

-   **Acessar o App MissionCare Plus:** <https://telesaudemissionaria.github.io/missioncare-plus/index.html>
-   **Playlist no YouTube:** [Telessaúde Missionária](https://youtube.com/playlist?list=PL6JIF2YBc-Bwo865kfBzRLCjd9lqhmOI1&si=HvYXdOM0L7tFgYe1)

## Funcionalidades Principais da Página

-   🎨 **Design Responsivo:** Totalmente adaptável para desktops, tablets e dispositivos móveis.
-   🗺️ **Narrativa Guiada:** A estrutura da página leva o usuário por uma jornada: O Desafio -> A Solução -> Envolva-se.
-   🖱️ **Componentes Interativos:**
    -   **Explorador de Funcionalidades:** Uma seção interativa onde o usuário pode clicar em diferentes funcionalidades do app para ver uma descrição detalhada.
    -   **Abas de Envolvimento:** Conteúdo organizado em abas para diferentes públicos-alvo (Missionários, Líderes, Profissionais da Saúde, Apoiadores).
-   📊 **Visualização de Dados:** Um gráfico de rosca (doughnut chart) criado com Chart.js para ilustrar os "Pilares do Cuidado Integral".
-   🌐 **Suporte Multilíngue:** Funcionalidade completa de tradução para **Português, Inglês, Espanhol e Francês**, ativada por um seletor de idiomas visual e intuitivo.

## Tecnologias Utilizadas

| Categoria      | Tecnologia                               |
| -------------- | ---------------------------------------- |
| **Estrutura** | HTML5                                    |
| **Estilização**| Tailwind CSS (via CDN)                   |
| **Lógica** | JavaScript (Vanilla)                     |
| **Gráficos** | Chart.js (via CDN)                       |
| **Fontes** | Google Fonts (Inter)                     |

## Estrutura do Código

O projeto está contido em um **único arquivo HTML**, o que simplifica a distribuição e o deploy.

1.  **`<head>`**: Contém metadados, links para as CDNs (Tailwind, Chart.js, Google Fonts) e estilos CSS customizados.
2.  **`<body>`**: Inclui o `<header>`, `<main>` com as seções da página (`#hero`, `#desafio`, `#solucao`, `#envolva-se`), e o `<footer>`.
3.  **`<script>`**: No final do `<body>`, um bloco de JavaScript gerencia todas as interações dinâmicas da página.

### Lógica JavaScript

O script principal gerencia todas as interações:

-   **Sistema de Tradução:** Um objeto `translations` armazena os textos em 4 idiomas. A função `setLanguage(lang)` atualiza dinamicamente o conteúdo da página com base na seleção do usuário, incluindo o texto do gráfico.
-   **Componentes Interativos:** Listeners de evento gerenciam a lógica para o menu móvel, o explorador de funcionalidades e as abas de envolvimento, controlando a visibilidade e o estado ativo dos elementos.
-   **Gráfico Dinâmico:** A função `createChart(lang)` destrói e recria o gráfico do Chart.js sempre que o idioma é alterado, garantindo que as legendas sejam traduzidas corretamente.

## Como Executar

Não é necessário nenhum processo de build ou servidor local. Basta abrir o arquivo `index.html` em qualquer navegador web moderno.

```bash
# Exemplo: Abrindo o arquivo no macOS
open index.html

# Exemplo: Abrindo o arquivo no Windows
start index.html
