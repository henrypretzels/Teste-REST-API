# Teste de API REST

Esse é um projeto para fins didáticos, com o intúito de testar uma API REST simples feita em Java com o auxílio do Springboot, que realiza o armazenamento local dos dados.

##  Pré-requisitos
- Java 24.0
- Maven 4.0
- SpringBoot 3.4.5
- (Opcional) Postman/Insomnia para testar endpoints
- Uma IDE para execução, como o IntelliJ

## Como preparar o projeto
1. Clone o repositório:
   ```bash
   git clone https://github.com/henrypretzels/Teste-REST-API.git
   ´´
2. Abra a pasta com o intelliJ
3. Localize o arquivo DemoApplication.java e o execute
4. Abra o Postman, e no campo principal, digite http://localhost:8080/users
5. Na aba de Headers (Cabeçalhos), adicione um novo par Chave-Valor, com a chave sendo Content-Type e o valor sendo application/json
## Como testar os endpoints
1. O endpoint GET, que nesse caso irá retornar todos os usuários presentes, pode ser testado sem alterar a URL, com um retorno funcional o código de status 200 (OK).
2. Para testar o endpoint POST, vá para a aba Body, selecione a opção Raw e insira requisições formatadas igual ao exemplo abaixo antes de clicar no botão Send:
   ```bash
   {
    "name": "Usuário",
    "age": 20
   }
´´
Esse irá retornar o código de status 201 (Created) se funcionar corretamente.

3. Para testar o endpoint PUT, a URL deve ser modificada para  http://localhost:8080/users/n, substituindo n pelo ID do usuário no qual se deseja alterar as informações,
seguindo o mesmo formato de requisição do passo 2. Esse terá como retorno funcional o código de status 200.

4. Para testar o endpoint DELETE, a lógica é similar ao passo 3, desta vez selecionando o ID do usuário no qual se deseja remover. Esse terá como retorno funcional o código de status 204 (No Content).


## Fluxo de execução exemplo:
    Crie 2 usuários via POST

    Liste todos via GET (deve retornar 2 itens)

    Atualize o segundo usuário via PUT

    Delete o segundo usuário via DELETE

    Liste novamente via GET (deve retornar 1 item atualizado)

    Crie um outro usuário (deve retornar um novo usuário sem pular IDs)
