# Relatório de integridade — builds experimentais

**Preparação dos pacotes:** 13 de outubro de 2026.

Os dois pacotes de distribuição foram preparados a partir dos artefatos GitHub Actions da branch `feature/lan-hybrid-v070`, commit `73b8dd0047b41bd464393d50580618ecaf966728`.

| Plataforma | Workflow | Artefato |
|---|---|---|
| Windows x86 | [38481402987](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38481402987) | `11856184806` |
| Android ARMv7 | [38481403085](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38481403085) | `11855704989` |

Na preparação anterior, foram feitas as seguintes verificações estáticas: extração íntegra do ZIP Windows, presença de `pokeemerald.exe` e `SDL2.dll`, cabeçalho PE x86; verificação da estrutura ZIP do APK, bibliotecas `libSDL2.so` e `libmain.so` da ABI `armeabi-v7a`, `classes.dex`, manifest e elementos de assinatura debug; testes de leitura dos arquivos e registro SHA-256 dos dois pacotes.

**Não foram comprovados:** ausência de vulnerabilidades, jogo iniciando em hardware real, controles/som/save sob gameplay, conclusão de batalhas/trocas LAN e mundo compartilhado.

Os hashes em [SHA256SUMS.txt](../SHA256SUMS.txt) referem-se aos **pacotes de distribuição preparados**. Não devem ser confundidos com os hashes dos ZIPs originais do GitHub Actions.

Este relatório descreve a verificação de empacotamento, não uma certificação de jogabilidade. **Atualização de publicação (19/10/2026):** os dois pacotes v0.7.0 constam na [Release pública de tag `Pokemon`](https://github.com/Fallzz16/emerald-hybrid-lan-downloads/releases/tag/Pokemon). Os hashes registrados aqui não foram recalculados a partir dos assets baixados nesta revisão documental; compare os SHA-256 localmente antes de usar. Consulte também [Estado das versões](../STATUS_DAS_VERSOES.md).