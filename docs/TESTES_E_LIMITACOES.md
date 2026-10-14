# Estado dos testes e limitações

Este documento distingue **código implementado**, **compilação aprovada** e **funcionalidade comprovada em jogo**. Esses estados não são equivalentes.

## Evidências verificadas para o commit dos binários

| Área | Resultado conhecido |
|---|---|
| Windows x86 — GitHub Actions | Build concluído com sucesso |
| Android ARMv7 — GitHub Actions | Gradle/CMake e validação estática do APK concluídos com sucesso |
| LAN — testes de transporte | 71 verificações reportadas como aprovadas (27 de sessão, 44 de link) na branch de origem |
| Android — instalação em dispositivo real | Não verificado |
| Windows ↔ Windows, batalha/troca | Não verificado |
| Android ↔ Android, batalha/troca | Não verificado |
| Windows ↔ Android, batalha/troca | Não verificado |
| Interrupção de Wi-Fi, timeout e reconexão no jogo real | Não verificado |
| Mundo compartilhado | Não implementado |

Relatórios originais:
- [Build Windows](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38481402987).
- [Build Android](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38481403085).

## Critérios para declarar LAN funcional

1. Conectar dois clientes de **mesma build compatível** e identificar ambos os jogadores.
2. Entrar no Cable Club e concluir uma batalha real sem inconsistências.
3. Executar uma troca real, confirmar os Pokémon nos dois lados e salvar corretamente.
4. Repetir os testes em Windows/Windows, Android/Android, Windows/Android e Android/Windows.
5. Encerrar o host, interromper Wi-Fi, cancelar a conexão, variar latência e verificar recuperação sem corromper saves.
6. Verificar áudio, comandos, FPS, fast-forward, tela, ciclo de vida Android e ausência de regressões do Hybrid.

## Riscos e limites atuais

O protocolo serial precisa conciliar cadência de emulação, filas de comandos e tempo de resposta da rede. Transporte TCP conectando não prova que a máquina de estados do jogo completou o handshake. Wi-Fi lento pode causar atraso, estagnação de filas ou desconexão durante operações mais longas. Atualizações futuras devem comprovar esse comportamento com logs e testes reais.

O APK experimental suporta apenas **ARMv7 32 bits**. A publicação de um APK não garante instalação em aparelhos recentes exclusivamente de 64 bits.

**Não marque esses itens como aprovados sem evidência.**