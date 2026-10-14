# Pokémon Emerald Vanilla+ Hybrid — LAN v0.7.0

**Versões experimentais do port nativo para Windows e Android. Documentação em português (Brasil).**

> [!WARNING]
> **Multiplayer ainda em validação.** A compilação e os testes unitários de transporte foram bem-sucedidos na branch de origem, mas **batalhas e trocas completas entre dois aparelhos ainda não foram comprovadas**. Este projeto não é uma versão estável.

## Downloads e versões

| Plataforma | Arquivo de distribuição | Arquitetura | Situação |
|---|---|---|---|
| Windows | `Emerald-Hybrid-LAN-v0.7.0-Windows-x86.zip` | x86 / 32 bits | Build experimental gerado |
| Android | `Emerald-Hybrid-LAN-v0.7.0-Android-armv7.apk` | ARMv7 / 32 bits | APK experimental gerado e assinado para debug |

**Arquivos da distribuição:** devem ser disponibilizados na aba **Releases** após a revisão dos direitos necessários para redistribuição. No momento, este repositório contém a documentação e links para os relatórios de compilação; **não significa que os dois arquivos já estejam publicados aqui**.

- [Compilação Windows no GitHub Actions](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38481402987)
- [Compilação Android no GitHub Actions](https://github.com/Fallzz16/pokeemerald-multiplatform/actions/runs/38481403085)
- [Repositório principal (código-fonte)](https://github.com/Fallzz16/pokeemerald-multiplatform)

As duas compilações citadas são do commit `73b8dd0047b41bd464393d50580618ecaf966728` da branch `feature/lan-hybrid-v070`. **Não incluem** as correções de rede posteriores ainda pendentes de validação.

## O que há no Emerald Hybrid?

O objetivo do projeto é ampliar Pokémon Emerald preservando a experiência em Hoenn. Entre os sistemas presentes na base Hybrid:

- Tipo **Fairy** e divisão de ataques em **Physical / Special / Status (PSS)**;
- Sistema de missões (**Quest UI**);
- Melhorias Vanilla+ e qualidade de vida (QoL);
- Aceleração do jogo (**Tab/F6**) no port Windows;
- Pipeline de sprites **Sprite Bridge**;
- Preservação planejada de história, mapas, treinadores, encontros e saves;
- Transporte **TCP por LAN**, com host/cliente para integração ao Cable Club original.

O código de rede é **experimental**: uma conexão TCP funcionando não comprova que a batalha ou a troca termina corretamente.

## Como funciona o LAN?

1. Instale a **mesma compilação compatível** nos dois dispositivos.
2. Conecte ambos à mesma rede local, sem isolamento de clientes Wi-Fi.
3. No Windows, inicie `LAN_HOST.bat` (host) ou `LAN_JOIN.bat` (cliente); o IP IPv4 informado deve ser o do host.
4. No Android, utilize **Host LAN** ou **Join LAN** na tela inicial do aplicativo.
5. A porta TCP padrão é **45680**. Dentro do jogo, a tentativa de batalha/troca ocorre pelo **Cable Club** original.
6. Faça **backup do save** antes dos testes.

A LAN não oferece matchmaking público pela internet. **O mundo compartilhado de Hoenn ainda não está implementado.**

## Guias em português

| Documento | Conteúdo |
|---|---|
| [Instalação Windows](docs/INSTALACAO_WINDOWS.md) | Extração, controles, conexão LAN e firewall |
| [Instalação Android](docs/INSTALACAO_ANDROID.md) | Compatibilidade ARMv7, APK e conexão |
| [Sobre o projeto](docs/SOBRE_O_PROJETO.md) | Arquitetura, recursos e histórico |
| [Testes e limitações](docs/TESTES_E_LIMITACOES.md) | O que está e não está comprovado |
| [Saves e segurança](docs/SAVES_E_SEGURANCA.md) | Backups e proteção contra perda |
| [Perguntas frequentes](docs/FAQ.md) | Soluções para dúvidas comuns |
| [Aviso legal](docs/AVISO_LEGAL.md) | Direitos de distribuição e afiliação |
| [Notas desta versão](NOTAS_DA_VERSAO.md) | Origem dos builds e pendências |

## Desenvolvimento

- [Branch LAN v0.7.0](https://github.com/Fallzz16/pokeemerald-multiplatform/tree/feature/lan-hybrid-v070)
- [Branch experimental de correções não bloqueantes](https://github.com/Fallzz16/pokeemerald-multiplatform/tree/feature/lan-v070-async-slot-hardening)
- [Pull Request de correções (rascunho)](https://github.com/Fallzz16/pokeemerald-multiplatform/pull/1)

**Projeto independente, não afiliado à Nintendo, The Pokémon Company ou GAME FREAK.** A publicação de modificações ou código de ferramentas não concede automaticamente o direito de redistribuir arquivos, marcas e recursos protegidos do jogo. Consulte [o aviso legal](docs/AVISO_LEGAL.md).
