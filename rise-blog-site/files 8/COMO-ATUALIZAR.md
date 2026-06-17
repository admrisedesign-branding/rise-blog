# Blog da RISE — versão BILÍNGUE (PT/EN)

Agora o toggle PT/EN funciona de verdade: troca a página inteira, incluindo o
CORPO dos 10 artigos. O idioma escolhido é lembrado entre páginas (localStorage).

## Como atualizar no GitHub

Você já tem o repo `rise-blog` com a pasta `rise-blog-site/` dentro.
Substitua os arquivos pelos desta pasta:

1. GitHub → repo `rise-blog` → entre na pasta `rise-blog-site/`.
2. Add file → Upload files → arraste o `index.html` novo e a pasta `blog/` (substitui).
3. Commit. O Vercel republica sozinho em segundos.

Domínio e DNS não mudam — só o conteúdo.

## Como o bilíngue funciona
- Cada texto tem duas versões (PT e EN) no HTML; o CSS mostra só a do idioma ativo.
- O botão PT/EN troca o atributo lang do documento e salva a preferência.
- Default: PT. Se o usuário escolher EN, fica EN nas próximas páginas/visitas.
