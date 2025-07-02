# **SAP-1 como Microcontrolador — com Timer, Porta de Entrada e Comunicação Serial (UART)**

Este projeto é uma extensão do microcomputador didático SAP-1 (Simple-As-Possible 1), baseado na arquitetura apresentada por Cláudio et al. (versão 5), implementado no **Logisim**.  
O objetivo foi transformar o SAP-1 em um microcontrolador funcional, adicionando periféricos essenciais como Timer, Porta de Entrada de 8 bits e uma Unidade de Comunicação Serial.

## **Descrição**

A arquitetura original do SAP-1 foi expandida com três blocos funcionais conectados ao barramento de dados e à Unidade de Controle, permitindo simulação de entrada/saída e temporização. Essa adaptação serve como base para o estudo de microcontroladores simples com arquitetura Harvard modificada e controle programável.

## **Funcionalidades**

* **Base SAP-1 versão 5** com todos os componentes principais: PC, IR, ACC, B, RAM, ULA, UC, Registrador de Saída.  
* **Timer de 8 bits**:
  * Contador que incrementa com clock separado.
  * Leitura via controle manual ou instrução simulada.
* **Porta de Entrada de 8 bits**:
  * Simula sensores ou switches externos.
  * Dados podem ser lidos no acumulador.
* **Unidade Serial (UART simplificada)**:
  * Registradores TX (transmissão) e RX (recepção).
  * Permite simular envio e recepção de dados via controle.
* **Expansão da UC (Unidade de Controle)**:
  * Novos sinais de controle para leitura de Timer, Porta e TX/RX.
  * Suporte a instruções simuladas (`IN`, `OUT`, `READ_TIMER`).
* **Barramento único com integração total** entre periféricos e memória.

## **Como Usar**

1. Abra o arquivo `.circ` no **Logisim**.
2. Use os botões de controle manual para:
   - Ativar leitura do Timer
   - Ler da Porta de Entrada
   - Enviar dados via TX ou ler do RX
3. Execute ciclos de clock e observe os dados fluindo no barramento.
4. Opcional: simule novas instruções ajustando o decodificador de instruções da UC.

## **Arquitetura SAP-1 Expandida**

| Componente | Descrição |
|------------|-----------|
| PC         | Contador de Programa |
| IR         | Registrador de Instruções |
| MAR        | Registrador de Endereço de Memória |
| RAM        | Memória de 16x8 |
| ACC / B    | Registradores de dados |
| ULA        | Somador e Subtrator com controle |
| UC         | Unidade de Controle expandida |
| OUT        | Registrador de Saída |
| **TIMER**  | Contador de 8 bits com leitura |
| **IN**     | Entrada de 8 bits via Input |
| **TX/RX**  | Unidade de Comunicação Serial |

## **Tecnologia Utilizada**
* **Logisim** — Simulador de circuitos digitais de código aberto.

## **Video**
* https://youtu.be/QKKQU-N-jg8

## **Autores**
* **Matheus Augusto**
* **Marcus Meleiro**
* **Ary Gomes da Costa**
* **Davi Wenzel Cury**
  
* Baseado em projeto de Cláudio et al. — SAP Versão 5 
