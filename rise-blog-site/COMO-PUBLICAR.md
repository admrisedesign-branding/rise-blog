# Blog da RISE — Como publicar

Blog estático completo, no estilo do Neuroplasticidar, com a identidade da RISE
(preto #070508, laranja #E8531A, Bricolage Grotesque + DM Sans).

## O que tem aqui

```
rise-blog-site/
├── index.html                     ← redireciona pra /blog/
└── blog/
    ├── index.html                 ← LISTAGEM (header editorial + filtros + cards)
    └── [10 artigos].html           ← cada artigo (CTA + relacionados + footer)
```

Tudo é **HTML estático** — sem build, sem dependências. Abre em qualquer navegador.

## Funcionalidades

- Header próprio do blog (logo RISE + navegação + "← Voltar ao site")
- Listagem editorial com filtro por categoria (Todos / GovTech / Branding / Marketing)
- Cards com tarja colorida por categoria + data + tempo de leitura
- Página de artigo com categoria, data, tempo de leitura, autor
- CTA laranja no fim de cada artigo (puxa pra contato/serviços da RISE)
- "Outros artigos que podem te interessar" (relacionados por categoria)
- 100% responsivo (menu hambúrguer no mobile)

## Onde os links apontam

O "Voltar ao site", o CTA e a navegação apontam pra `https://riseagencia.com`.
Se quiser mudar, é só editar a constante `SITE_URL` (ou buscar/trocar no HTML).

---

## Publicar (recomendado: Vercel + subdomínio)

Mesmo esquema que você já usou no Capta.

### 1. Subir pro Vercel
- Crie um repositório no GitHub (ex: `admrisedesign-branding/rise-blog`) e suba esta pasta.
- No Vercel → New Project → importe o repo. Não precisa configurar build
  (é estático); só "Deploy".

### 2. Apontar o subdomínio `blog.riseagencia.com`
- No Vercel → projeto → Settings → Domains → adicione `blog.riseagencia.com`.
- No Hostinger (DNS), crie um registro **CNAME**:
  - Nome/Host: `blog`
  - Valor: o destino que o Vercel mostrar (ex: `cname.vercel-dns.com`)
- Aguarde propagar (alguns minutos).

### 3. Ligar o menu do site (Webflow) ao blog
No Webflow, edite o link "Blog" do menu:
- URL: `https://blog.riseagencia.com`
- Marque **"Open in new tab"** (abrir em nova aba) — o comportamento que você quis.

Pronto: clicar em "Blog" abre o blog em nova aba; dentro dele, os artigos abrem
na mesma aba; e "Voltar ao site" traz de volta pro riseagencia.com.

---

## Editar / adicionar artigos depois

Cada artigo é um arquivo `.html` em `blog/`. Pra um novo artigo, o mais simples é
copiar um existente e trocar título, categoria, data, tempo e corpo — e adicionar
um card novo no `blog/index.html`. (Se preferir automatizar, o gerador em Python
que criou isso pode ser reaproveitado.)
