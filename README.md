# mackenzie-iot
Descrição e código do projeto da disciplina Objetos Inteligentes Conectados

Descrição:
O Dispositivo está conectado ao Desktop. O Arduino IDE carrega o código para o Microcontrolador executar. Esse dispositivo possui três mecanismos principais. O principal é o Microcontrolador NodeMCU ESP8266, que fornece a voltagem para o sensor e o atuador. O NodeMCU também capta a temperatura do sensor e envia para o display. Depois disso, essa informação também é transmitida como um tópico para a rede wi-fi local que por sua vez a encaminha para um broker público (HiveMQ) via protocolo MQTT. Após essa primeira transmissão, o broker envia essa mensagem para o Desktop através da HiveMQ MQTT WebSocket client. 

Hardware Utilizado:
Microcontrolador NodeMCU ESP8266, Sensor de Temperatura DHT22, Display LCD Oled Module, Protoboard, Resistor 4K7, Jumpers Macho x Macho, Arduino IDE, HiveMQ Broker.

Protocolo Utilizado: MQTT.O ponto central de comunicação é o broker MQTT, responsável por despachar todas as mensagens entre os remetentes e os destinatários legítimos. Cada cliente que publica uma mensagem no Broker inclui um tópico na mensagem. O tópico são as informações de roteamento para o Broker. Cada cliente que deseja receber mensagens assina um determinado tópico e o Broker entrega todas as mensagens com o tópico correspondente ao cliente. 

