# Syntax Highlighting for Gantry 5

A Gantry 5 Particle that lets you display beautifully formatted, syntax-highlighted code blocks on your Joomla or WordPress site — powered by [Prism.js](https://prismjs.com/).

<img width="478" height="269" alt="2026" src="https://github.com/user-attachments/assets/c1136277-b1b1-4ae2-a63c-66ce7bf17529" />

---

## Features

- Syntax highlighting via Prism.js (v1.29.0)
- Optional line numbers
- One-click **Copy** button with visual feedback
- Optional title/heading above the code block
- Language label displayed in the toolbar
- Support for 10 languages out of the box, with more loaded automatically via Prism's autoloader
- Optional custom CSS class on the wrapper for extra styling control

---

## Supported Languages

| Label        | Language   |
|--------------|------------|
| HTML / XML   | `markup`   |
| CSS          | `css`      |
| JavaScript   | `javascript` |
| PHP          | `php`      |
| Python       | `python`   |
| SQL          | `sql`      |
| Bash         | `bash`     |
| TypeScript   | `typescript` |
| JSON         | `json`     |
| YAML         | `yaml`     |

Additional languages are loaded on demand by Prism's autoloader plugin.

---

## Files

| File | Purpose |
|------|---------|
| `codehighlight.yaml` | Particle configuration and admin form fields |
| `codehighlight.html.twig` | Twig template — renders the HTML, loads Prism.js, and handles copy-to-clipboard |
| `_codehighlight.scss` | SCSS styles for the particle |
| `custom.scss` | Entry point to import `_codehighlight.scss` into your theme |

---

## Installation

1. Copy the particle files into your Gantry 5 theme's particle directory:

   ```
   templates/<your-theme>/custom/particles/
   ```

   Place these three files there:
   - `codehighlight.yaml`
   - `codehighlight.html.twig`

2. Copy the SCSS files into your theme's custom SCSS directory:

   ```
   templates/<your-theme>/custom/scss/
   ```

   Place these two files there:
   - `_codehighlight.scss`
   - `custom.scss` *(or merge its contents into your existing `custom.scss`)*

3. Clear the Gantry cache via **Gantry 5 → Extras → Clear Cache**.

4. The **Code Highlight** particle will now be available in the Gantry Layout Manager.

---

## Configuration

In the Gantry 5 admin, drag the **Code Highlight** particle into your layout and configure the following fields:

| Field | Description |
|-------|-------------|
| **Enabled** | Show or hide the particle |
| **Title** | Optional heading displayed above the code block |
| **Language** | The programming language for syntax highlighting |
| **Code** | The code to display |
| **Line Numbers** | Toggle line number display |
| **CSS Class** | Optional extra CSS class on the outer wrapper |

---

## Dependencies

Prism.js and its plugins are loaded from cdnjs.cloudflare.com at runtime — no local installation required.

- `prism.min.js` (core)
- `prism-tomorrow.min.css` (dark theme)
- `prism-autoloader.min.js` (lazy-loads language grammars)
- `prism-line-numbers` (loaded only when line numbers are enabled)

---

## License

MIT — free to use and modify.
