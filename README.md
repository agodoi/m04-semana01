# Professor André Godoi

* Graduado em Engenharia Elétrica;
* Mestre em Engenharia Elétroca;
* Doutor em Engenharia de Computação.
* Especialista em IoT
* Proprietário da Inova Fusca (@inovafusca)

* <picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m04-semana01/blob/main/imgs/inovafusca.png">
   <img alt="Tecnologias Módulo 02" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m04-semana01/blob/main/imgs/inovafusca.png)">
</picture>

# Horários de Atendimento

Todas terças e quintas, das 8h às 16h.


# Semana 01 - Programação com TinkerCad e Arduino IDE

## Aula de Hoje
- **Ambiente do TinkerCad**
- **Ambiente do Arduino IDE**
- **Eletrônica Básica**



<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m04-semana01/blob/main/imgs/divisor_aguas.png">
   <img alt="Tecnologias Módulo 02" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m04-semana01/blob/main/imgs/divisor_aguas.png)">
</picture>


---

## Ambiente TinkerCad

### Componentes
À direita da tela do TinkerCad, você encontrará a lista de componentes como a imagem abaixo.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m04-semana01/blob/main/imgs/Captura%20de%20tela%202024-10-17%20090405.png">
   <img alt="Tecnologias Módulo 02" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m04-semana01/blob/main/imgs/Captura%20de%20tela%202024-10-17%20090405.png)">
</picture>

### Botão Código
- Utilize o modo **somente TEXTO** para inserir o código-fonte.
- O pisca-pisca vem como código-fonte padrão.

### Monitor Serial
- Serve para interagir com o Arduino Uno, imprimindo dados de saída e inserindo dados de entrada no Arduino.
- Utiliza a porta USB para comunicação com o ESP32.

### Baud Rate
- **Baud rate**: a taxa de comunicação da porta serial, que deve ser a mesma no `Serial.begin` e no monitor serial.
- Valores padrão: 9600bps e 115200bps. O de menor valor é para projetos simples, o de maior valor, para projetos mais profissionais.

### Botão Iniciar Simulação
- Compila e executa o código.
- Seus projetos são armazenados na sua conta do TinkerCad.

---

## Matriz de Contato (Breadboard)
- A fila de 5 furos permite o contato elétrico entre os 5 furos.
- A fila é isolada das vizinhas.
- Linhas vermelhas e pretas são réguas de contatos de uma ponta a outra, mas as linhas de cima e de baixo não se conectam automaticamente.
- O protoboard tem um “sulco” que separa a matriz em duas metades isoladas.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m04-semana01/blob/main/imgs/proto.png">
   <img alt="Tecnologias Módulo 02" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m04-semana01/blob/main/imgs/proto.png)">
</picture>

---

## Prática no TinkerCad
### Objetivo:
- Monte o circuito: **LED vermelho** com resistor de **330Ω** no pino 2 do Arduino Uno R3, e um botão no pino 3 com resistor **1kΩ** de pull-down.
- Fonte de 5V alimentando o sistema.

### Programação:
- **LED aceso** enquanto pressiona o botão.
- **LED apagado** quando o botão não é pressionado.
- Imprima no **Monitor Serial**: "led aceso" e "led apagado".

---

## Ambiente Arduino IDE

### Estrutura Básica:
- Funções obrigatórias:
  ```cpp
  void setup() {
    // Configurações iniciais
  }
  
  void loop() {
    // Algoritmo principal
  }
  ```

---

## Prática no Arduino IDE - Exemplo do Fade
### Passos:
1. Abra o Arduino IDE.
2. Vá em **Arquivo > Exemplos > Básico > Fade**.
3. Substitua `LED_BUILTIN` pelo pino 2 (ESP32 não reconhece `LED_BUILTIN`).
4. Selecione a placa **DOIT ESP32 DEVKIT V1** e a porta COM correta.
5. Descarregue o programa e observe o LED azul nativo da placa.

---

## ESP32 - Pinout
### Funções dos Pinos GPIO
- Atenção aos pinos que alteram o estado durante o boot (evitar relés ou sensores que devolvem dados nos pinos: 01, 02, 03, 04, 05, 12, 13, 14 e 15).
- Pinos que funcionam apenas como **input digital**: 34, 35, 36, 39.
- **ADC2** não funciona se WiFi estiver ativo.

---

## Ponderada

Até a sexta-feira dessa semana, cada aluno deverá enviar o seu GitHub particular para a correção.
Nesse GitHub deve conter prints e fotos compondo o seu relatório que o enunciado solicita.
