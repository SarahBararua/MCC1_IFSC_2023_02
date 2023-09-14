# CONCEPÇÃO DO PROJETO

Vivemos em uma época em que muitos problemas foram solucionados pela tecnologia, e muitos outros ainda nos incomodam como uma pedra no sapato. É a era da revolução digital, eletrônica e mecânica, portanto, continuamos a buscar mais e mais soluções tecnológicas. Um exemplo é a ascensão da indústria 4.0 e o uso da IoT dentro das empresas que trouxe grandes melhorias para os processos industriais. 
Pensando na produção de larga escala, uma etapa muito importante é o transporte de produtos e materiais. 
Utilizando um robô capaz de fazer o transporte autônomo de forma inteligente podemos obter grandes vantagens, sendo elas:

* Eficiência operacional: Carrinhos podem operar de forma contínua sem tempo de descanso;
* Redução de custos de mão de obra: A automação do transporte elimina a necessidade de trabalhadores para realizar tarefas de transporte manual, economizando em custos de mão de obra e potencialmente reduzindo erros humanos;
* Segurança: Carrinhos autônomos são projetados com sensores avançados que podem detectar obstáculos e evitar colisões, tornando o transporte mais seguro para os funcionários e equipamentos;
* Precisão: Esses carrinhos podem ser programados para seguir trajetórias precisas, o que é particularmente útil em ambientes industriais onde é essencial evitar danos aos produtos durante o transporte;
* Flexibilidade: Os carrinhos autônomos podem ser reprogramados ou reconfigurados rapidamente para se adaptar a mudanças nas necessidades de transporte da indústria;
* Rastreamento e monitoramento: Muitos sistemas autônomos são equipados com tecnologia de rastreamento e monitoramento, permitindo que os gerentes de operações acompanhem a localização e o status dos carrinhos em tempo real;
* Aumento na capacidade de transporte: Carrinhos autônomos podem ser programados para trabalhar em conjunto e otimizar rotas, aumentando a capacidade de transporte da indústria;
* Redução de danos: A automação pode ajudar a reduzir danos a produtos durante o transporte, pois os carrinhos autônomos podem ser programados para evitar solavancos, choques e outros movimentos bruscos;


Alguns possíveis benefícios mais gerais também podem surgir da automação de aumtomóveis e/ ou robôs, sendo elas:

* Acessibilidade e autossuficiencia: Pessoas com mobilidade reduzida e pessoas de idade avançada que não poderiam dirigir, teriam acesso á carros.
* Segurança e patrulhamento: Carros autônomos ou com uma rota prédifinida podem fazer patrulhas de monitoramento e fiscalização;
* Conforto: Pessoas embriagadas ou cansadas não precisariam dirigir;
* Acidentes: A maioria dos acidentes ocorrem por falha humana;
* Velocidade: Carros autônomos, se conectados em rede, poderiam diminuir expressivamente congestionamentos. Além disso, não precisam estacionar por perto, poderiam simplesmente ir embora e voltar quando preciso, ou estacionar mais longe, procurando vagas sózinho;
* Economia e sustentabilidade: Com menos filas, menos combustível ou energia seriam gastos;


## REQUISITOS DE PROJETO
Nosso projeto visa exemplificar a implementação de um sistema de transporte utilizando o carro autônomo desenvolvido pelo LPAE. Os seguintes requisitos de projeto foram estabelecidos:

1. O veículo deve conseguir se comunicar com o dispositivo de controle de forma remota;
2. Monitorar e enviar o status de sua posição atual para o dispositivo de controle.
3. Deve ter modo de operação **manual**;
4. Deve ter modo de operação **Seguidor de linha**;
5. Deve ter modo de operação **piloto automático**;
6. Deve desviar de objetos;
7. Monitoramento da bateria;


## TECNOLOGIAS EMPREGADAS

O controle do carrinho será feito utilizando um aplicativo para celular android. A comunicação entre o carrinho e o celular ocorrerá a partir do módulo bluetooth HC-05 que utiliza comunicação serial UART.

Para detectar obstáculos, serão utilizados os sensores de proximidade ultrassônicos HC-SR04, por serem acessíveis e fáceis para a aplicação. 

O sistema de odometria que monitora a posição do veículo e permite que ele se movimente até uma coordenada de entrada será implementado utilizando uma fusão de sensores, sendo eles: Sensores de posição, encoders e uma IMU (Inertial Measurements Units) composta por giroscópio e acelerômetro.

O controle manual será empregado diretamente pelo aplicativo android no celular e os comandos serão enviados via bluetooth.

O monitoramente da bateria será feito utilizando um amplificador com ganho de 1/3 conectado ao ADC do microcontrolador. 

Para seguir a linha será utilizado um arranjo com dois sensores de linha.

Será necessário o desenvolvimento de um adaptador para compatibilidade do microcontrolador com a placa de potência do veículo.


