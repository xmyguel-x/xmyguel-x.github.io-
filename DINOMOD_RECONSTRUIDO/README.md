# DinoMod reconstruído + NEXUS Fullscreen

Este pacote reúne os módulos JavaScript compilados extraídos do preview original do DinoMod.

## Conteúdo
- `index.html`: estrutura HTML recuperada do preview.
- `assets/index-DX1qfN7c.js`: bundle principal original.
- `assets/routes-a600ZoZK.js`: rota principal e sistema de mods.
- `assets/engine-_K4YV0Me.js`: motor do Dino Runner.
- `assets/batalha-B9bTLxU3.js`: módulo do modo Batalha.
- `assets/styles-Yz9btNF_.css`: estilos originais recuperados.
- `fullscreen.js` e `assets/nexus-fullscreen.css`: complemento NEXUS para tela cheia.

## Como executar
Os módulos usam caminhos absolutos (`/assets/...`) e precisam ser servidos por um servidor HTTP local.
Não abra `index.html` diretamente com `file://`.

Se tiver Python instalado, abra um terminal nesta pasta e execute:
    python -m http.server 8000

Depois abra:
    http://localhost:8000

## Limitações conhecidas
- Os três módulos e o bundle principal foram recuperados como JavaScript compilado, não como os arquivos-fonte originais.
- Os arquivos de imagem do sprite do Dino foram identificados na extração, mas não vieram como dados binários no JSON. O motor pode tentar carregar `/dino/sprite-2x.png` e `/dino/sprite-1x.png`; esses sprites precisam ser copiados para a pasta `dino` para uma execução totalmente offline.
- Fontes IBM Plex Mono e Silkscreen continuam referenciadas pelo Google Fonts, portanto podem depender de internet.
- O botão de tela cheia usa a Fullscreen API do navegador e precisa ser acionado por clique. O navegador pode bloquear a API em contextos não seguros ou incorporados.

## Origem
Reconstrução baseada nos arquivos `NEXUS_LOVABLE_EXTRACTION (1).json` e `DINOMOD_SOURCE_RECOVERY.json` fornecidos nesta conversa.


## Sprites recuperados
- `dino/sprite-1x.png`: spritesheet original em resolução 1x.
- `dino/sprite-2x.png`: spritesheet original em resolução 2x.

Os caminhos do HTML foram ajustados para carregar os arquivos locais em `/dino/`.
