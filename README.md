# MCC1_IFSC_2023_02

**1. PROPOSTA**

Com base na proposta da unidade curricular de Microcontroladores I, foi definido a criação de um projeto de uma fechadura eletrônica. Este projeto seguirá a metodologia CDIO, uma abordagem composta por quatro etapas essenciais: Concepção, Design, Implementação e Operação, as quais serão detalhadas ao longo deste documento.

**2. CONCEPÇÃO**

Nesta etapa, a finalizade é definir os requisitos e os meios para alcançar nossos objetivos que é o desenvolvimento de uma fechadura eletrônica que ofereça segurança e confiabilidade ao usuário. Para isso, estruturamos as condições e tecnologias que serão aplicadas ao projeto:

- **Módulo de Controle e Sensores:**
  O núcleo deste projeto reside no uso do microcontrolador FRDM-KL05Z da Freescale com instruções pré-programadas para gerenciar todos os sensores e interfaces.

- **Fechadura Eletrônica:**
  Será utilizada uma fechadura eletrônica pronta que é acionada com parâmetros de tensão e corrente pré-definidos.

- **Display Incorporado e Controle por Senha:**
  O controle de senha será realizado por meio de um display touchscreen. A interface UART (Universal Asynchronous Receiver-Transmitter) será utilizada para conectar e controlar o display, permitindo a inserção da senha de forma intuitiva.

- **Controle por Impressão Digital:**
  Faremos uso de interfaces GPIO (General Purpose Input/Output) para conectar e controlar um sensor de impressão digital, permitindo o cadastro e a verificação de impressões digitais.

- **Controle por Cartões de Acesso:**
  A interface SPI (Serial Peripheral Interface) será utilizada para conectar um sensor RFID, possibilitando a identificação de cartões eletrônicos cadastrados.

- **Sinalização por Alarme:**
  Para o alarme sonoro, utilizaremos GPIO para controlar um buzzer e gerar alertas sonoros quando necessário.

- **Conectividade com Dispositivos Externos:**
  A interface Bluetooth, que pode ser UART ou SPI, será usada para possibilitar a comunicação com dispositivos externos, como smartphones e computadores.

- **Fonte de Alimentação:**
  A fechadura operará com uma fonte de alimentação de corrente contínua de 12V.

O objetivo principal deste projeto é criar um sistema de controle dinâmico que utilize diversas plataformas de acesso, tornando a comunicação com o usuário mais eficaz e aumentando a segurança. No decorrer do projeto, detalharemos as tecnologias específicas a serem implementadas em cada uma dessas interfaces.

Tabela de requisitos:

| REQUISITOS                           | TIPO DE TECNOLOGIA        | QUANTIDADE |
|--------------------------------------|---------------------------|------------|
| Controle por Impressão Digital      | Sensor Biométrico         | 1          |
| Controle por Cartões de Acesso       | Sensor RFID               | 1          |
| Conectividade com Dispositivos Externos | Módulo Bluetooth        | 1          |
| Sinalização por Alarme               | Buzzer                    | 1          |
| Display Incorporado e Controle por Senha | Display Touchscreen     | 1          |
| Módulo de Controle e Sensores        | Microcontrolador FRDM-KL05Z | 1        |
| Fonte de Alimentação                 | Fonte 12V                 | 1          |
| Fechadura                            | Fechadura Eletrônica      | 1          |` 
____________

