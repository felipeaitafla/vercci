# Vercci Construtora — prévia estática

Export estático para preview na Vercel. Site final é **WordPress** (tema
standalone `vercci`); este repositório é só para revisão visual.

## Deploy na Vercel

Site estático sem build. Ao importar o repositório:

- **Framework Preset:** Other
- **Build Command:** deixar vazio
- **Output Directory:** deixar vazio (a raiz já é o site)

## Estrutura

```
index.html                      home renderizada, caminhos relativos
politica-de-privacidade.html    página de política (texto jurídico)
assets/css/                     colors_and_type.css (tokens) + styles.css
assets/js/                      lenis.min.js (rolagem suave, servido localmente)
assets/fonts/                   Inter Tight self-hosted (woff2, variável 300–500)
assets/images/                  .avif das seções + portfólio + logos + ruído
```

## O que está nesta prévia

Todas as 12 seções do copy: Hero, Depoimentos, Nossos Serviços, Como te
Ajudamos / Administração de Obras, Portfólio, Diferenciais, Ambiental,
Retrofit, Benefícios / Quem Somos, Unidades, Contato e Rodapé — mais a página
de Política de Privacidade.

## Ressalvas

- **Depoimentos são fictícios.** O bloco é um placeholder de layout
  (`Cliente exemplo A/B/C/D`) que existe só enquanto o plugin Trustindex não
  está ativo. No site real ele é substituído pelo widget do Google.
  **Não usar este conteúdo como se fossem avaliações reais** e não abrir esta
  prévia ao público enquanto ele estiver aqui.
- **O formulário não envia.** Sem backend na prévia, o `action` foi trocado por
  uma âncora inerte. No WordPress ele funciona (nonce, honeypot e `wp_mail`),
  mas as caixas `leads@` e `marketing@` ainda não existem.
- Links de WhatsApp e mapas apontam para destinos reais.
- **Regenerar após mudanças no tema** — o export sai do WordPress local, não
  editar os `.html` à mão.

## Requisições externas

Duas, ambas na seção de Unidades: os `<iframe>` do Google Maps, exigidos pela
§4.5 do padrão. Todo o resto (fontes, CSS, JS, imagens) é servido localmente.
