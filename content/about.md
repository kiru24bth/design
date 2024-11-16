---
Title: About
Description: This is our about page.
---

Om sidan
==========================

Grunden för webbplatsen utgörs av textinnehåll som skrivs i Markdown-filer, som i sin tur renderas som HTML med hjälp av Pico CMS. Sidans olika templates för bland annat navigation och footer använder Twig. Markdown är enkelt för användaren och kräver inte heller några djupare kunskaper i varken HTML eller programmering överlag.  Med hjälp av SCSS skrivs sidans tidigare CSS. Olika SCSS-filer delas upp efter deras syfte och funktion och på så sätt skapas en överskådlig mappstruktur som gör att projektet blir enklare att underhålla och förstå.

Strukturen är:
* Abstracts: Globala och återanvändbara delar med variabler, mixins, funktioner etc.
* Base: Grundstilar för typografi och basstilar för övergripande element.
* Components: Enskilda UI-komponenter som tex. tabeller, formulär, knappar.
* Layout: Layout-specifika stilar för content, sidhuvud, sidfot och navigation.
* Themes: Stilar för att hantera flera design-/färgscheman, tex. dark mode eller high contrast.

För närvarande används typsnitt från Google Fonts, ”New Amsterdam” för rubriker och ”Open Sans” för brödtext och övrigt innehåll. Båda av typen sans serif för bättre läsbarhet. Webbplatsens ikoner är Font Awesome.