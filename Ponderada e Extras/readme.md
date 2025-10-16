

# HELLO M4: Tutorial Semana 01

Bem vindas(os) ao 4º Módulo do Inteli! 

Esperamos que vocês estejam tão animadas(os) quanto a gente. 

Esse documento deve te ajudar a **conhecer as ferramentas** do módulo e a **explorar os autoestudos** indicados. 

Você também vai encontrar aqui as **instruções da primeira ponderada de programação**. 


## Introdução 

Nesse módulo, como vocês já devem saber, vamos desenvolver projetos com **Internet das Coisas** (ou IoT - Internet of Things). Nesse novo universo de hardwares e componentes, usaremos linguagens de programação (como Arduino e C/C++) para descrever as tarefas que os nossos microcontroladores (as "placas" Arduino e ESP32) irão executar. 

Para que a gente consiga desenvolver os projetos do módulo, construir alguns robôs ou até equipar nossas casas com sistemas inteligentes e cheios de "coisas", vamos precisar começar do começo: também conhecido como *blink*, o `Hello World` do arduíno é fazer um LED piscar. 

Seguindo esse tutorial até o final, você vai conseguir realizar todas as instalações necessárias, preparar o ambiente e conhecer algumas das ferramentas que usaremos nesse módulo. No final desse arquivo, você encontrará a descrição da ponderada de programação.

> **⚠️ ATENÇÃO!** : Essa ponderada é dividida nas partes 1 e 2. **A `parte 1` deverá ser realizada e commitada antes da instrução de programação**. A `parte 2` poderá ser realizada ao longo da semana, com prazo de entrega até sexta-feira.

Estão preparados?


## Autoestudos da Semana 1

Eu sei! Eu sei! Parece coisa demais. Mas eu também sei que até agora vocês conseguiram conhecer um montão de tecnologias diferentes, e elas foram se tornando usuais. Nesse módulo 4 não será diferente!

O que você vai aprender:
- Linguagem de Programação Arduino e C/C++ 
- Microcontrolador Arduino
- Circuito Eletrônico (Simulador e Montagem Física)

<br>
<br>



**1. Conhecer a linguagem (C++)**

