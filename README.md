# LP Workshop Black Friday 2026 · UPFY

Página de captação do workshop gratuito de 21/10/2026, 12h. Todos os botões levam ao grupo VIP do WhatsApp.

## Estrutura

```
wrangler.jsonc            configuração do Worker (serve a pasta public/)
public/
  index.html              a LP (CSS, JS e logo dentro do arquivo)
  privacidade.html        Política de Privacidade (abre em /privacidade)
  _headers                cabeçalhos de segurança e cache
  favicon.png             ícone da aba
  apple-touch-icon.png    ícone ao salvar no celular
  og-image.jpg            imagem de compartilhamento (WhatsApp, Instagram, Facebook)
```

## Antes de ligar os anúncios

1. Preencher em `public/privacidade.html` os campos marcados em amarelo: [CNPJ], [ENDEREÇO COMPLETO], [PRAZO], [NOME DO ENCARREGADO], [E-MAIL DE PRIVACIDADE].
2. Se o domínio não for `workshop.upfy.net.br`, trocar esse endereço nas linhas `og:url`, `og:image` e `canonical` do `index.html` e do `privacidade.html`.

## Onde trocar o link do grupo

No fim do `index.html`, bloco CONFIGURAÇÃO: `groupUrl`.

## Tracking

- GTM-TH22KBV com Consent Mode v2 (tudo negado até aceitar os cookies).
- Clique em qualquer botão do grupo: `dataLayer.push({event:'cta_click', cta_location, lp_name:'LP Workshop Black'})`.
- A tag "Meta - Evento - Contact" do GTM dispara sozinha no clique (link para chat.whatsapp.com).
- Para o GTM disparar neste domínio, nada muda: é o mesmo container.

## UTM para os anúncios

`https://workshop.upfy.net.br/?utm_source=meta&utm_medium=paid&utm_campaign=workshop-black-2026&utm_content={anuncio}`
