# Saves e segurança — como evitar perda de progresso

## Windows

O port utiliza um arquivo chamado `pokeemerald.sav`. Localize o save da instalação experimental e crie uma cópia **antes** de testar multiplayer ou substituir os executáveis. Guarde a cópia em outro diretório e não a sobrescreva durante QA.

## Android

O aplicativo utiliza armazenamento privado do Android (pasta própria de dados do app). A remoção/desinstalação pode excluir esse armazenamento. APKs debug produzidos em execuções diferentes podem ter chaves de assinatura distintas e não aceitar instalação como atualização.

**Não desinstale o aplicativo para resolver conflito de assinatura antes de confirmar um método efetivo de exportar e restaurar o save.** Sem isso, não há garantia de preservar dados.

## Testes seguros

- Use uma gravação de teste em cada dispositivo, distinta do seu save principal.
- Registre versão do APK/EXE, plataforma, data e origem dos artefatos.
- Confirme que o jogo carrega o save antes de iniciar qualquer conexão LAN.
- Verifique novamente os Pokémon e o inventário depois de batalhas e trocas de teste.
- Em caso de erro ou encerramento inesperado, pare e preserve cópias dos saves e logs para diagnóstico.

## Rede local

Use redes confiáveis. Evite liberar a porta TCP 45680 na internet pública ou desativar todo o firewall. Não compartilhe logs contendo informações privadas sem revisão.

As builds e o tratamento de desconexão ainda não foram validados em todas as circunstâncias. Consulte [Testes e limitações](TESTES_E_LIMITACOES.md).