# Sobre o projeto

**Pokémon Emerald Vanilla+ Hybrid v0.7.0** é uma continuação técnica do port multiplataforma de Emerald, preservando a proposta Vanilla+ e adicionando recursos modernos.

## Funcionalidades do Hybrid

- Tipo Fairy.
- Categorias Physical / Special / Status aplicadas aos golpes.
- Quest UI para missões.
- Melhorias QoL/Vanilla+, com atenção à compatibilidade de progresso.
- Fast-forward no port de desktop, incluindo Tab/F6.
- Sprite Bridge para importação opcional.
- Base original de Hoenn, com história, mapas e encontros preservados conforme o projeto.

## Arquitetura do LAN

O modo de rede atual usa dois jogadores conectados por **TCP host/cliente** (IPv4 e porta padrão 45680), transportando dados do link serial do Emerald. A integração utiliza o Cable Club original para **tentar** batalhas e trocas.

A implementação da branch `feature/lan-hybrid-v070` introduziu arquivos no diretório `src/lnet/` (rede, sessões, slots, emulação serial), adaptou `src/link.c` e integrou opções de LAN ao SDL2 e à interface Android. O transporte tem testes unitários e de loopback; **jogabilidade LAN completa permanece pendente**.

## Plataformas

**Windows:** port nativo SDL2, distribuído como EXE x86 com `SDL2.dll`, `LAN_HOST.bat` e `LAN_JOIN.bat`.

**Android:** port nativo SDL2, atualmente somente ARMv7 32 bits, com launcher offline/host/join e controles touchscreen.

As builds documentadas nesta distribuição vieram do commit `73b8dd0047b41bd464393d50580618ecaf966728`. Uma branch posterior de melhoria de slots TCP não bloqueantes está separada e **não faz parte desses binários**.

## Estado do Modo C

- **Fase 1:** validar batalhas, trocas e robustez da conexão usando o Cable Club.
- **Fase 2:** planejar e implementar Hoenn compartilhada, com entidades remotas, IDs de sessão/mapa, movimento, interpolação, entrada/saída e desconexões.

A Fase 2 **não está implementada**. Evite confundir um canal TCP com multiplayer de mundo compartilhado.

[Código-fonte e histórico](https://github.com/Fallzz16/pokeemerald-multiplatform) · [Branch LAN](https://github.com/Fallzz16/pokeemerald-multiplatform/tree/feature/lan-hybrid-v070).