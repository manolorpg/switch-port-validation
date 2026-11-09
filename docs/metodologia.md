# Metodologia de Testes

## 1. Objetivo

Verificar individualmente a conectividade física das 24 portas Ethernet RJ45 de um switch gerenciável D-Link DGS-3120-24TC.

## 2. Ambiente e ferramentas

- Switch D-Link DGS-3120-24TC.
- Computador com Windows.
- Máquina virtual Ubuntu Linux.
- VirtualBox para comunicação com a porta serial.
- Minicom 2.10 para acesso ao console.
- Cabo Ethernet previamente testado.
- Interface de rede Ethernet do computador utilizado no teste.

## 3. Acesso ao equipamento

O acesso ao switch foi realizado por meio do console serial.

Parâmetros utilizados:

| Parâmetro | Configuração |
|---|---|
| Dispositivo serial | `/dev/ttyS0` |
| Velocidade | 115200 bps |
| Bits de dados | 8 |
| Paridade | Nenhuma |
| Bits de parada | 1 |
| Controle de fluxo | Desabilitado |

Após estabelecer a comunicação, foi realizado o acesso à interface CLI do equipamento.

## 4. Procedimento de validação

O teste foi realizado individualmente em cada uma das 24 portas RJ45.

Foram utilizados o mesmo cabo Ethernet e o mesmo computador durante todas as verificações.

Sequência executada:

1. Conectar o cabo Ethernet à porta avaliada.
2. Verificar a indicação luminosa de conexão no switch.
3. Verificar a indicação de conexão na interface de rede do computador.
4. Consultar o estado da interface pelos comandos de diagnóstico.
5. Registrar o estado do link, a velocidade e o modo duplex.
6. Repetir o procedimento até completar as 24 interfaces.

## 5. Comandos utilizados

Para consultar o estado das portas: `show ports 1-24`.

Para verificar individualmente uma interface: `show ports <número_da_porta>`.

Esses comandos permitem consultar o estado das interfaces e identificar eventuais falhas de conectividade.

## 6. Critério de aprovação

Uma porta foi considerada aprovada quando apresentou:

- Link estabelecido (Link Up).
- Velocidade de conexão de 1000 Mbps.
- Operação em Full Duplex.

A avaliação também considerou a indicação luminosa de conexão no switch e no computador.

## 7. Cuidados durante o procedimento

- Foi utilizado um cabo Ethernet previamente testado.
- O mesmo computador foi utilizado em todas as verificações.
- Nenhuma configuração do equipamento foi modificada.
- Não foram realizados procedimentos de reset ou atualização de firmware.
- O teste foi limitado à conectividade física das interfaces RJ45.

## 8. Limitações

O procedimento não contempla testes de desempenho, transferência de dados entre múltiplos dispositivos, validação de recursos avançados do switch ou funcionamento das interfaces de fibra óptica.
