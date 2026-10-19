# Qual versão do Emerald Hybrid estou vendo?

**Consulta em 19/10/2026.** O repositório de downloads é um registro de distribuições; o desenvolvimento acontece em [pokeemerald-multiplatform](https://github.com/Fallzz16/pokeemerald-multiplatform).

| Linha | Origem exata | Disponibilidade | O que foi comprovado |
|---|---|---|---|
| **LAN v0.7.0** | `feature/lan-hybrid-v070`, commit `73b8dd0047b41bd464393d50580618ecaf966728` | Dois arquivos anexados à [Release de tag `Pokemon`](https://github.com/Fallzz16/emerald-hybrid-lan-downloads/releases/tag/Pokemon): Windows x86 e Android ARMv7 | Compilação e inspeções estáticas dos pacotes; **não** batalhas/trocas completas entre aparelhos |
| **EHL8 / M2.3-B2 (desenvolvimento)** | `feature/emerald-v100-m23a-server-first-lab`, commit `59b94d1a6b2411f85b0eac8a12d31cb7b92fc73f` | [Preview Windows completo no Actions](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38994717968), **não** na Release v0.7.0 | Jobs `game`, `gui-tools` e `portable` concluídos; QA gráfico/humano do fluxo M2.3 ainda pendente |

## Compatibilidade e limites

- **Não misture** executáveis, servidor, launcher, Lab, DLLs, APKs ou perfis de builds diferentes. Prefira sempre o pacote completo de uma mesma revisão.
- **LAN v0.7.0** usa o canal TCP P2P do Cable Club; o servidor **EHL8** e o Lab da branch mais recente são uma arquitetura distinta. Não suponha compatibilidade entre protocolos.
- A porta `45680` aparece em ambos os fluxos em situações diferentes; isso **não** torna os protocolos compatíveis.
- Um build aprovado no CI não comprova batalha/troca, Android real, crossplay, saves após gameplay ou mundo compartilhado. Esses itens necessitam validação separada.
- A Release v0.7.0 está marcada como publicação normal no GitHub, **mas o software continua explicitamente experimental**. Publicação não é aprovação de estabilidade ou autorização automática para redistribuir material de terceiros.
- Os SHA-256 publicados em [SHA256SUMS.txt](SHA256SUMS.txt) foram registrados para os pacotes preparados da v0.7.0. Para verificar o conteúdo de um download, recalcule o hash localmente e compare; estes valores não certificam a jogabilidade nem a segurança do programa.
- **Para QA EHL8**, use o [roteiro M2.3-A/B2](https://github.com/Fallzz16/pokeemerald-multiplatform/blob/feature/emerald-v100-m23a-server-first-lab/docs/V100_M23A_SERVER_FIRST_QA_PTBR.md), com saves de teste isolados.

## Links de referência

- [Release histórica da v0.7.0](https://github.com/Fallzz16/emerald-hybrid-lan-downloads/releases/tag/Pokemon)
- [Repositório principal](https://github.com/Fallzz16/pokeemerald-multiplatform)
- [PR #19 — desenvolvimento EHL8](https://github.com/Fallzz16/pokeemerald-multiplatform/pull/19)
- [Windows Preview completo, SHA correspondente ao PR #19](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38994717968)
- [Direitos e distribuição](docs/AVISO_LEGAL.md)

> Este registro descreve o estado verificado acima. Novos commits ou releases exigem atualizar a tabela e as evidências antes de declarar uma funcionalidade aprovada.
