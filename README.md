# Arapinha Pneus — Site

Landing page da Arapinha Pneus (alinhamento, balanceamento e vulcanização), com duas unidades em Belo Horizonte: Jardim Alvorada e Alípio de Melo.

Site estático de página única, sem build (HTML/CSS/JS puros em um único arquivo). Deploy direto no Netlify a partir da raiz deste repositório.

## Estrutura

```
index.html       # site inteiro (marcação, estilos e scripts)
robots.txt        # instruções para crawlers de busca
sitemap.xml       # sitemap para o Google Search Console
_headers          # cabeçalhos de segurança usados pelo Netlify
```

## Rodando localmente

Não há dependências nem build. Basta abrir o `index.html` no navegador, ou servir a pasta com qualquer servidor estático, por exemplo:

```bash
python -m http.server 8000
# depois acesse http://localhost:8000
```

## Deploy

O deploy no Netlify é feito publicando o conteúdo desta pasta (raiz do repositório) diretamente — não há passo de build.

## SEO

- `robots.txt` libera a indexação e aponta para o `sitemap.xml`.
- `sitemap.xml` lista a home do site para o Google Search Console.
- `index.html` inclui meta tags (description, Open Graph, canonical) e dados estruturados (JSON-LD) do tipo `AutoRepair` com as duas unidades.

Após alterações no conteúdo, reenviar o sitemap e solicitar reindexação da home no Google Search Console.
