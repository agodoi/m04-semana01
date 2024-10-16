# Professor André Godoi

* Graduado em Engenharia Elétrica;
* Mestre em Engenharia Elétroca;
* Doutor em Engenharia de Computação.
* Especialista em IoT
* Proprietário da Inova Fusca (@inovafusca)

# Horários de Atendimento

Todas terças e quintas, das 8h às 16h.


# Semana 01 - Programação com TinkerCad e Arduino IDE

## Aula de Hoje
- **Ambiente do TinkerCad**
- **Ambiente do Arduino IDE**
- **Eletrônica Básica**
- **Ponteiro e Gerenciamento de Memória**

---

## Ambiente TinkerCad

### Componentes
À direita, você encontrará a lista de componentes.

### Botão Código
- Utilize o modo **somente TEXTO** para inserir o código-fonte.
- O pisca-pisca vem como código-fonte padrão.

### Monitor Serial
- Serve para interagir com o Arduino Uno, imprimindo dados de saída e inserindo dados de entrada no Arduino.
- Utiliza a porta USB para comunicação com o ESP32.

### Baud Rate
- **Baud rate**: a taxa de comunicação da porta serial, que deve ser a mesma no `Serial.begin` e no monitor serial.

### Botão Iniciar Simulação
- Compila e executa o código.
- Seus projetos são armazenados na sua conta do TinkerCad.

---

## Matriz de Contato (Breadboard)
- A fila de 5 furos permite o contato elétrico entre os 5 furos.
- A fila é isolada das vizinhas.
- Linhas vermelhas e pretas são réguas de contatos de uma ponta a outra, mas as linhas de cima e de baixo não se conectam automaticamente.
- O protoboard tem um “sulco” que separa a matriz em duas metades isoladas.

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

## Ponteiros
- **Ponteiros** são variáveis que armazenam o endereço de memória de outra variável.
- Exemplo de declaração de ponteiro:
  ```cpp
  int x = 9;
  int *pt = &x;
  ```
- **&** é usado para obter o endereço de uma variável.

### Atenção:
- Manipulação direta de memória pode ser perigosa, devendo ser feita com cautela para evitar falhas e instabilidade do sistema.

---

## Práticas com Ponteiros

### Exemplo 1
```cpp
char x;

void setup(){
  Serial.begin(9600);
  Serial.print("Endereco x: ");
  Serial.println((int)&x);
}

void loop() {}
```

### Exemplo 2
```cpp
char x, y, z;

void setup(){
  Serial.begin(9600);
  Serial.print("Endereco x: ");
  Serial.println((int)&x);
  Serial.print("Endereco y: ");
  Serial.println((int)&y);
  Serial.print("Endereco z: ");
  Serial.println((int)&z);
}

void loop() {}
```

### Exemplo 3
```cpp
char x, y, z;
char xyz[3] = {'x', 'y', 'z'};

void setup(){
  Serial.begin(9600);
  Serial.print("Endereco xyz: ");
  Serial.println((int)&xyz);
  Serial.print("Endereco x: ");
  Serial.println((int)&x);
  Serial.print("Endereco y: ");
  Serial.println((int)&y);
  Serial.print("Endereco z: ");
  Serial.println((int)&z);
}

void loop() {}
```

### Exemplo 4
```cpp
int x = 1000, y = 2000, z = 3000;
int xyz[3] = {222, 333, 444};
int *pt = &xyz[2];

void setup(){
  Serial.begin(9600);
  Serial.print("Endereco pt: ");
  Serial.println((int)&pt);
  Serial.print("Valor de pt: ");
  Serial.println((int)pt);
  Serial.print("Valor apontado por pt: ");
  Serial.println(*pt);
}

void loop() {}
```

---

Esse conteúdo agora está pronto para ser utilizado como documentação no GitHub!
