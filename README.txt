1. Eliminação de código duplicado
 As funções `createTask` e `updateTask` tinham validações e tratamento de erros repetidos.
 Foram criadas funções auxiliares para reutilizar essa lógica.

2. Função de requisição genérica
Todas as chamadas `fetch` eram parecidas.
 Foi criada a função `apiRequest` para centralizar as requisições e o tratamento de erros.

3. Uso de useCallback
 As funções do hook eram recriadas a cada renderização.
 Foi utilizado `useCallback` para melhorar o desempenho e evitar renderizações desnecessárias.

4. Atualização otimista de estado
 Antes, após cada alteração, a lista era recarregada da API.
 Agora, o estado local é atualizado diretamente, reduzindo requisições e tornando a aplicação mais rápida.

5. Separação de responsabilidades
A comunicação com a API foi organizada em uma função específica (`apiRequest`).
Isso deixa o código mais limpo e fácil de manter.

A refatoração reduziu a repetição de código, melhorou a organização, aumentou a reutilização de funções e otimizou o desempenho da aplicação.
