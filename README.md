
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
