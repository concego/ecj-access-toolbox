<div align="center">

<img src="https://img.shields.io/badge/ECJ-Access%20Toolbox-5b8dee?style=for-the-badge&labelColor=0f1117" alt="ECJ Access Toolbox" />

### Stop writing inaccessible components. Generate the correct code — instantly.

[![Live Tool](https://img.shields.io/badge/🌐%20Open%20the%20tool-concego.github.io-5b8dee?style=flat-square)](https://concego.github.io/ecj-access-toolbox/)
[![WCAG 2.2 AA](https://img.shields.io/badge/WCAG-2.2%20AA-22c55e?style=flat-square)](https://www.w3.org/TR/WCAG22/)
[![WAI-ARIA 1.2](https://img.shields.io/badge/WAI--ARIA-1.2-22c55e?style=flat-square)](https://www.w3.org/TR/wai-aria-1.2/)
[![Components](https://img.shields.io/badge/components-9%20available-f59e0b?style=flat-square)](#components)
[![License: MIT](https://img.shields.io/badge/License-MIT-a78bfa?style=flat-square)](LICENSE)
[![Zero deps](https://img.shields.io/badge/dependencies-zero-64748b?style=flat-square)](index.html)

[**→ Open the tool**](https://concego.github.io/ecj-access-toolbox/) &nbsp;·&nbsp; [Report a bug](https://github.com/concego/ecj-access-toolbox/issues) &nbsp;·&nbsp; [Request a component](https://github.com/concego/ecj-access-toolbox/issues/new?labels=component-request)

</div>

---

## Why this exists

The [WebAIM Million 2026](https://webaim.org/projects/million/) audited one million real websites and found **56 accessibility errors per page on average**. 96% of homepages fail WCAG.

The root cause is rarely malice — it's **knowledge gaps at implementation time**:

- A developer uses `disabled` instead of `aria-disabled` and the button disappears from the keyboard tab order
- An input gets no `<label>` because the placeholder "looks like one"
- A progress bar has no `role="progressbar"` so screen readers announce nothing
- An image is linked but has no alt text, so the screen reader reads the URL

The ECJ Access Toolbox fixes this at the source. Instead of reading the spec, developers **configure the component, see it live, and copy working code** — with correct ARIA, visible focus states, and real HTML semantics baked in.

> I've been working in digital accessibility since 2004. I'm blind and use NVDA and TalkBack every single day. I built this because I got tired of auditing the same 6 mistakes on every project I touch.
>
> — Anderson Carvalho · [Eu Concego Jogar](https://site.zapia.com/0alwlra4)

---

## Key advantages for developers

**No setup, no friction.**
Open the URL. Pick a component. Download the code. There is no install, no account, no API key, no build step, no dependency. It works offline.

**The output is production-ready, not educational.**
Generated code isn't a stripped-down example — it includes the full CSS with focus states, error states, high-contrast support, and `.sr-only` utility. You paste it in and it works.

**Real-time preview as you configure.**
Every change — label text, ARIA state, variant, error message — updates the live preview and the generated code instantly. You see exactly what you'll get before you copy.

**Covers the top errors from real-world audits.**
Components are prioritized by the [WebAIM Million](https://webaim.org/projects/million/) failure rate, not by what's theoretically interesting. The most common mistakes come first.

**Bilingual (PT / EN).**
Full interface and generated code comments available in Portuguese and English.

**Built by someone who depends on assistive technology daily.**
Every component is validated against NVDA + Firefox and TalkBack + Chrome — not just against an automated linter.

---

## Components

### Available now — 9 components

All components are prioritized by the [WebAIM Million 2026](https://webaim.org/projects/million/) — the annual audit of one million real websites.

| Component | What gets generated |
|---|---|
| 🎨 **Color Contrast** — **83.9% of sites fail** | Real-time WCAG ratio calculator with color pickers. Checks AA (4.5:1 normal / 3:1 large) and AAA (7:1 / 4.5:1). Outputs ready-to-use CSS with verified contrast values. |
| 🖼️ **Image Alt Text** — **53.1% of images fail** | Five patterns: informative (`alt="description"`), decorative (`alt=""` + `role="presentation"`), functional (linked image), `<figure>` + `<figcaption>`, and complex image with `aria-describedby`. |
| ✏️ **Input Field** | Input with a real `<label>` (never a placeholder), `aria-required`, `aria-invalid`, `aria-describedby` linking the field to a visible hint and a visible error message. |
| 🔗 **Accessible Link** | Six types: descriptive text, ambiguous text with `aria-label`, external link (new tab + sr-only warning), download link, icon-only link with `aria-label`, and mailto. |
| ☑️ **Form Group** | Checkbox or radio group with `<fieldset>` + `<legend>`, `aria-required` on the group, and proper semantic association between inputs and their labels. |
| 🔘 **Button** | All variants (primary, secondary, danger, ghost) with `aria-disabled` (not `disabled`), `aria-busy` for loading, `aria-pressed` for toggles, `aria-expanded` for disclosures. Visible `:focus-visible` always included. |
| 📋 **Select / Combobox** | Native `<select>` with real `<label>`, accessible placeholder option, `aria-invalid`, visible error message linked via `aria-describedby`, and visible focus state. |
| 📊 **Progress Bar** | Three modes: determinate (`role="progressbar"` + `aria-valuenow/min/max`), indeterminate (`aria-busy="true"`), and step indicator (`aria-current="step"`). All include `aria-live="polite"` for dynamic updates. |
| ⏭️ **Skip Link + Live Region** | Skip link that appears on focus (keyboard users and screen readers), `aria-live` regions (polite and assertive), and `aria-atomic` — the two most forgotten patterns in every audit. |

### Coming next — Phase 2

| Component | Key ARIA patterns |
|---|---|
| 🗔 **Modal / Dialog** | `role="dialog"`, `aria-modal`, focus trap, `aria-labelledby` + `aria-describedby`, focus return on close |
| 🔔 **Toast / Alert** | `role="alert"` vs `aria-live="polite"`, dismissible controls, timeout accessibility, stacking |
| 🗂️ **Accordion** | `aria-expanded`, `aria-controls`, `aria-labelledby`, keyboard navigation (Up/Down/Home/End) |
| 📑 **Tabs** | `role="tablist/tab/tabpanel"`, `aria-selected`, keyboard navigation, automatic vs manual activation |

---

## What the generated code looks like

```html
<!-- Input Field — WCAG 2.2 + WAI-ARIA 1.2 -->
<div class="ecj-field-wrapper">
  <label class="ecj-label" for="email">
    E-mail
    <span class="ecj-required" aria-hidden="true">*</span>
  </label>
  <input
    class="ecj-input ecj-input--error"
    type="email"
    id="email"
    name="email"
    autocomplete="email"
    aria-required="true"
    aria-invalid="true"
    aria-describedby="email-hint email-error"
  />
  <span class="ecj-hint" id="email-hint">Use your work e-mail address.</span>
  <span class="ecj-error" id="email-error" role="alert">Enter a valid e-mail address.</span>
</div>

<style>
  .ecj-input:focus-visible { outline: 3px solid #2563eb; outline-offset: 2px; }
  .ecj-input[aria-invalid="true"] { border-color: #dc2626; }
  .sr-only { position: absolute; width: 1px; height: 1px; overflow: hidden; clip: rect(0,0,0,0); white-space: nowrap; }
</style>
```

Every component output follows the same structure: semantic HTML, ARIA attributes where needed, complete CSS (including focus, error, and disabled states), and a `.sr-only` utility class.

---

## Design principles

Every component in this tool is built on the same non-negotiable rules:

| Rule | Why |
|---|---|
| **Semantics before ARIA** | Use the correct HTML element first. ARIA is a patch, not a foundation. |
| **`aria-disabled` instead of `disabled`** | `disabled` removes the element from the keyboard tab order entirely. `aria-disabled="true"` keeps it reachable and announces its state. |
| **`:focus-visible` on every interactive element** | WCAG 2.2 SC 2.4.11 (Focus Appearance) is AA. Invisible focus is not a style choice — it's a barrier. |
| **`aria-describedby` links visible text** | Error messages and hints are visible text elements linked to inputs — not ARIA strings floating in the DOM. |
| **`.sr-only` shipped with every component** | Screen-reader-only content should be a utility class, not an inline style you copy-paste differently every time. |
| **Self-contained output** | Generated code includes its own CSS. No Tailwind, no Bootstrap, no external stylesheet required. Drop it anywhere and it works. |

---

## Architecture

```
ecj-access-toolbox/
└── index.html   # Complete tool — single-file app (~2,900 lines)
```

Intentionally kept as a single file. No build process, no package manager, no framework.

- Works offline (save the page, it still works)
- Works on GitHub Pages, Netlify, S3, a USB drive, or dropped directly into any project
- Zero supply-chain risk — there is nothing to audit but one HTML file

---

## Roadmap

```
v1.0 ✅  Button · Input Field · Form Group · Select / Combobox · Progress Bar
         Bilingual UI (PT/EN) · Real-time live preview · Per-component download

v1.1 ✅  Color Contrast checker (live WCAG ratio, AA/AAA badges, CSS output)
         Image Alt Text (5 types) · Accessible Link (6 types) · Skip Link + Live Region
         9 components total — covers top 5 WebAIM failure categories

v2.0 🔜  Modal / Dialog · Toast / Alert · Accordion · Tabs

v3.0 📋  React/JSX output · Vue SFC output · Bulk export
         Custom color token support
```

---

## Contributing

Found a bug? [Open an issue](https://github.com/concego/ecj-access-toolbox/issues).

Want to suggest a component? Open an issue with the `component-request` label and include:
- The HTML element or ARIA pattern it addresses
- The common mistake it would prevent
- A real-world example of where you've seen it break

**PRs welcome.** The only requirement: every change must be verifiable with **NVDA + Firefox** and **TalkBack + Chrome** — not just an automated checker.

---

## Support

If this tool saved you time on an audit, a sprint, or a client project:

[![Support via PayPal](https://img.shields.io/badge/Support%20this%20project-PayPal-ffc439?style=flat-square&logo=paypal&logoColor=003087)](https://www.paypal.com/donate/?business=aanderson.carvalho%40hotmail.com&currency_code=USD)

---

## About

**[Eu Concego Jogar (ECJ)](https://site.zapia.com/0alwlra4)** is a digital inclusion project by Anderson Carvalho — accessibility specialist with 20+ years of experience, blind user of NVDA and TalkBack, software developer, and content creator.

*"Concego"* is a Brazilian Portuguese wordplay: *eu consigo* (I can) + *cego* (blind) + *jogar* (play/work).

📧 [euconcego@gmail.com](mailto:euconcego@gmail.com)

---

<div align="center">

*Built with real-world pain. Tested with real screen readers. Made for everyone.*

</div>
