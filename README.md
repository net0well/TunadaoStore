# TunadãoStore🔥 

## 🚀 Sobre o Projeto

O TunadãoStore é uma aplicação completa de e-commerce desenvolvida do zero utilizando .NET 8 e Angular 18, implementando uma arquitetura robusta com padrões como Repository, Unit of Work e Specification. O projeto conta com um backend construído em ASP.NET Core utilizando Entity Framework Core para acesso a dados, ASP.NET Identity para autenticação e autorização baseada em roles, Redis para persistência do carrinho de compras, SignalR para comunicação em tempo real e integração com Stripe para processamento seguro de pagamentos com suporte a 3D Secure. O frontend foi desenvolvido em Angular 18 com Angular CLI, utilizando Angular Material e Tailwind CSS para uma interface moderna e responsiva, Angular Reactive Forms para formulários reutilizáveis, lazy loading para otimização de performance, além de funcionalidades avançadas como paginação, busca, filtros, ordenação e um sistema completo de gestão de pedidos, demonstrando as melhores práticas de desenvolvimento full-stack moderno.

## 🛠️ Tecnologias Utilizadas

### Backend (.NET 8)
- **ASP.NET Core** - Framework principal
- **Entity Framework Core** - ORM para acesso a dados
- **ASP.NET Identity** - Sistema de autenticação e autorização
- **Redis** - Cache para carrinho de compras
- **SignalR** - Comunicação em tempo real
- **Stripe** - Processamento de pagamentos (3D Secure)

### Frontend (Angular 18)
- **Angular CLI** - Framework principal
- **Angular Material** - Componentes UI
- **Tailwind CSS** - Estilização
- **Angular Reactive Forms** - Formulários reativos
- **Lazy Loading** - Carregamento otimizado de módulos

### Banco de Dados
- **Multiple DbContext** - Contextos separados por domínio
- **SQL Server** - Banco de dados principal

## ✨ Funcionalidades Implementadas (Em construção)

### 🏪 Loja Virtual
- Catálogo de produtos com busca, filtros e ordenação
- Paginação otimizada para grandes volumes de dados
- Carrinho de compras persistente (Redis)
- Sistema de pedidos completo

### 👤 Autenticação e Autorização
- Registro e login de usuários
- Autenticação baseada em roles
- Proteção de rotas e endpoints

### 💳 Pagamentos
- Integração com Stripe
- Suporte a 3D Secure (padrões europeus)
- Processamento seguro de transações

### 🎨 Interface de Usuário
- Design responsivo e moderno
- Componentes reutilizáveis
- Experiência de usuário otimizada
- Feedback em tempo real (SignalR)

## 🏗️ Arquitetura

O projeto implementa padrões de arquitetura robustos:

- **Repository Pattern** - Abstração do acesso a dados
- **Unit of Work Pattern** - Gerenciamento de transações
- **Specification Pattern** - Consultas complexas e reutilizáveis
- **Modular Architecture** - Separação clara de responsabilidades

## 📋 Pré-requisitos

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Node.js](https://nodejs.org/) (versão 18 ou superior)
- [Angular CLI](https://angular.io/cli)
- [Redis](https://redis.io/)
- [SQL Server](https://www.microsoft.com/sql-server) ou [SQL Server LocalDB](https://docs.microsoft.com/sql/database-engine/configure-windows/sql-server-express-localdb)

## 🚀 Como Executar

### 1. Clone o repositório
```bash
git clone https://github.com/net0well/TunadaoStore.git
cd TunadaoStore
```

### 2. Configure o Backend
```bash
# Navegue até o diretório da API
cd API

# Restaure as dependências
dotnet restore

# Configure a string de conexão no appsettings.json
# Configure as chaves do Stripe e Redis

# Execute as migrações
dotnet ef database update

# Execute a aplicação
dotnet run
```

### 3. Configure o Frontend
```bash
# Navegue até o diretório do cliente
cd client

# Instale as dependências
npm install

# Execute a aplicação Angular
ng serve
```

### 4. Acesse a aplicação
- **Frontend**: http://localhost:4200
- **Backend API**: http://localhost:5000
- **Swagger**: http://localhost:5000/swagger

## 🔧 Configuração

### Variáveis de Ambiente
Configure as seguintes variáveis no `appsettings.json`:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "sua-string-de-conexao-sql-server",
    "Redis": "sua-string-de-conexao-redis"
  },
  "StripeSettings": {
    "PublishableKey": "sua-chave-publica-stripe",
    "SecretKey": "sua-chave-secreta-stripe"
  }
}
```

## 📝 Funcionalidades Detalhadas

### Gestão de Produtos
- CRUD completo de produtos
- Upload de imagens
- Categorização
- Controle de estoque

### Carrinho de Compras
- Persistência em Redis
- Atualização em tempo real
- Cálculo automático de totais

### Sistema de Pedidos
- Histórico de compras
- Rastreamento de status
- Integração com pagamentos

### Pagamentos Seguros
- Processamento via Stripe
- Conformidade com PCI DSS
- Suporte a múltiplos métodos de pagamento

## 🤝 Contribuindo

Contribuições são sempre bem-vindas! Sinta-se à vontade para:
- Reportar bugs
- Sugerir novas funcionalidades
- Enviar pull requests
- Melhorar a documentação

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👨‍💻 Autor

**net0well**
- GitHub: [@net0well](https://github.com/net0well)

---

⭐ Se este projeto te ajudou, considere dar uma estrela!

## 🚀 Deploy

O projeto está configurado para deploy no Azure com:
- App Service para a API
- Static Web Apps para o frontend
- Azure SQL Database
- Azure Cache for Redis

Para instruções detalhadas de deploy, consulte a documentação específica na pasta `docs/deployment`.
