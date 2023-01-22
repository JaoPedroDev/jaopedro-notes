# A Internet

A internet começou como um projeto acadêmico em 1969 conhecido como ARPANET, fundado pelo contro militar ""Advanced Research Projects Agency""(ARPA, now DARPA). O projeto foi liderado por Bob Taylor, um administrador da ARPA.

Em 1973, engenheiros de software Vint Cerf e Bob Kahn começaram a trabalhar na nova geração dos padrões para a ARPANET, o TCP/IP, que se tornaram a fundação da internet moderna. Que entrou em vigor em 1 de janeiro de 1983.

## Estrutura da internet

- **A ultima parada** é a parte que conecta casas e pequenas empresas na internet. Operadoras como Vivo, Claro, TIM, etc. oferecem seus serviços conectando os seus clientes a internet utilizando cabos de cobre ou a mais atualizada fibra óptica. Também  são incluídos as torres de internet móvel.

- **Data centers** são salas cheias de servidores que armazenam o conteúdo da internet. Alguns pertencem a grandes empresas como Google e Facebook. Outros são empresas que oferecem seus servidores como serviços para pequenas empresas.

- **The backbone** consistem de cabos que atravessam longas distancias, carregando dados entre data centers e consumidores.

## Endereço de IP
Internet Protocol addresses são sequencias de números que computadores utilizam para identificarem uns aos outros dentro de uma rede. Ex: 192.168.0.0

A Internet Assigned Number Authority é responsável por distribuir endereços de IP para organizações, garantindo que cada uma possua um endereço de IP diferente.

Tipos de endereço IP:
- **IPv4:** É o primeiro padrão criado, consiste de 4 números que podem ir de 0 a 255 cada, possibilitando 4 bilhões de combinações possíveis. Ex: 192.168.0.0
- **IPv6:** Conforme o numero de empresas usando os IPs, foi necessário criar um novo padrão que possibilitasse mais IPs distintos. Com isso foi criado o IPv6, que é composto de 8 grupos de 4 dígitos hexadecimais. Ex: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

## Pacotes
Um pacote é a unidade minima de informação transmitida pela internet. Dividir a informação em pactes pequenos possibilita uma maior eficiência de seu funcionamento.

Um pacote possui duas partes, o cabeçalho(Header) que contem informações sobre seu destino, seu tamanho, entre outras. Após isso vem a informação que de fato foi enviada.

Se houver problemas na transmissão de algum pacote, o mesmo pode ser descartado, e o computador que enviou o pacote possui a responsabilidade de reenviar o pacote.