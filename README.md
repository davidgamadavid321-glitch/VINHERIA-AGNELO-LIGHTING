<p align="center">
  <img src="vinheria_agnello/imgs/circuit_image.png" width="600" alt="Circuito montado no Tinkercard">
</p>

1. Visão Geral
O sistema monitora continuamente os níveis de luminosidade, garantindo condições ideais de conservação dos vinhos. Utiliza sensor LDR, LEDs indicadores, buzzer e LCD para alertas visuais e sonoros.
2. Funcionalidades
Exibe mensagem inicial com logotipo.
Calibração automática de luz mínima e máxima.
Conversão da leitura do LDR para porcentagem (0–100%) usando map().
LEDs indicativos:
Verde: luz ideal
Amarelo: alerta
Vermelho: luz excessiva + buzzer por 3 segundos
Exibição contínua da porcentagem no LCD.
3. Componentes
Componente	Quantidade	Função
Arduino Uno	1	Microcontrolador
Sensor LDR	1	Medir luz
LCD 16x2	1	Exibição
LEDs (verde, amarelo, vermelho)	3	Indicação visual
Buzzer	1	Alerta sonoro
Resistores 220Ω/10kΩ	4	Limitação de corrente/divisor de tensão
Protoboard e Jumpers	Diversos	Conexões
4. Estrutura do Projeto
VINHERIA_AGNELLO/
├── vinheria_auto.ino
├── imgs/
│   └── circuit_image.png
├── README.md
5. Montagem e Uso
Monte o circuito conforme circuito_auto.png.
Abra vinheria_auto.ino na Arduino IDE e carregue no Arduino.
Calibração:
Cubra o sensor → luz mínima
Ilumine o sensor → luz máxima
Após calibração, o sistema exibe continuamente a porcentagem de luz e aciona alertas quando necessário.
6. Detalhes Técnicos
map() converte leituras analógicas (0–1023) em porcentagem.
millis() gerencia temporizações sem bloquear o código.
tone() / noTone() controlam o buzzer.
Média de 5 leituras reduz ruído do sensor.
7. Requisitos de Software
Arduino IDE ≥ 1.8
Biblioteca LiquidCrystal.h
Simulação recomendada: Wokwi / Tinkercad Circuits
8. Equipe
Nome	Função
Pedro Viana	Desenvolvimento
Pedro Salles	Desenvolvimento
David Gama	Desenvolvimento