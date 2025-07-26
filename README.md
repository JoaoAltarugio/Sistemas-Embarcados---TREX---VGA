# 🦖 Sistemas Embarcados — T-Rex VGA Game
Projeto Final do Curso Sistemas Embarcados

Departamento de Computação - UFSCar

Professor Dr. Emerson Carlos Pedrino


### Chrome Dino Game (Versão FPGA)  
Um clássico jogo de dinossauro adaptado para hardware FPGA.

---

## 🎮 Como Jogar

- **Inicie o Jogo:**  
  Após carregar o programa no FPGA, a tela de introdução aparecerá. Pressione a `KEY1` no kit DE1-SoC (ou hardware equivalente) para começar.

- **Pular:**  
  Pressione `KEY0` para fazer o dinossauro pular e desviar de obstáculos (cactos e pássaros).

- **Objetivo:**  
  Sobreviva o máximo possível para alcançar a maior pontuação.

- **Game Over:**  
  Se o dinossauro colidir com um obstáculo, o jogo termina. Pressione `KEY1` para reiniciar.

---

## 🛠️ Como Rodar o Código

Este projeto é escrito em **C** para sistemas embarcados baseados em **FPGA**, como o kit **DE1-SoC**, que integra um **processador ARM** e controladores de vídeo.

### ✅ Pré-requisitos

- **Hardware:**
  - Kit FPGA com processador ARM (ex: ARM Cortex-A9 no DE1-SoC)
  - Periféricos de vídeo (buffer de pixels e buffer de caracteres)

- **Software:**
  - [Intel Quartus Prime](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html)
  - [Intel FPGA Monitor Program](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/hls-debugger.html)

- **Arquivo necessário:**
  - `address_map_arm.h` (não incluído)  
    Define os endereços dos periféricos:  
    `PIXEL_BUF_CTRL_BASE`, `RGB_RESAMPLER_BASE`, `KEY_BASE`, `FPGA_CHAR_BASE`.

---

## ⚙️ Passos para Compilação e Execução

### 1. Configurar o Projeto FPGA

- Certifique-se de que seu projeto Quartus contenha:
  - Processador ARM (HPS)
  - Controlador de buffer de pixels
  - Controlador de buffer de caracteres
  - Interface de leitura de botões (KEYs)  
    mapeados conforme definido em `address_map_arm.h`.

### 2. Compilar o Código C

- Crie um novo projeto C/C++
- Inclua:
  - Arquivos `.c`
  - `address_map_arm.h`
- Configure o compilador (ex: `arm-none-eabi-gcc`)
- Compile e gere o executável (`.axf`, `.elf`, etc)

### 3. Carregar e Executar no FPGA

- Conecte o FPGA ao seu computador via USB
- Use um debugger ou monitor para:
  - Carregar o executável no ARM
  - Iniciar a execução
- A tela conectada ao FPGA exibirá o jogo

---

##  Demonstração do Jogo
Clique e assista ao vídeo!

[![Assista ao vídeo](https://img.youtube.com/vi/HuWzXzB60Ag/0.jpg)](https://youtu.be/HuWzXzB60Ag)


## 📄 Licença

Distribuído para fins educacionais no contexto da disciplina **Sistemas Embarcados**.

---
