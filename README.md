- **Guilherme Barreto Santos** - RM97674  
- **Nicolas Oliveira da Silva** - RM98939

# 🍷 Winery - Web Service SOAP

Projeto acadêmico de desenvolvimento de Web Services utilizando o protocolo SOAP, com implementação em Java e Maven, dividido em um publicador de serviços e dois clientes consumidores.

## 📦 Estrutura do Projeto

Winery/
│
├── Publisher/
│   └── WinerySys/
│       ├── pom.xml
│       └── src/
│           └── main/
│               ├── java/
│               │   └── br/
│               │       └── com/
│               │           └── fiap/
│               │               └── winery/
│               │                   ├── WineStockService.java
│               │                   ├── WineStockServiceImplementation.java
│               │                   ├── WineWarningService.java
│               │                   ├── WineWarningServiceImplementation.java
│               │                   └── Loader.java
│               └── resources/
│
├── Consumer/
│   ├── WineStockClient/
│   │   ├── pom.xml
│   │   └── src/
│   │       └── main/
│   │           ├── java/
│   │           │   └── br/
│   │           │       └── com/
│   │           │           └── fiap/
│   │           │               └── winery/
│   │           │                   └── ApplicationClient1.java
│   │           └── resources/
│   │
│   └── WineOrderClient/
│       ├── pom.xml
│       └── src/
│           └── main/
│               ├── java/
│               │   └── br/
│               │       └── com/
│               │           └── fiap/
│               │               └── winery/
│               │                   └── ApplicationClient2.java
│               └── resources/

## 🔧 Tecnologias Utilizadas

- Java 17+
- Maven
- Jakarta JAX-WS (jaxws-rt)
- SOAP (Simple Object Access Protocol)

## 📡 Serviços Disponibilizados

1. **WineStockService**
   - `getMenu()`: retorna lista de vinhos disponíveis.
   - `placeOrder(String name, int quantity)`: realiza um pedido.

2. **WineWarningService**
   - `sendWarn()`: retorna um aviso sobre o estoque.

## ▶️ Como Executar

1. Compile e execute o projeto `WinerySys` (Publisher) para publicar os serviços em:
   - `http://localhost:8085/WineStockService?wsdl`
   - `http://localhost:8086/WineWarningService?wsdl`

2. Nos projetos consumidores, configure o `pom.xml` com `jaxws-maven-plugin` e gere os stubs com `wsimport`.

3. Execute as classes `ApplicationClient1` e `ApplicationClient2` para consumir os serviços.