No card [`Fundamentos de Linguagem C/C++ (parte I)`](https://en.wikibooks.org/wiki/C%2B%2B_Programming), você vai encontrar um guia da estrutura fundamental da linguagem C++ (organização de Arquivos, declarações, variáveis, tipos, controles de fluxo). É essa linguagem que usaremos para programar nossos microcontroladores.

**2. Conhecendo os materiais (componentes)**

No card [`Explodindo um Capacitor`](https://www.youtube.com/watch?v=C54Cp819Ebc), você vai ser introduzido a alguns componentes eletrônicos importantes para o módulo. Esse vídeo explica brevemente como funciona um circuito eletrônico, introduz um diagrama esquemático, apresenta leds, resistores, potenciômetros, capacitores, relés, diodos e transistores, além de demonstrar o uso de um multímetro. 


**3. Resistores, Corrente, Tensão... E agora?**

No card [`Pode colocar resistor no negativo do LED?`](https://www.youtube.com/watch?v=zxkB4cPuJC8), você vai relembrar conceitos como corrente, tensão, resistência e também observar um circuito com LED, resistor e bateria montado em uma protoboard. Aqui também você vai entender como não queimar seus LEDS!


**4. Como programar Arduino?**

No card [`Instalação de ambiente - Arduino IDE`](https://www.youtube.com/watch?v=B6JMZWqPBsM), você vai entender como instalar a IDE do Arduino, conectar sua placa no seu computador e enviar seus primeiros programas para serem executados no Arduino. 

Faça o download da IDE e explore alguns exemplos aqui: [arduino.cc](https://www.arduino.cc/en/software)

**5. Sobre a Protoboard**

No card [`Como usar a Protoboard`](https://www.youtube.com/watch?v=DfU6llvIMcM), você vai entender como uma protoboard funciona por dentro - e isso vai te ajudar muito nesse módulo. É nessa plaquinha que você vai construir seus circuitos, montando e desmontando enquanto você aprende e testa. Ela funciona como solução temporária para a prototipagem de circuitos.

**6. Sobre o Multímetro**

No card [`Como usar o Multímetro`](https://www.youtube.com/watch?v=1WIWrmc-rBk), você vai entender como o Multímetro pode te ajudar nesse módulo. Ele é um instrumento de medição que pode verificar várias grandezas elétricas, como tensão (voltagem), corrente e resistência. Também usaremos bastante esse equipamento para testar a continuidade de ligações dos nossos circuitos.


**7. Simulador Tinkercad**

Imagina se toda vez que a gente quisesse testar um circuito precisássemos realizar a montagem física da protoboard e dos componentes? No card [`Simulador Tinkercad`](https://www.youtube.com/watch?v=YFq9nPDs0SY), você vai explorar um grande facilitador para esse módulo. Um simulador como o Tinkercad nos faz ganhar tempo e não corremos o risco de queimar nenhum componente!


**8. Projetos com Arduino - Pisca LED (opcional!)**

Se você chegou até aqui, está com a IDE instalada, o Arduino funcionando e está confiante dos seus aprendizados, no card opcional [`Projetos com Arduino - Pisca LED`](https://www.youtube.com/watch?v=t0tCMcDhbZE), você vai encontrar uma demonstração de um projeto básico em Arduino. Este material inclui a montagem de um circuito na protoboard com led e resistor, além da programação do led piscando. Durante a instrução, você terá a oportunidade de montar esse circuito na prática! 


## PONDERADA DE PROGRAMAÇÃO

A imagem a seguir é de um Arduino UNO. Existem diversos modelos de Arduino (UNO, Nano, Mega, Leonardo, entre muitos outros), por isso você precisa tomar algum cuidado quando for procurar uma referência nova na internet.

Na placa, bem ao lado do logotipo do Arduino (o símbolo do infinito), podemos reparar em um pequeno retângulo, com um ponto de luz e um "L". Esse é o **LED INTERNO** do Arduino Uno. Também conhecido como `LED_BUILTIN`, o LED interno está presente na maioria das placas Arduino, e geralmente é conectado ao pino 13. Ele é bastante utilizado para testes de saída digital, como no exemplo clássico do "Blink", facilitando a verificação do funcionamento básico da placa.

<br>
<br>

<div style="text-align: center;">
<img title="Led Interno" src="https://github.com/agodoi/m04-semana01/blob/main/imgs/L_led.png"  style="width: 70%;">
</div>

<br>
<br>


### Parte 1: Blink Led Interno  
> Essa `Parte 1` deverá ser realizada **antes da sua instrução de programação**. 

Instale a Arduino IDE em seu computador e assista aos vídeos indicados nos autoestudos conforme o roteiro descrito anteriormente. Você deverá realizar o "blink" com esse LED Interno e postar em seu GitHub as evidências dessa realização. 

Você vai fazer o led ficar aceso por um tempo X, apagar e aguardar Y segundos e depois voltar a acender, propondo um loop que gera uma "luz piscando".

⚠️ **Entrega Parte 1**: em seu GitHub pessoal (usando sua conta com email Inteli), inserir screenshots de sua tela com o IDE e seu código, além de uma fotografia que demonstre seu Arduino ligado no computador e o seu led aceso. Você também poderá enviar um vídeo que evidencie esse funcionamento.

<br>
<br>

### Parte 2: Simulando Blink Externo
> Essa `Parte 2` pode ser realizada até sexta-feira.

Na imagem anterior do Arduino UNO, os quadradinhos pretos numerados (A0, A1, A2, ..., ~11, 12, 13) são as portas de entrada e/ou saídas para os nossos componentes. Podemos dizer, por exemplo, que um LED está na "porta 6" e que outro está na "porta 13". Nós vamos escrever programas que recebem ou enviam comandos específicos para esses "endereços", por exemplo, definimos o pino 13 como uma saída `pinMode(13, OUTPUT);` e depois enviamos o comando para "ligar o led" `digitalWrite(13, HIGH);`

Nessa `parte 2` você deverá fazer uma simulação **no TinkerCad** com uma montagem do pisca-pisca com Arduino Uno. Ao clicar no play do TinkerCad, o projeto deve executar sem erros uma rotina que simula um pisca-pisca de qualquer cadência. Utilize no projeto um protoboard, ligações elétricas, LED (precisa ser um OFF_BOARD), resistor e um Arduino. 

Envie o link do seu projeto do Tinkercad na Adalove. Obtenha o código do Tinkercad, publique no seu repositório pessoal do GitHub e também envie este link no card.
