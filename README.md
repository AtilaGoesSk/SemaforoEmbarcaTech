Programa de Controle de Semáforo com LEDs
Este programa em C foi desenvolvido para o Raspberry Pi Pico e controla um semáforo com três LEDs (vermelho, amarelo e verde). O semáforo alterna entre os estados de "Parar", "Atenção" e "Seguir" em intervalos definidos, simulando o funcionamento de um semáforo real.

Funcionalidades
Controle de LEDs: O programa alterna entre os LEDs vermelho, amarelo e verde para simular o ciclo de um semáforo.
Temporização: O semáforo troca de sinal a cada 3 segundos, utilizando um temporizador repetitivo para controlar a troca dos sinais.
Saída Serial: Mensagens sobre o estado atual do semáforo são enviadas para o terminal via serial.
Materiais Necessários
Raspberry Pi Pico ou placa compatível.
3 LEDs (vermelho, amarelo e verde).
3 resistores (para os LEDs).
Fios para conexão.
Esquema de Conexão
LEDs:
O LED verde está conectado ao pino GPIO 11.
O LED amarelo está conectado ao pino GPIO 12.
O LED vermelho está conectado ao pino GPIO 13.
Como Utilizar
Compilar o Código:

Certifique-se de ter o toolchain do Raspberry Pi Pico configurado.
Compile o código com o seguinte comando:
bash
Copiar
Editar
make
Carregar no Raspberry Pi Pico:

Conecte o Raspberry Pi Pico ao seu computador enquanto mantém pressionado o botão BOOTSEL.
O dispositivo aparecerá como uma unidade de armazenamento.
Copie o arquivo .uf2 gerado para o Raspberry Pi Pico.
Execução:

Após carregar o programa, o Raspberry Pi Pico será reiniciado automaticamente.
O semáforo começará com o LED vermelho aceso e irá alternar entre os LEDs a cada 3 segundos. As mensagens sobre o estado do semáforo serão exibidas no terminal.
Explicação do Código
GPIOs: O código usa os pinos GPIO 11, 12 e 13 para controlar os LEDs do semáforo.
Temporização: A função add_repeating_timer_ms() é usada para criar um temporizador repetitivo que alterna os sinais a cada 3 segundos.
Saída Serial: O estado do semáforo (vermelho, amarelo, verde) é enviado para o terminal com a função printf(), informando o status atual do semáforo.
Ciclo de sinais: O estado do semáforo alterna entre 3 estados:
Vermelho (parar)
Amarelo (atenção)
Verde (seguir)
