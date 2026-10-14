# Perguntas frequentes

### Preciso de um emulador de GBA?

Não. Estas distribuições são **ports nativos SDL2** para Windows e Android.

### A batalha e a troca por LAN já funcionam 100%?

**Ainda não foi comprovado.** O transporte de rede foi implementado e testado isoladamente; a jogabilidade completa entre dois dispositivos aguarda testes.

### Posso usar o APK em qualquer celular?

Não. O APK desta versão é **armeabi-v7a/32 bits**; telefones exclusivamente 64 bits podem rejeitar a instalação.

### Windows e Android podem jogar juntos?

Esse é um objetivo da implementação, mas a compatibilidade ponta a ponta ainda está **pendente de validação**.

### Quais são o IP e a porta?

A porta padrão é **45680/TCP**. O cliente informa o **IPv4 local do host**, que varia de rede para rede. `192.168.1.50` é só um exemplo.

### Posso usar meu save principal?

Não é recomendado durante o desenvolvimento experimental. Use cópias e saves de teste. No Android, desinstalar pode remover dados privados do aplicativo.

### O modo LAN mostra outros jogadores andando em Hoenn?

Não. O **mundo compartilhado não foi implementado**. A fase atual foca o sistema original de batalha/troca do Cable Club.

### Por que os links da Release podem não mostrar os binários?

O repositório pode conter somente a documentação enquanto os direitos de distribuição e os anexos da pré-release são resolvidos. Compilar arquivos e publicá-los são etapas distintas.

### Onde estão as atualizações de código?

No [repositório principal](https://github.com/Fallzz16/pokeemerald-multiplatform). A branch `feature/lan-hybrid-v070` contém a base deste candidato; `feature/lan-v070-async-slot-hardening` contém melhorias posteriores **ainda não compiladas nesses dois pacotes**.