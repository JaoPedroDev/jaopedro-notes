# Node.js

É um runtime de [[../JavaScript]] de código aberto e multi-plataforma, utiliza a engine de JavaScript V8 fora do navegador, permitindo a criação de aplicativos nativos através do JavaScript.

Um aplicativo em Node.js roda em um único processo, sem criar uma nova thread para cada request. O padrão no Node.js são códigos assíncronos, ou seja, códigos que não bloqueiam a execução do programa aguardando certa instrução ser completada.

Quando o Node.js faz uma operação I/O, como ler algo da rede, acessar um banco de dados, etc. ao invés de bloquear o thread desperdiçando ciclos de CPU aguardando a operação acabar, Node.js executará a próxima operação e voltará para operação anterior quando ela der uma resposta.

Isso permite que aplicações em Node.js consigam manusear milhares de conexões simultâneas em um único servidor, sem entrar na área de thread concurrency.

# Relacionado
-  [[../JavaScript Engine]]



