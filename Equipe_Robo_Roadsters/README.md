# CONCEPÇÃO DO PROJETO

Vivemos em uma época em que muitos problemas foram solucionados pela tecnologia, e muitos outros ainda nos incomodam como uma pedra no sapato. É a era da revolução digital, eletrônica e mecânica, portanto, continuamos a buscar mais e mais soluções tecnológicas. A ascensão da indústria 4.0 e o uso da IoT dentro das empresas que trouxe grandes melhorias para os processos industriais e, pensando na produção de larga escala, o transporte de produtos e materiais é uma etapa muito importante que merece atenção. 
Utilizando um robô capaz de fazer o transporte autônomo de forma inteligente, podemos obter grandes vantagens, sendo elas:

* Eficiência operacional: Carrinhos podem operar de forma contínua, sem tempo de descanso;
* Redução de custos de mão de obra: A automação do transporte elimina a necessidade de trabalhadores realizarem tarefas de transporte manual, economizando em custos de mão de obra e potencialmente reduzindo erros humanos;
* Segurança: Carrinhos autônomos são projetados com sensores avançados que podem detectar obstáculos e evitar colisões, tornando o transporte mais seguro para os funcionários e  os equipamentos;
* Precisão: Esses carrinhos podem ser programados para seguir trajetórias precisas, o que é particularmente útil em ambientes industriais onde é essencial evitar danos aos produtos durante o transporte;
* Flexibilidade: Os carrinhos autônomos podem ser reprogramados ou reconfigurados rapidamente para se adaptar a mudanças nas necessidades de transporte da indústria;
* Rastreamento e monitoramento: Muitos sistemas autônomos são equipados com tecnologia de rastreamento e monitoramento, permitindo que os gerentes de operações acompanhem a localização e o status dos carrinhos em tempo real;
* Aumento na capacidade de transporte: Carrinhos autônomos podem ser programados para trabalhar em conjunto e otimizar rotas, aumentando a capacidade de transporte da indústria;
* Redução de danos: A automação pode ajudar a reduzir danos a produtos durante o transporte, pois os carrinhos autônomos podem ser programados para evitar solavancos, choques e outros movimentos bruscos;

Alguns possíveis benefícios mais gerais também podem surgir da automação de veículos e robôs, sendo elas:

* Acessibilidade e autossuficiência: Pessoas com mobilidade reduzida e pessoas de idade avançada que não poderiam dirigir, teriam acesso a carros.
* Segurança e patrulhamento: Carros autônomos ou com uma rota pré-definida podem fazer patrulhas de monitoramento e fiscalização;
* Conforto: Pessoas embriagadas ou cansadas não precisariam dirigir;
* Acidentes: A maioria dos acidentes ocorrem por falha humana;
* Velocidade: Carros autônomos, se conectados em rede, poderiam diminuir expressivamente congestionamentos. Além disso, não precisam estacionar por perto, poderiam simplesmente ir embora e voltar quando preciso, ou estacionar mais longe, procurando vagas sozinho;
* Economia e sustentabilidade: Com menos filas, menos combustível ou energia seriam gastos;


## REQUISITOS DE PROJETO
Nosso projeto visa exemplificar a implementação de um sistema de transporte utilizando o carro autônomo desenvolvido pelo Laboratório de Pesquisa Avançada em Eletrônica (LPAE) do Instituto Federal de Santa Catarina - Campus Florianópolis. Os seguintes requisitos de projeto foram estabelecidos:

1. O veículo deve conseguir se comunicar com o celular de forma remota via bluetooth;
2. Monitorar e enviar o status de sua posição atual para o celular;
3. O veículo deve ser teleoperado, através do celular o usuário terá controle total do carrinho;
4. Deve ter modo de operação **Seguidor de linha** que, quando definido pelo usuário, o carrinho seguirá um percurso definido por uma linha no chão;
5. O veículo também deve ter a opção de seguir até uma coordenada destino (x, y) definida pelo usuário;
6. Deve desviar de objetos de forma autônoma;
7. Monitoramento da bateria;


## TECNOLOGIAS EMPREGADAS

* O controle do carrinho será feito utilizando um aplicativo para celular android. A comunicação entre o carrinho e o celular ocorrerá a partir do módulo bluetooth HC-05 que utiliza comunicação serial UART.

* O sistema de odometria que monitora a posição do veículo será implementado utilizando uma fusão de sen	sores, sendo eles: Sensores de posição, encoders e uma IMU (Inertial Measurements Units) composta por giroscópio e acelerômetro.
  
* O controle manual será empregado diretamente pelo aplicativo android no celular e os comandos serão enviados via bluetooth.

* Para seguir a linha será utilizado um arranjo com dois sensores de linha, dessa forma será possível identificar quando o carrinho estiver se desviando do percurso definido pela linha e para qual direção ele precisa se ajustar.

* Será utilizado o um sistema de controle PID para permitir que o carrinho se movimente até a coordenada passada, dessa forma podemos garantir que o carrinho chegará no destino de forma mais precisa.

* Para detectar obstáculos, serão utilizados os sensores de proximidade ultrassônicos HC-SR04, por serem acessíveis e fáceis para a aplicação.
  
* O monitoramento da bateria será feito utilizando um amplificador diferencial conectado ao ADC do microcontrolador. 

* Será necessário o desenvolvimento de um adaptador para compatibilidade do microcontrolador com a placa de potência do veículo.

* O microcontrolador utilizado será o KL05Z, requisito obrigatório para a aplicação.

## DIAGRAMA DE BLOCOS
<p align=center> 
Figura 1 - Diagrama de Blocos do Projeto 
</p>

<div align="center">

![Diagrama de Blocos](https://github.com/ciceroed/MCC1_IFSC_2023_02/blob/main/Equipe_Robo_Roadsters/Diagrama%20de%20Blocos.jpg)

</div>

A imagem acima exemplifica, de forma simplificada, o que foi descrito no tópico "Tecnologias Empregadas". Podemos verificar como cada periférico irá se comunicar com o microcontrolador e a comunicação com a interface para o usuário. Além do controle dos motores por meio de ponte H e a realimentação da posição a partir dos encoders. 
