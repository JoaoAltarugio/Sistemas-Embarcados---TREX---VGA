# Sistemas-Embarcados---TREX---VGA

Chrome Dino Game (FPGA Version)
Um clássico jogo de dinossauro para hardware FPGA.

Como Jogar
Inicie o Jogo: Assim que o programa for carregado no seu FPGA, a tela de introdução aparecerá. Pressione a KEY1 no seu kit DE1-SoC (ou hardware equivalente) para começar a partida.

Pular: Para fazer o dinossauro pular e desviar dos obstáculos (cactos e pássaros), pressione a KEY0.

Objetivo: Sobreviva o máximo que puder para conseguir a maior pontuação.

Game Over: Se o dinossauro colidir com um obstáculo, o jogo termina. Pressione a KEY1 novamente para reiniciar.

Como Rodar o Código
Este projeto é desenvolvido em C para ser executado em um sistema embarcado baseado em FPGA (especificamente, kits como o DE1-SoC ou similares que possuem um processador ARM e hardware de vídeo configurável).

Pré-requisitos:

Kit FPGA: Um kit de desenvolvimento FPGA com um processador ARM (como o ARM Cortex-A9 no DE1-SoC) e periféricos de vídeo (buffer de pixels, buffer de caracteres).

Ambiente de Desenvolvimento:

Intel Quartus Prime (ou equivalente para seu FPGA).

Intel FPGA Monitor Program.

address_map_arm.h: Este arquivo (não incluído aqui, mas essencial para o projeto) deve conter as definições de endereço de memória para os periféricos do FPGA, como PIXEL_BUF_CTRL_BASE, RGB_RESAMPLER_BASE, KEY_BASE, e FPGA_CHAR_BASE.

Passos para Compilação e Execução:

Configuração do Projeto FPGA:

Garanta que seu projeto Quartus (ou equivalente) esteja configurado com um sistema de hardware que inclua um processador ARM (HPS), controlador de buffer de pixels, controlador de buffer de caracteres e uma interface de leitura de botões (KEYs) mapeados para os endereços usados no código (address_map_arm.h).

Compilação do Código C:


Crie um novo projeto C/C++ e inclua todos os arquivos .c  necessários (especialmente este arquivo C e address_map_arm.h).

Configure o compilador para o seu alvo ARM (por exemplo, arm-none-eabi-gcc).

Compile o código-fonte. Isso gerará um arquivo executável (geralmente .axf ou .elf).

Carregar e Executar no FPGA:

Conecte seu kit FPGA ao computador.

Use o debugger (ou sua ferramenta preferida) para carregar o arquivo executável compilado para o processador ARM do seu FPGA.

Inicie a execução. O jogo deve aparecer na tela conectada ao seu FPGA.
