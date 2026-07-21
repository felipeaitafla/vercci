# Vercci Construtora — prévia estática

Export estático da home para preview na Vercel. Site final é **WordPress**
(tema standalone `vercci`); este repositório é só para revisão visual.

## Deploy na Vercel

Site estático sem build. Ao importar o repositório:

- **Framework Preset:** Other
- **Build Command:** deixar vazio
- **Output Directory:** deixar vazio (a raiz já é o site)

## Estrutura

```
index.html          home renderizada, caminhos relativos
assets/css/         colors_and_type.css (tokens) + styles.css
assets/js/          lenis.min.js (rolagem suave, servido localmente)
assets/fonts/       Inter Tight self-hosted (woff2, variável 300–500)
assets/images/      .avif das seções + logos + textura de ruído
```

Sem dependências externas: nenhuma requisição sai do domínio.

## O que está nesta prévia

Seções 1 a 3.2: Hero, Depoimentos, Nossos Serviços e Como te Ajudamos /
Administração de Obras. Portfólio (seção 4) em diante ainda não foi construído.

## Ressalvas

- **Depoimentos são fictícios.** O bloco é um placeholder de layout
  (`Cliente exemplo A/B/C/D`) que existe só enquanto o plugin Trustindex não
  está ativo. No site real ele é substituído pelo widget do Google. Não usar
  este conteúdo como se fossem avaliações reais.
- Formulários e links de WhatsApp apontam para destinos reais, mas nada é
  processado — não há backend nesta prévia.
- Regenerar após mudanças no tema: o export é gerado a partir do WordPress
  local, não editar `index.html` à mão.
