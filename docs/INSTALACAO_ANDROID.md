# Instalação no Android — Emerald Hybrid LAN v0.7.0

## Compatibilidade

Esta compilação é um **APK Android nativo baseado em SDL2**, e não um emulador de ROM. O arquivo experimental `Emerald-Hybrid-LAN-v0.7.0-Android-armv7.apk` contém bibliotecas **armeabi-v7a (32 bits)**. Em celulares que aceitam apenas aplicativos 64 bits, pode não instalar.

Requisitos de compilação reportados: Android com API mínima **21**, permissão `INTERNET`, Android SDK 34 e SDL2 2.30.7.

## Instalação

1. Obtenha o APK de uma fonte autorizada e confira sua origem.
2. Faça cópia de qualquer save de testes anterior antes de substituir aplicativos.
3. Abra o APK no celular e siga as permissões normais de instalação de aplicativo externo, se disponíveis.
4. Abra o aplicativo e comece por **Play offline**, verificando inicialização, tela, botões, som e save.

**Atenção:** instalação e execução real em aparelho ainda não foram comprovadas pelos testes de CI existentes. O APK foi compilado e verificado estaticamente.

## Menu inicial

- **Play offline:** iniciar sem sessão LAN.
- **Host LAN:** criar sessão na rede local e exibir IPv4 local quando disponível; porta padrão `45680`.
- **Join LAN:** inserir o IPv4 do host (por exemplo `192.168.1.50`) e porta opcional `45680`.

Os controles touchscreen incluem direcional, A, B, Start, Select, L e R.

Dois aparelhos devem estar em uma rede local acessível, sem isolamento de clientes. Para conexão com Windows, use builds do mesmo conjunto experimental e IP do dispositivo host.

## Proteção de dados e limitações

O save Android utiliza armazenamento privado do aplicativo. **Desinstalar pode apagar os dados do jogo.** APKs de debug de execuções diferentes podem ter assinaturas distintas e falhar ao atualizar; não desinstale uma versão antiga sem garantir backup utilizável.

O mundo compartilhado não existe nesta versão e batalha/troca LAN ainda não foram comprovadas. Leia [Saves e segurança](SAVES_E_SEGURANCA.md) e [Testes e limitações](TESTES_E_LIMITACOES.md).