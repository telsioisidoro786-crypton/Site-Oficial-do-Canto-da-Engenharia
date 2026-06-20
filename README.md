# Canto da Engenharia

Site institucional de página única (*single-page*) para o movimento juvenil **Canto da Engenharia**, em Luanda, Angola — "Um universo, várias visões".

## ✨ Visão geral

- HTML5 semântico, CSS puro com *custom properties* (design tokens) e JavaScript vanilla — **sem build tooling, sem dependências de NPM**.
- Fundo animado de partículas com [three.js](https://threejs.org/) e *reveals*/transições com [anime.js](https://animejs.com/) (ambos carregados via CDN).
- Modal de **Termos de Participação** acessível: *focus trap*, fecho com `Escape` e clique no overlay, atributos `role="dialog"` / `aria-modal`.
- Formulário de adesão que valida os campos e encaminha o pedido para o WhatsApp da organização.

## 📁 Estrutura

```
canto-da-engenharia/
├── index.html        # site completo (HTML + CSS + JS inline, sem build)
├── README.md
├── LICENSE
└── .gitignore
```

O projeto é deliberadamente um único ficheiro auto-contido. Se no futuro crescer (imagens próprias, múltiplas páginas, formulário com backend), o próximo passo natural é introduzir uma pasta `assets/` para imagens/ícones — sem necessidade de build tooling.

## 🚀 Como executar localmente

Não há dependências para instalar. Basta abrir `index.html` diretamente no navegador, ou servir como ficheiro estático:

```bash
# Opção 1 — sem instalar nada (Python já vem em quase todos os sistemas)
python3 -m http.server 8080

# Opção 2 — Node, sem instalação permanente
npx serve .
```

Depois acede a `http://localhost:8080`.

## 🌐 Deploy

Por ser um único ficheiro estático, pode ser publicado em qualquer serviço de *hosting* estático, sem passos de build:

- **GitHub Pages** — `Settings → Pages → Branch: main → pasta: / (root)`.
- **Netlify / Vercel** — ligar o repositório (sem comando de build, *output directory* = raiz).
- **Hosting tradicional (cPanel, etc.)** — fazer upload direto do `index.html`.

## 🛠️ Pontos de configuração rápida

| O que mudar | Onde procurar em `index.html` |
|---|---|
| Número de WhatsApp (contacto + formulário) | procurar `922040548` / `244922040548` |
| Redes sociais (Instagram, Facebook, Canal/Grupo WhatsApp) | secção `<footer>` → bloco "Redes & Comunidade" |
| Termos de Participação | bloco `#terms-modal` → lista `.modal-terms-list` |
| Cores / paleta da marca | `:root` no `<style>`, variáveis `--grad-*` |
| Tipografia | `:root`, variáveis `--font-d` (display) e `--font-b` (texto corrido) |

## 📄 Licença

Distribuído sob a licença MIT — ver [LICENSE](./LICENSE).
