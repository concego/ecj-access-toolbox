# 🧰 ECJ Access Toolbox

**Gerador de componentes HTML acessíveis — prontos para produção.**  
*Accessible HTML component generator — production-ready.*

[![GitHub Pages](https://img.shields.io/badge/Live-GitHub%20Pages-blue?logo=github)](https://concego.github.io/ecj-access-toolbox/)
[![WCAG 2.2](https://img.shields.io/badge/WCAG-2.2%20AA-green)](https://www.w3.org/TR/WCAG22/)
[![WAI-ARIA 1.2](https://img.shields.io/badge/WAI--ARIA-1.2-green)](https://www.w3.org/TR/wai-aria-1.2/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

---

## 🌐 Acesse / Access

**https://concego.github.io/ecj-access-toolbox/**

Ferramenta 100% client-side. Sem backend, sem login, sem instalação.  
100% client-side tool. No backend, no login, no installation.

---

## O que é / What is it

O **ECJ Access Toolbox** nasceu de uma observação real: a maioria dos erros de acessibilidade reportados por usuários reais (comunidade r/Accessibility, auditorias do mundo real) é causada por desenvolvedores que **não sabem o que estão fazendo de errado**.

O objetivo não é ensinar teoria — é **entregar código pronto**, correto e explicado, para que o desenvolvedor copie, cole e aprenda na prática.

> Trabalho com acessibilidade digital desde 2004. Sou cego e uso NVDA e TalkBack diariamente.  
> — Anderson Carvalho, [Eu Concego Jogar](https://site.zapia.com/0alwlra4)

---

## ✨ Componentes disponíveis / Available Components

### Fase 1 — Críticos / Phase 1 — Critical

| Componente | O que resolve / What it solves |
|---|---|
| **Button** | Estados completos (`aria-disabled`, `aria-busy`, `aria-pressed`, `aria-expanded`), foco visível, variantes primary/secondary/danger |
| **Input Field** | Label real (não placeholder), `aria-invalid`, `aria-describedby`, autocomplete, estado de erro acessível |
| **Form Group** | `<fieldset>` + `<legend>` corretos para checkbox/radio, `aria-required`, associação semântica real |
| **Select / Combobox** | Label real, `aria-invalid`, placeholder acessível, estado de erro, hint text |

### Fase 2 — Em breve / Phase 2 — Coming Soon

- Modal / Dialog
- Toast / Alert
- Accordion
- Tabs

---

## 🔑 Princípios de design / Design Principles

- **Semântica antes de ARIA** — usar o elemento HTML correto sempre que possível
- **`aria-disabled` em vez de `disabled`** — mantém o elemento focável por leitores de tela
- **`:focus-visible` por padrão** — foco visível incluído em todo componente gerado
- **`.sr-only` incluído** — classe utilitária para conteúdo visível apenas para leitores de tela
- **Framework-agnostic** — HTML/CSS puro, funciona em qualquer stack

---

## 🛠 Como usar / How to use

1. Acesse **https://concego.github.io/ecj-access-toolbox/**
2. Escolha o componente na barra lateral
3. Configure as opções (variante, estados ARIA, textos)
4. Veja o preview em tempo real
5. Copie o código ou baixe o `.html`

A ferramenta é bilíngue — clique em **PT** ou **EN** no cabeçalho.

---

## 💛 Contribuir / Support

Se esta ferramenta ajudou seu projeto, considere apoiar:

[![PayPal](https://img.shields.io/badge/Contribuir-PayPal-ffc439?logo=paypal&logoColor=003087)](https://www.paypal.com/donate/?business=aanderson.carvalho%40hotmail.com&currency_code=USD)

---

## 📦 Estrutura / Structure

```
ecj-access-toolbox/
└── index.html   # Ferramenta completa — single-file app
```

Projeto intencionalmente mantido como arquivo único para máxima portabilidade.  
Intentionally kept as a single file for maximum portability.

---

## 📋 Roadmap

### v1.0 (atual / current) — Free
- [x] Button
- [x] Input Field
- [x] Form Group
- [x] Select / Combobox
- [x] Interface bilíngue PT/EN
- [x] Preview em tempo real
- [x] Download individual por componente

### v2.0 (Ko-fi) — Planned
- [ ] Modal / Dialog
- [ ] Toast / Alert
- [ ] Accordion
- [ ] Tabs
- [ ] Exportação React e Vue

---

## 🤝 Sobre / About

**Eu Concego Jogar (ECJ)** é um projeto de inclusão digital criado por Anderson Carvalho, especialista em acessibilidade com mais de 20 anos de experiência — usuário diário de NVDA e TalkBack.

- 🌐 [Site / Portfolio](https://site.zapia.com/0alwlra4)
- 📧 [euconcego@gmail.com](mailto:euconcego@gmail.com)

---

## 📄 Licença / License

MIT — livre para usar, modificar e distribuir com atribuição.  
MIT — free to use, modify, and distribute with attribution.
