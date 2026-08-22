# eu & gabi — linha do tempo

Site estático de página única (`index.html` + `css/` + `js/` + `images/`), sem build, sem dependências além de fontes do Google Fonts.

## Como subir no GitHub Pages

1. Crie um repositório novo no GitHub (ex: `dois-anos` ou `nossa-timeline`).
2. Dentro desta pasta (`site/`), rode:
   ```
   git init
   git add .
   git commit -m "primeira versão da linha do tempo"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/NOME_DO_REPO.git
   git push -u origin main
   ```
3. No GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root)**.
4. Em alguns minutos o site fica em `https://SEU_USUARIO.github.io/NOME_DO_REPO/`.

> Repositório precisa ser **público** pra usar o GitHub Pages gratuito (a menos que você tenha GitHub Pro/Team, aí dá pra ter Pages num repo privado).

## O que falta / o que revisar

- Todas as fotos já foram incluídas — não sobrou nenhum placeholder pendente.
- O trecho da última conversa (seção "a última conversa") foi adaptado da conversa de 16/08/2026 sobre o mirante — dei uma enxugada, tirando as partes sobre dinheiro/logística e mantendo o que era mais sobre vocês duas. Se quiser trocar por outro trecho, ele está direto no `index.html`, dentro de `<div class="chat-window">`, cada linha é um `<div class="chat-bubble me">` (mensagens suas) ou `<div class="chat-bubble them">` (mensagens da Gabi).
- Depois da última conversa, a página segue num segundo capítulo — "diário da observabilidade" — com o pós-término: dias na academia, café/almoço com o seu pai, o primeiro domingo sozinha, as fotos de progresso do bíceps, a prancha. Esse conteúdo veio do seu diário real; só usei as partes que falam de você mesma e deixei de fora trechos que citavam outras pessoas (colegas de trabalho, seus pais, comparações com relacionamentos passados), pra não expor ninguém numa página pública com nomes reais. Se quiser incluir algo desses trechos de um jeito diferente (mais editado, sem nomes, etc.), é só pedir.
- O contador final ("dias vividos juntas" etc.) usa 25/ago/2024 como início e 31/jul/2026 como o dia em que o término foi confirmado no chat — ajuste as datas em `js/script.js` (constantes `START`, `END_FULL`, `LAST_DAY`) se quiser marcar outro dia como referência.

## Estrutura

```
site/
├── index.html      → todo o conteúdo e textos da timeline (história do casal + capítulo pós-término)
├── css/style.css   → tema escuro cinematográfico
├── js/script.js    → animações de scroll, contador, lightbox das fotos
├── images/         → todas as fotos já convertidas pra .jpg/.png
└── README.md       → este arquivo
```
