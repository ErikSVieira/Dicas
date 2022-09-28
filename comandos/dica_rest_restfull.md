# Diferença entre Rest Restfull

-  A aplicação mais comum de REST é a própria World Wide Web, que utilizou REST como base para o desenvolvimento do protocolo HTTP.

    - **Cliente–servidor:** sua principal característica é separar as responsabilidades de diferentes partes de um sistema (back-end e front-end), permitindo a evolução e a escalabilidade dessas responsabilidades de forma independente.
    - **Stateless:** propõe que cada requisição ao servidor contenha todas as informações necessárias para que ela seja tratada com sucesso pelo servidor.
    - **Cache:** um sistema REST deve permitir que suas respostas sejam passíveis de cache, para oferecer uma melhor performance.
    - **Interface uniforme:** o sistema deve ter uma interface modelada e padronizada, obedecendo importantes padrões, considerando os seguintes elementos: recursos, mensagens autodescritivas e hipermídia.
    - **Sistema em camadas:** um sistema REST deve permitir a escalabilidade necessária para grandes sistemas distribuídos, tendo a capacidade de adicionar elementos intermediários que sejam totalmente transparentes para seus clientes.
    - **Código sob demanda**: seu objetivo é aumentar a flexibilidade dos clientes, sendo essa a única prática opcional dentro das constraints.

- O termo REST se refere ao conjunto de boas práticas denominado constraints, enquanto o termo RESTful se refere à implementação de uma API (application programming interface, ou interface de programação de aplicativos) que segue os princípios definidos dentro do REST.

- Caso a implementação da API não siga os princípios definidos pelo REST, ela será considera uma API HTTP.

- Os formatos mais usados para trafegar entre servidor e cliente são JSON, XML e YAML.

# Status HTTP

- **Informativo (1XX):** a solicitação foi aceita ou o processo continua em andamento.
- **Sucesso (2XX):** a ação foi concluída ou entendida.
- **Redirecionamento (3XX):** algo mais precisa ser feito ou precisou ser feito para completar a solicitação.
- **Erro do cliente (4XX):** a solicitação não pode ser concluída ou contém a sintaxe incorreta.
- **Erro no servidor (5XX):** o servidor falhou ao concluir a solicitação.

# Métodos

- **Safe:** um método HTTP é seguro se ele não altera o estado do servidor.
- **Idempotent:** um método HTTP é idempotente se uma requisição idêntica pode ser feita uma ou mais vezes em sequência com o mesmo efeito enquanto deixa o servidor no mesmo estado.
- **Cacheable:** uma resposta armazenável em cache é uma resposta HTTP que pode ser armazenada em cache para ser recuperada e usada posteriormente, salvando uma nova  olicitação para o servidor.

- GET, POST, HEAD, PUT, DELETE, CONNECT, OPTIONS, TRACE e PATCH.

Método   | Função
--------- | -------------------------------------------------------------------------------
GET | Utilizado para obter um recurso.
POST | Utilizado para criar um recurso.
PUT | Utilizado para atualizar um recurso.
DELETE | Utilizado para apagar um recurso.
PATCH | Utilizado para atualizar partes de um recurso.
HEAD | Utilizado para obter o cabeçalho de uma requisição
OPTIONS | Utilizado para obter os métodos que podem ser utilizados em determinado recurso.
CONNECT | Utilizado para converter uma requisição de conexão para um túnel TCP/IP transparente, geralmente utilizado para facilitar a comunicação criptografada com SLL (HTTPS) por meio de um proxy HTTP não criptografado. 
TRACE | Utilizado para verificar se houve mudanças e adições feitas por servidores intermediários. Observação: por questões de segurança, este método deve ser desabilitado.

