# Projeto de Microcontroladores

##### Aluno: João Bacelar


### Conceito do projeto
Projeto de firmmware para o microcontrolador STM32F103C8 de maneira à estabelecer comunicação com outro microcontrolador através de um rádio nrf24l01p. Sendo capaz de receber e enviar pacotes de dados via ondas RF. 

### Função

O projeto tem como função utilizar-se do rádio nrf24l01p para estabelecer a comunicação entre robôs de um time de futebol da categoria VSS e um computador rodando os códigos de inteligência, responsável pela tomada de decisões de estados e movimentação do robô. Assim as velocidades desejadas em cada uma das duas rodas do robô a cada ciclo de controle será passada via pacotes por um segundo microcontrolador com um nrf24 em modo de transmissão, que por sua vez recebe os dados do PC via USB.

### Motivação

Uma maneira eficiente de transmitir dados diferentes de um mesmo transmissor para múltiplos receptores sem fio é através de um rádio nrf24l01p. A necessidade de estabelecer o envio das velocidades calculadas pela inteligência para os robôs de maneira rápida e diferente para cada robô motivou ao desenvolvimento do firmmware para utilização do radio.

### Diagrama de Blocos

A comunicação entre o rádio e o microcontrolador é através do protocolo SPI, usando o periférico SPI do microcontrolador. O código para a recepção ou envio de dados é executado em uma task default de um firmmware com FreeRTOS.

##### Diagrama de Blocos da eletrônica:


![Diagrama de Blocos](blocos.png)


