# Dependências de assets de terceiros

Este repositório público deliberadamente não contém sprites, texturas, animações, controladores de animação, prefabs, modelos, áudio, fontes, scripts ou quaisquer outros arquivos-fonte provenientes dos quatro pacotes abaixo. O fato de um repositório ser público ou privado não substitui a licença de redistribuição do fornecedor.

## Dependência obrigatória da cena principal

### Hero Knight - Pixel Art

- Unity Asset Store product ID: `165188`
- Versão usada na cópia local auditada: `1.2`
- Caminho esperado: `Assets/Hero Knight - Pixel Art`
- Aquisição/instalação: deve ser feita separadamente por cada usuário por meio do Unity Asset Store/Package Manager, sob a licença fornecida pelo autor.

A cena `Assets/Scenes/Quiz1_Movimentacao.unity` contém referências aos seguintes GUIDs:

| GUID | Caminho esperado na versão 1.2 |
| --- | --- |
| `16944a65ef007594a9a62996602798ae` | `Assets/Hero Knight - Pixel Art/Environment/EnvironmentTiles_2.asset` |
| `33dccf83b7f7f294992c97ebe1990464` | `Assets/Hero Knight - Pixel Art/Sprites/Background.png` |
| `932822c3aa72d6245a38fc0e08fe9ef3` | `Assets/Hero Knight - Pixel Art/Environment/EnvironmentTiles_1.asset` |
| `9c497a4ce1f356b448c0dd3eca091d35` | `Assets/Hero Knight - Pixel Art/Environment/Walls_noFriction.physicsMaterial2D` |
| `a3f5e82170913a042b8a1a7ca021cd41` | `Assets/Hero Knight - Pixel Art/Environment/EnvironmentTiles_0.asset` |
| `f094595c900579d4c85a02612d8fa36c` | `Assets/Hero Knight - Pixel Art/Sprites/EnvironmentTiles.png` |

O prefab `Assets/Quiz1/Quiz1Hero.prefab` contém referências aos seguintes GUIDs:

| GUID | Caminho esperado na versão 1.2 |
| --- | --- |
| `2f2a8bdc7f41b704693ad497097f30dc` | `Assets/Hero Knight - Pixel Art/Demo/Sensor_HeroKnight.cs` |
| `3c2a5b7097b0fe44394328c0bdb9252e` | `Assets/Hero Knight - Pixel Art/Animations/HeroKnight_AnimController.controller` |
| `ae297123f091bbf4e8f1835eb98fb293` | `Assets/Hero Knight - Pixel Art/Sprites/HeroKnight.png` |

### Limitação de versão

GUIDs são definidos nos arquivos `.meta` distribuídos pelo fornecedor. Uma versão diferente do pacote, uma importação que regenere `.meta`, ou arquivos renomeados/movidos pode quebrar as referências serializadas mesmo quando o conteúdo visual parece equivalente. A reconstrução fiel requer preferencialmente a versão 1.2 instalada no caminho original. Se os GUIDs divergirem, as referências de Sprite, Animator Controller, Physics Material, Tile assets e script Sensor deverão ser religadas manualmente no Inspector sem copiar os arquivos protegidos para este repositório.

## Pacotes presentes na cópia de desenvolvimento, mas não referenciados pela cena/prefab publicados

Estes pacotes também foram excluídos integralmente. Eles não são necessários para executar a cena principal auditada, mas podem ser adquiridos separadamente caso sejam usados em evolução futura:

| Pacote | Product ID | Versão local auditada | Caminho local excluído |
| --- | ---: | --- | --- |
| Bandits - Pixel Art | `104130` | `2.2` | `Assets/Bandits - Pixel Art` |
| Cainos Village Props | `166114` | `2.3.2` | `Assets/Cainos` |
| Fantasy Wooden GUI Free | `103811` | `2.0` | `Assets/Fantasy Wooden GUI  Free` |

## Diagnóstico depois da instalação

1. Abra `Assets/Scenes/Quiz1_Movimentacao.unity`.
2. Verifique no Console se não há `Missing (Mono Script)` ou referências ausentes.
3. Inspecione `Quiz1Hero` e confirme Sprite/Animator/Sensor.
4. Inspecione Tilemaps e confirme tiles, sprites e material 2D.
5. Execute Play Mode e valide movimento, pulo, animações e a plataforma temporizada.

Sem o Hero Knight instalado, elementos visuais, animações, tiles e o Sensor do prefab ficarão ausentes; essa é uma limitação intencional da distribuição pública sem arquivos licenciados de terceiros.
