# Instalação no Windows — Emerald Hybrid LAN v0.7.0

## Requisitos

- Computador Windows compatível com executáveis x86 (32 bits).
- Rede local para tentar a conexão LAN com outro jogador.
- Permissão do Firewall para receber conexões TCP na porta `45680`, caso o sistema solicite.

## Executar o jogo

1. Obtenha o pacote `Emerald-Hybrid-LAN-v0.7.0-Windows-x86.zip` de uma fonte autorizada.
2. Extraia **todos** os arquivos para uma pasta própria. Não execute o EXE de dentro do ZIP.
3. Confirme que `pokeemerald.exe` e `SDL2.dll` estão na mesma pasta.
4. Abra `pokeemerald.exe` para tentar jogar offline. Não é necessário um emulador GBA separado.

## Multiplayer LAN experimental

**Host:** abra `LAN_HOST.bat` ou execute:

```bat
pokeemerald.exe --lan-host=45680
```

**Cliente:** abra `LAN_JOIN.bat` e informe o IP do host, ou execute:

```bat
pokeemerald.exe --lan-client=192.168.1.50:45680
```

O endereço acima é **somente um exemplo**: no computador host, use `ipconfig` e localize o endereço IPv4 real da rede ativa. Os dois jogadores devem usar builds compatíveis, estar na mesma LAN e entrar no **Cable Club** dentro do Emerald para tentar batalha ou troca.

Se necessário, permita o tráfego **TCP de entrada na porta 45680** somente em redes privadas confiáveis. Redes Wi-Fi de convidados podem isolar os clientes.

## Gerar logs para depuração

```bat
pokeemerald.exe --lan-log host.log --lan-host=45680
pokeemerald.exe --lan-log cliente.log --lan-client=192.168.1.50:45680
```

O argumento `--lan-log` deve aparecer **antes** do parâmetro de rede.

## Saves e cuidados

O save Windows é `pokeemerald.sav`. Faça cópia antes de testar LAN e evite usar sua única gravação valiosa nas builds experimentais. A ausência de erros de compilação **não garante** que batalhas, trocas e salvamentos estejam estáveis.

Para limitações: [Testes e limitações](TESTES_E_LIMITACOES.md).