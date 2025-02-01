# 3 LEDs Alarm Button Embarcatech

Este projeto implementa uma simulação de um sistema com **3 LEDs** e um **botão**, com o objetivo de alternar entre os LEDs. Quando o botão é pressionado, os três LEDs são acionados e cada LED é apagado, um por um, a cada 3 segundos, utilizando temporização por hardware ( função: add_alarm_in_ms() ).

## Funcionalidades

- Simulação de **3 LEDs** que alternam entre acender e apagar.
- O sistema começa com todos os LEDs acesos por 3 segundos quando o **botão** é pressionado.
- A cada 3 segundos um LED é apagado até que todos os LEDs estejam apagados.
- O comportamento é controlado por **temporização por hardware add_alarm_in_ms()**.
- Simulação do sistema utilizando o **Wokwi** ou rodando diretamente no **kit BitDogLab (RP2040)**.

## Tecnologias Utilizadas

- **Microcontrolador**: Raspberry Pi Pico 2040.
- **Kit BitDogLab**
- **Linguagem de Programação**: C (usando o **Pico SDK**).
- **Ambiente de Desenvolvimento**: Visual Studio Code (VSCode) com Pico SDK.
- **Simulador**: [Wokwi](https://wokwi.com/), uma plataforma online para simulação de circuitos e microcontroladores.

## Instalação

### Requisitos

- **Visual Studio Code** (VSCode) instalado.
- **Pico SDK** configurado no seu ambiente de desenvolvimento.
- **CMake** instalado.
- **Wokwi** para simulação (opcional).

### Passos para Configuração

1. **Instale o Visual Studio Code**:
   - Baixe o VSCode em: [https://code.visualstudio.com/](https://code.visualstudio.com/).
   
2. **Instale o Pico SDK**:
   - Siga o guia de instalação do Pico SDK em: [https://datasheets.raspberrypi.org/pico/getting-started-with-pico.pdf](https://datasheets.raspberrypi.org/pico/getting-started-with-pico.pdf).

3. **Clone o repositório**:
   - Abra o terminal e execute:
     ```bash
     git clone https://github.com/pedropalmarella/3_leds_alarm_btn_Embarcatech.git
     ```

4. **Abra o projeto no VSCode**:
   - Abra a pasta do projeto no VSCode.

5. **Configure o ambiente de desenvolvimento**:
   - Instale as dependências e ferramentas recomendadas, como o **CMake**.

6. **Compilando o código**:
   - Abra o terminal integrado do VSCode e execute:
     ```bash
     mkdir build
     cd build
     cmake ..
     make
     ```

7. **Carregue o código no Raspberry Pi Pico**:
   - Conecte o Raspberry Pi Pico ao computador.
   - Coloque o Pico no modo de bootloader e copie o arquivo compilado `.uf2` para o dispositivo.

### Usando o Simulador Wokwi (Opcional)

1. Acesse o site [Wokwi](https://wokwi.com/).
2. Crie um novo projeto e escolha a opção para simular o Raspberry Pi Pico.
3. Importe o código do seu projeto para o simulador.
4. Inicie a simulação e veja o funcionamento do sistema com os 3 LEDs e o botão.

## Como Usar

1. Compile o projeto utilizando o VSCode.
2. Carregue o código no Raspberry Pi Pico ou use o simulador Wokwi para testar.
3. Ao pressionar o **botão**, os **3 LEDs** serão acionados e permanecerão acesos por 3 segundos.
4. Após os 3 segundos, o sistema começará a apagar um LED a cada 3 segundos, até que todos os LEDs estejam apagados.
