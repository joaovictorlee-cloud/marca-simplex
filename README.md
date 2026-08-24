# Marca Simplex

Fonte pública da marca **Simplex Analytics** em formato legível por máquina.

Um arquivo, `marca.json`, com paleta, tipografia, regras de logo, pattern, tom de voz e os
12 inegociáveis. Mais os vetores oficiais em `logos/` e os 24 ícones conceituais de
SEO/GEO em `icones/` (ver `icones/README.md`).

## Consumir

```bash
curl -s https://raw.githubusercontent.com/joaovictorlee-cloud/marca-simplex/main/marca.json
```

```python
import json, urllib.request
URL = "https://raw.githubusercontent.com/joaovictorlee-cloud/marca-simplex/main/marca.json"
M = json.load(urllib.request.urlopen(URL))

M["cor"]["laranja"]["hex"]        # "#FF6C00"
M["cor"]["laranja"]["papel"]      # onde pode e onde não pode usar
M["tipografia"]["oficial"]        # "Gilroy"
M["inegociaveis"]                 # as 12 regras que não se quebram
```

## Procedência

Cada regra vem marcada, e isso decide o que se pode discutir:

| Marca | Significado |
|---|---|
| **BB** | Está no brandbook oficial de 2021. Não se discute |
| **ASSET** | Vem de arquivo oficial. Use o arquivo, não recrie |
| **CONV** | Convenção interna, sem lastro documental. Pode mudar |

## Versionamento

O campo `versao` usa `AAAA.MM.DD`. Quem consome compara esse campo para saber se há
mudança. Toda alteração de marca sobe a versão.

## O que não está aqui

Tipografia Gilroy é comercial e licenciada: os binários não são distribuídos. Sem licença,
o substituto é **Poppins** no Google Workspace e **Outfit** na web. O logo não depende
disso — os SVG em `logos/` já trazem o wordmark em curvas.

Portfólio comercial, ICP e material de venda ficam no repositório privado da Simplex.
