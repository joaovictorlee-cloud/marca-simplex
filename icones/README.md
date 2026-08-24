# Ícones SEO e GEO

24 ícones desenhados no vocabulário geométrico da marca: traço, ângulo reto, triângulo,
hexágono e nó de rede. Mesma família visual do icosaedro e do pattern em `../marca/`.

| Especificação | Valor |
|---|---|
| Grid | 24 × 24 |
| Traço | 1,75 |
| Preenchimento | nenhum, só contorno |
| Cor | `currentColor`, herda do elemento pai |
| Caps e joins | round, para legibilidade em corpo pequeno |

## Os 24

**SEO (15).** `busca` · `palavra-chave` · `ranking` · `trafego-organico` · `backlink` ·
`crawl` · `indexacao` · `serp` · `pagina` · `velocidade` · `dominio` · `auditoria` ·
`sitemap` · `loja-fisica` · `catalogo`

**GEO (9).** `resposta-ia` · `citacao` · `mencao-marca` · `share-of-voice` · `prompt` ·
`zero-click` · `ai-overview` · `modelo-llm` · `visibilidade-ia`

Os termos de busca em português e inglês para cada ícone estão em `sinonimos.json`.

## Como usar

**Arquivo isolado**, para importar em Figma, Canva ou deck: cada ícone é um `.svg`
independente nesta pasta.

**Sprite**, para web:

```html
<svg class="sx-icon"><use href="sprite.svg#sx-icon-visibilidade-ia"/></svg>
```

```css
.sx-icon {
  width: 24px; height: 24px;
  fill: none; stroke: currentColor; stroke-width: 1.75;
  stroke-linecap: round; stroke-linejoin: round;
  color: var(--sx-role-destaque);
}
```

## Regras de cor

O ícone herda `currentColor`, então a cor vem das mesmas regras do resto da marca:

- **Padrão:** a cor do texto ao lado, ou o azul de destaque quando precisa se sobressair
- **Laranja (`#FF6C00`)** só quando o ícone marca uma ação ou um alerta
- **Verde (`#32A62F`)** só quando marca um dado positivo
- Nunca cor fora da paleta da marca

## Ícone dentro do hexágono

Para peças que seguem o padrão de moldura hexagonal (ex.: `simplex.news`), coloque o
ícone dentro do hexágono da marca em vez de usá-lo solto:

```html
<svg viewBox="0 0 100 100" class="sx-icon-hex">
  <polygon points="50,4 90,27 90,73 50,96 10,73 10,27" fill="none" stroke="currentColor" stroke-width="4"/>
  <g transform="translate(26,26) scale(2)"><use href="sprite.svg#sx-icon-radar"/></g>
</svg>
```

Fora desse contexto, prefira o ícone solto: o hexágono é o container das **sub-marcas**,
e usá-lo em todo ícone faz conteúdo comum parecer marca.

## Faltou algum?

Antes de desenhar um novo: confira se algum destes 24 já cobre o conceito por
aproximação — reusar um ícone vizinho vale mais que ter o ícone exato.

Se nenhum servir, siga a mesma regra ao criar um novo: grid 24, traço 1,75, só
contorno, geometria angular. Evite forma orgânica, arredondamento decorativo e ícone
preenchido — nada disso existe no sistema. Depois, cadastre o novo ícone e seus termos
de busca em `sinonimos.json`.
