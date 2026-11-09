# Validação de Portas Ethernet — D-Link DGS-3120-24TC

## Sobre o projeto

Este projeto documenta um procedimento prático de diagnóstico e validação básica de conectividade em um switch gerenciável, utilizando interface serial e comandos de diagnóstico em CLI.

O objetivo foi verificar individualmente o funcionamento das 24 portas Ethernet RJ45, registrando o estado do link, a velocidade de conexão e o modo duplex.

## Equipamento utilizado

- **Fabricante:** D-Link
- **Modelo:** DGS-3120-24TC
- **Interface de gerenciamento:** Console serial
- **Sistema operacional utilizado:** Ubuntu Linux
- **Terminal serial:** Minicom

## Ambiente de testes

A comunicação com o equipamento foi realizada por meio de uma conexão serial entre o computador e o switch.

O acesso ao terminal de comandos permitiu consultar o estado das interfaces e verificar os parâmetros de conexão de cada porta.

## Resultado geral

**24 de 24 portas Ethernet RJ45 aprovadas no teste básico de conectividade.**

- Link: Up
- Velocidade: 1000 Mbps
- Duplex: Full

As interfaces combo foram avaliadas exclusivamente pela conexão física RJ45. As interfaces de fibra óptica não fizeram parte dos testes.

## Documentação

- [Metodologia de testes](docs/metodologia.md)
- [Resultados detalhados](docs/resultados.md)

## Escopo e limitações

Este procedimento avaliou a conectividade física básica das portas Ethernet RJ45.

Não foram realizados testes de transferência de dados entre múltiplos dispositivos, desempenho sob carga, interfaces de fibra óptica ou validação completa dos recursos de gerenciamento do equipamento.

Nenhuma configuração do switch foi alterada durante o procedimento.

## Observação sobre segurança

Informações internas de infraestrutura, como endereços IP, endereços MAC, números de série, nomes de host, credenciais e configurações, foram omitidas para preservar a segurança do ambiente.

---

*Documentação técnica desenvolvida para registro de atividade prática em diagnóstico de infraestrutura de redes.*
