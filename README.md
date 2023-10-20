# Teste Caixa Branca
## Conexão com Banco de Dados Hipotético - Exemplo Java

Este repositório contém um exemplo de código que demonstra como se conectar a um banco de dados hipotético utilizando Java. O código inclui uma classe chamada User com os seguintes métodos e variáveis:

### Funcionalidades
conectarBD(): Este método estabelece uma conexão com um banco de dados MySQL e retorna a conexão.

verificarUsuario(String login, String senha): Este método verifica as credenciais do usuário no banco de dados e armazena o resultado em uma variável booleana chamada result e o nome do usuário em uma variável chamada nome.

**Avaliação do Código**
Aqui está uma análise dos principais aspectos do código:

**Documentação**
O código atual não possui documentação, o que pode dificultar sua compreensão. Recomendamos adicionar comentários explicativos em cada método e classe para melhorar a documentação e ajudar outros desenvolvedores a entender o funcionamento do código.

**Nomenclatura de Variáveis**
A maioria das variáveis possui nomes razoáveis, mas pode ser benéfico torná-los mais descritivos. Por exemplo, em vez de nome e result, você poderia usar nomeUsuario e resultadoVerificacao para tornar o código mais legível.

**Legibilidade e Organização**
Melhorar a formatação do código é importante para torná-lo mais legível. Certifique-se de usar espaços em branco e recuo adequados para facilitar a leitura do código. Além disso, organize o código em seções ou blocos lógicos para tornar a estrutura mais clara.

**Tratamento de Exceções**
O código atual não lida adequadamente com exceções ou verifica valores nulos. É essencial adicionar tratamento de exceções para evitar erros não tratados que podem ocorrer durante a execução.

**Arquitetura**
A arquitetura do código não está claramente definida neste exemplo isolado. Recomendamos criar uma estrutura organizada para o projeto, separando as camadas de conexão com o banco de dados, lógica de negócios e interface do usuário, se aplicável.

**Fechamento de Conexões**
Uma prática recomendada é garantir que as conexões com o banco de dados sejam fechadas corretamente após o uso para evitar vazamentos de recursos. Certifique-se de fechar as conexões, instruções e resultados quando não forem mais necessários.

Este repositório é um exemplo simples e pode ser expandido e aprimorado de acordo com as necessidades do projeto. Certifique-se de seguir boas práticas de desenvolvimento de software e documentação para criar um código robusto e fácil de manter.


![diagrama](https://github.com/MathJorge23/Teste-Caixa-Branca/assets/108235675/6b19a3b1-ec25-4006-a195-65626afb3d9f)

# Complexidade Ciclomática.

M = 8 - 7 + 2*1 M = 1 + 2 M = 3


# Autenticação de Usuário e Conexão com Banco de Dados

Este repositório contém uma classe Java chamada "User" que permite autenticar usuários e estabelecer uma conexão com um banco de dados MySQL.

## Classe User

A classe `User` oferece as seguintes funcionalidades:

- `conectarBD()`: Método para estabelecer uma conexão com o banco de dados MySQL.

- `verificarUsuario(String login, String senha)`: Método para verificar as credenciais de login de um usuário no banco de dados.

- `nome`: Uma variável de instância que armazena o nome do usuário.

- `result`: Uma variável de instância que armazena o resultado da autenticação (verdadeiro se autenticado, falso caso contrário).

## Uso

Você pode utilizar a classe `User` para conectar-se a um banco de dados MySQL e verificar as credenciais do usuário. Abaixo está um exemplo básico de como usar a classe `User`:

```java
User user = new User();
String login = "user123";
String senha = "senha123";

// Verificar as credenciais do usuário
boolean autenticado = user.verificarUsuario(login, senha);

if (autenticado) {
    System.out.println("Usuário autenticado com sucesso. Bem-vindo, " + user.nome);
} else {
    System.out.println("Falha na autenticação. Credenciais inválidas.");
}
