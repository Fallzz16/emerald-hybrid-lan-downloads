# Emerald Hybrid LAN v0.7.0 — Notas da versão experimental

**Estado:** candidato para testes, ainda sem aprovação de gameplay LAN ponta a ponta.

## Pacotes preparados

- `Emerald-Hybrid-LAN-v0.7.0-Windows-x86.zip` — EXE x86, SDL2.dll, `LAN_HOST.bat`, `LAN_JOIN.bat`, instruções.
- `Emerald-Hybrid-LAN-v0.7.0-Android-armv7.apk` — app SDL2 nativo Android ARMv7/32 bits, launcher offline/host/cliente, controles touchscreen e assinatura debug.

**Situação atualizada em 19/10/2026:** ambos os binários estão anexados à [Release pública de tag `Pokemon`](https://github.com/Fallzz16/emerald-hybrid-lan-downloads/releases/tag/Pokemon). A disponibilidade pública não é validação de jogabilidade ou autorização de redistribuição de ativos de terceiros; consulte o aviso legal.

## Recursos presentes no projeto Hybrid

Fairy Type, divisão Physical/Special/Status, Quest UI, melhorias QoL/Vanilla+, fast-forward para desktop e Sprite Bridge. A conexão TCP/LAN utiliza o Cable Club tradicional como alvo de integração, mas ainda não possui comprovação de batalhas/trocas concluídas em dois dispositivos reais.

## Origem verificada

- [Repositório-fonte](https://github.com/Fallzz16/pokeemerald-multiplatform)
- Branch: `feature/lan-hybrid-v070`.
- Commit dos builds: `73b8dd0047b41bd464393d50580618ecaf966728`.
- [Workflow Windows — execução 38481402987](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38481402987).
- [Workflow Android — execução 38481403085](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38481403085).

## Ainda não comprovado

Batalha completa e troca confirmada no Cable Club, save pós-troca, instalação e jogabilidade em celular físico, Windows↔Android, reconexão após quedas de rede, latência real e mundo compartilhado.

As melhorias da branch `feature/lan-v070-async-slot-hardening` e a arquitetura posterior **EHL8/M2.3** **não foram incorporadas aos dois binários v0.7.0**. Para distinguir os pacotes, consulte [Estado das versões](STATUS_DAS_VERSOES.md).

## Segurança

Faça backups antes de testar. A edição Android só suporta ARMv7, e trocar APKs de debug pode causar conflito de assinatura ou perda de saves se o app for desinstalado.

[Guia Windows](docs/INSTALACAO_WINDOWS.md) · [Guia Android](docs/INSTALACAO_ANDROID.md) · [Testes pendentes](docs/TESTES_E_LIMITACOES.md) · [Aviso legal](docs/AVISO_LEGAL.md).