# IOT-Floodian

1. Protótipo Funcional
---1.1. Descrição do Protótipo
O protótipo da solução Floodian tem como objetivo monitorar o nível de água em bueiros urbanos, prevendo possíveis alagamentos em situações de emergência. Ele utiliza um sensor ultrassônico (HC-SR04) para medir a distância, um ESP32 como dispositivo central, que coleta os dados do sensor e os envia para um broker MQTT público (test.mosquitto.org). O sistema também utiliza LEDs e um motor para indicar visualmente e fisicamente o nível de água (baixo, médio ou alto).

Sensor ultrassônico: Mede o nível de água em tempo real.

ESP32: Conecta-se à rede Wi-Fi e envia os dados via MQTT.

LEDs: Indicadores visuais para diferentes níveis de água.

Motor: Ativa-se para ações como bombeamento de água ou controle de válvulas.

MQTT: Protocolo de comunicação utilizado para enviar os dados para o Node-RED.

---1.2. Funcionalidade Operacional
O sensor ultrassônico mede a distância entre a água e o sensor.

O ESP32 se conecta à rede Wi-Fi e ao broker MQTT.

Com base na leitura do sensor, o ESP32 publica um JSON com os dados (nível de água e risco) no tópico floodian/sensor01.

LEDs são acionados conforme o nível de água (baixo, médio, alto) para indicar visualmente o estado do sistema.

O motor é ativado de acordo com o nível de água (ligado para níveis baixos, desligado para níveis médios e altos).

---1.3. Teste e Validação do Protótipo
Simulação no Wokwi: O protótipo foi simulado utilizando o Wokwi, uma plataforma de prototipagem IoT, onde o código foi testado e validado com os sensores e atuadores conectados.

Testes em Hardware Real: O código foi transferido para um ESP32 real, e os sensores e atuadores (LEDs e motor) foram testados para garantir a precisão das medições e a funcionalidade dos controles.

---1.4. Aplicação Prática
Esse sistema pode ser integrado a um monitoramento de bueiros em áreas urbanas para detectar o acúmulo de água e prevenir inundações. Em um cenário real, o sistema pode ser utilizado para:

Ativar bombas para retirar a água dos bueiros.

Acionar válvulas de drenagem automáticas para evitar o transbordamento.

Enviar alertas para a administração pública e serviços de emergência.

2. Documentação
---2.1. Descrição Completa da Solução
A solução Floodian utiliza a tecnologia IoT para monitorar e gerenciar o nível de água em bueiros urbanos, com o objetivo de evitar alagamentos. O sistema foi projetado com sensores ultrassônicos para detectar níveis de água, e os dados coletados são enviados a um broker MQTT. O fluxo de dados é integrado ao Node-RED, que exibe as informações de forma visual através de um dashboard. A solução é composta por:

Sensores ultrassônicos: Medem o nível de água.

ESP32: Conecta-se à rede Wi-Fi e ao broker MQTT.

LEDs: Indicadores de nível (baixo, médio e alto).

Motor: Controla bombas ou válvulas de drenagem.

Node-RED: Plataforma para exibir dados em tempo real e fornecer visualizações interativas.

--- 2.2. Imagens e Ilustrações
Aqui estão algumas imagens que ilustram a solução:

![image](https://github.com/user-attachments/assets/6d6464ee-470e-492c-8781-febef1b2e95e)

![image](https://github.com/user-attachments/assets/4c4c96eb-3b8b-4d1a-98f4-c5c3da3599ff)

![image](https://github.com/user-attachments/assets/2bf813f1-bdf3-413a-81cf-4616cca9bc73)


Diagrama do Sistema:

Um diagrama mostrando a conexão entre os sensores, ESP32, MQTT, Node-RED, LEDs e motor.

Dashboard do Node-RED:

Imagem do painel de controle (dashboard) do Node-RED que exibe os níveis de água em tempo real, com gráficos e indicadores de risco.
