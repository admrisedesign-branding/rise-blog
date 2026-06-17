# Blog RISE — versão FINAL (bilíngue PT/EN + favicon + navbar nova)

## ⚠️ O ERRO QUE ACONTECEU ANTES
Os uploads anteriores subiram o ARQUIVO .ZIP (que o GitHub NÃO descompacta) ou
criaram pastas aninhadas (files 8, files 10). Por isso o site continuava antigo.

## ✅ O JEITO CERTO DE SUBIR (sem zip!)
1. DESCOMPACTE o .zip no seu Mac (dois cliques). Vai virar a pasta `rise-blog-site`.
2. ABRA a pasta. Dentro tem: index.html + pasta blog/ (com 11 arquivos).
3. No GitHub, a forma mais limpa é começar do zero (veja abaixo).

## LIMPEZA + UPLOAD CORRETO (recomendado)
Como o repo está bagunçado (blog antigo, files 8, files 10), o melhor é:
1. GitHub → repo rise-blog → entre na pasta rise-blog-site.
2. Apague as pastas/arquivos antigos: blog (a antiga), files 8, files 10,
   index.html, COMO-PUBLICAR.md (deixe o repo limpo).
3. Add file → Upload files → arraste de DENTRO da pasta descompactada:
   o index.html E a pasta blog/ (NÃO o zip, NÃO a pasta rise-blog-site inteira).
4. Commit.

## VERCEL
- Root Directory deve ser: rise-blog-site
- Após o upload, Deployments → Redeploy (sem cache).
- Teste em aba anônima: blog.riseagencia.com/blog/pitch-apresentacao-gestor-publico.html
  → clique EN (deve traduzir) e veja o favicon "R" laranja na aba.
