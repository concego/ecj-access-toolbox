# 🧰 ECJ Access Toolbox

**Gerador de componentes HTML acessíveis — prontos para produção.**

Criado por [Anderson Carvalho](https://site.zapia.com/0alwlra4) · [Eu Concego Jogar](https://site.zapia.com/0alwlra4)

---

## O que é

O ECJ Access Toolbox é uma ferramenta que gera código HTML acessível e pronto para uso — com ARIA correto, foco visível e semântica real, baseado em WCAG 2.2 e WAI-ARIA 1.2.

Feito para desenvolvedores que estão começando na acessibilidade web e precisam de um ponto de partida sólido, sem ter que decifrar a especificação do zero.

---

## Como usar

### Opção 1 — GitHub Pages (online)

Acesse diretamente no navegador:

👉 **https://concego.github.io/ecj-access-toolbox/**

### Opção 2 — Local (offline)

1. Clone o repositório:
   ```bash
   git clone https://github.com/concego/ecj-access-toolbox.git
   ```
2. Abra o arquivo `index.html` diretamente no seu navegador.

Não precisa de servidor, build, npm, node ou dependências. É um arquivo HTML puro.

---

## Componentes disponíveis (v1)

| Componente | Recursos de acessibilidade |
|---|---|
| **Button** | `aria-disabled`, `aria-busy`, `aria-pressed`, `aria-expanded`, `:focus-visible`, variantes visuais |
| **Input Field** | `<label>` real com `for=`, `aria-describedby`, `aria-required`, `aria-invalid`, `role="alert"` para erro |
| **Form Group** | `<fieldset>` + `<legend>`, radio e checkbox group, foco visível |
| **Select** | Label real, `aria-describedby`, `aria-invalid`, `aria-required`, erro semântico |

---

## Como funciona

1. Escolha o componente na barra lateral
2. Configure as opções (nome, estados, variações)
3. Clique em **Gerar código**
4. Copie ou baixe o arquivo `.html` gerado

---

## Por que HTML puro?

HTML puro é o denominador comum. Qualquer desenvolvedor adapta para React, Vue, Angular ou qualquer outro framework. A ferramenta entrega a base semântica correta — a integração com o framework é decisão sua.

---

## Fundamentos técnicos

- **WCAG 2.2** — critérios de sucesso aplicados em cada componente
- **WAI-ARIA 1.2** — papéis, propriedades e estados corretos
- **Primeira regra do ARIA** — elemento nativo sempre preferido
- **Foco visível** — `:focus-visible` em todos os componentes interativos
- **Semântica antes de estilo** — o código funciona sem CSS

---

## Sobre o autor

Anderson Carvalho é cego, usa NVDA e TalkBack diariamente como sua forma real de navegar pelo mundo — não como simulação de teste.

Trabalha com acessibilidade digital desde 2004: auditorias WCAG, desenvolvimento front-end acessível e inclusão digital. É cofundador do **Eu Concego Jogar**, projeto brasileiro focado na inclusão digital de jogadores cegos e com deficiência visual.

- 🌐 Portfólio: https://site.zapia.com/0alwlra4
- 📧 Contato: euconcego@gmail.com
- 🎮 Projeto: [Eu Concego Jogar](https://site.zapia.com/0alwlra4)

---

## Roadmap

- [x] v1 — Button, Input Field, Form Group, Select (HTML puro)
- [ ] v2 — Modal/Dialog, Toast/Alert, Accordion, Tabs
- [ ] v3 — Export para React e Vue

---

## Licença

MIT — pode usar, modificar e distribuir livremente com atribuição.

---

*ECJ Access Toolbox · Baseado em WCAG 2.2 + WAI-ARIA 1.2*
