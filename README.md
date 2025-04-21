# CsharpMarketSys: Sistema Completo de Gerenciamento Comercial

![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Windows Forms](https://img.shields.io/badge/Windows%20Forms-045FD9?style=for-the-badge&logo=microsoft&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)

## 📖 Descrição do Projeto

O **CsharpMarketSys** é uma solução robusta de gerenciamento comercial, desenvolvida em **C#** com a interface **Windows Forms**, projetada para otimizar as operações de **pequenos e médios negócios**. O sistema oferece um conjunto abrangente de ferramentas para controle de **vendas**, **estoque**, **emissão de notas fiscais**, **cadastro de usuários e clientes**, além de **relatórios financeiros detalhados**.

Construído sobre uma base de dados **SQL Server**, o CsharpMarketSys garante segurança e eficiência no armazenamento de informações. Integrações estratégicas com **APIs externas**, como a **API do Gmail** para comunicação automatizada e bibliotecas como **QRCoder** e **ClosedXML**, enriquecem suas funcionalidades, permitindo, por exemplo, o envio de notas fiscais por e-mail e a exportação de dados para planilhas Excel.

## ✨ Funcionalidades Principais

O sistema CsharpMarketSys abrange as seguintes áreas chave:

-   🛒 **Gerenciamento de Vendas:**
    * Adição rápida e intuitiva de produtos ao carrinho.
    * Aplicação de descontos em tempo real.
    * Emissão de notas fiscais em formato **XML**, pronta para integração com sistemas contábeis.
    * Suporte a múltiplos métodos de pagamento: **Dinheiro**, **Débito**, **Crédito** e **Pix**.

-   📦 **Controle de Estoque:**
    * Funcionalidades completas de cadastro, edição e exclusão de produtos.
    * Atualização automática do inventário após cada venda.
    * Interface amigável para consulta e gestão de produtos.

-   👥 **Cadastro de Usuários e Funcionários:**
    * Cadastro detalhado de clientes e funcionários, incluindo informações pessoais e profissionais.
    * Funcionalidade de upload de fotos para perfis de funcionários.
    * Gestão completa de dados de funcionários (cargo, salário, contato, etc.).

-   📊 **Relatórios e Faturamento:**
    * Geração de relatórios financeiros abrangentes baseados nas vendas realizadas.
    * Exportação de dados financeiros para **Excel** (.xlsx) através da biblioteca ClosedXML.
    * Visualização direta de lucros e métricas comerciais essenciais no sistema.

-   🔌 **Integração com APIs e Serviços Externos:**
    * Envio automatizado de notas fiscais e outras comunicações por e-mail via **Google Gmail API**.
    * Geração dinâmica de **QR Codes** para facilitar pagamentos via Pix, utilizando a biblioteca QRCoder.

## 🛠️ Tecnologias Utilizadas

Este projeto foi desenvolvido com as seguintes tecnologias:

-   **Linguagem e Frameworks:**
    * **C#**: A linguagem principal do sistema.
    * **Windows Forms**: Para a construção da interface gráfica do usuário.
    * **.NET Framework**: A plataforma subjacente que suporta o desenvolvimento.

-   **Banco de Dados:**
    * **SQL Server**: Sistema de gerenciamento de banco de dados relacional.

-   **Bibliotecas e APIs:**
    * **Google Gmail API**: Para serviços de e-mail.
    * **QRCoder**: Para a geração de QR Codes.
    * **ClosedXML**: Para manipulação e exportação de arquivos Excel (.xlsx).
    * **MimeKit**: Para composição e envio de mensagens de e-mail.

## 📁 Estrutura do Projeto

Uma visão geral da estrutura de diretórios e arquivos principais do projeto:

.
├── Pagamentos/          # Formulários e lógica para diferentes métodos de pagamento

├── UsuaryControl/       # Formulários para cadastro, login e gestão de usuários/funcionários

├── RH/                  # Funcionalidades relacionadas a Recursos Humanos

├── FINAL V2/            # Diretório principal contendo a lógica de negócio e UI

│   ├── Vendas.cs        # Gerenciamento do fluxo de vendas, NFs e produtos

│   ├── Pix.cs           # Implementação do método de pagamento Pix

│   ├── Débito.cs        # Implementação do método de pagamento Débito

│   ├── Crédito.cs       # Implementação do método de pagamento Crédito

│   ├── Dinheiro.cs      # Implementação do método de pagamento Dinheiro

│   ├── Faturamento.cs   # Geração de relatórios financeiros e exportação

│   ├── Função.cs        # Métodos utilitários, incluindo configuração de conexão com DB

│   └── ...              # Outros formulários e arquivos do projeto

└── ...                  # Outros arquivos de configuração e projeto (.csproj, etc.)

## ⚙️ Configuração do Ambiente

Para configurar e executar o projeto em sua máquina local, siga os passos abaixo:

### Pré-requisitos

* **Visual Studio**: Com a workload de "Desenvolvimento para desktop com .NET".
* **SQL Server**: Uma instância do SQL Server instalada e acessível.
* **.NET Framework**: Versão compatível com a utilizada no desenvolvimento do projeto.

### Passos para Configuração

1.  Clone o repositório para o seu ambiente local:
    ```bash
    git clone <URL_DO_SEU_REPOSITORIO>
    ```
2.  Abra o projeto no **Visual Studio**.
3.  Configure a string de conexão com o banco de dados SQL Server. Edite o arquivo `Função.cs` e atualize a propriedade `ConnectionString` com suas credenciais:
    ```csharp
    // Exemplo de configuração da string de conexão em Função.cs
    // Certifique-se de usar suas próprias credenciais e nome do servidor/instância.
    cn.ConnectionString = "Data Source=SEU_SERVIDOR_OU_INSTANCIA;Initial Catalog=SistemaYiG;User ID=SEU_USUARIO_SQL;Password=SUA_SENHA_SQL";
    ```
    *Substitua `SEU_SERVIDOR_OU_INSTANCIA`, `SEU_USUARIO_SQL` e `SUA_SENHA_SQL` pelos seus dados.*
4.  Restaure o banco de dados no seu SQL Server utilizando o script de criação (caso exista no repositório) ou restaure um backup se disponível.
5.  Compile o projeto no Visual Studio (`Ctrl + Shift + B`).
6.  Execute o projeto (`F5`).

## 🚀 Uso do Sistema

Após a configuração e execução, o fluxo básico de uso do sistema é o seguinte:

1.  **Login**: Acesse o sistema utilizando suas credenciais de usuário cadastradas.
2.  **Cadastro de Produtos**: Utilize o módulo de estoque para adicionar, editar ou remover produtos do inventário.
3.  **Realização de Vendas**: No módulo de vendas, selecione os produtos, aplique descontos (se necessário) e processe o pagamento, emitindo a nota fiscal correspondente.
4.  **Relatórios**: Acesse o módulo de faturamento para gerar relatórios financeiros e exportar dados para análise.

## 🤝 Contribuição

Contribuições são muito bem-vindas para aprimorar este projeto! Se você deseja contribuir, por favor, siga estes passos:

1.  Faça um fork deste repositório.
2.  Crie uma branch para a sua contribuição: `git checkout -b minha-feature-ou-correcao`.
3.  Faça as alterações desejadas e adicione os commits (`git commit -m 'Adiciona minha feature'`). Certifique-se de que suas mudanças seguem as boas práticas de código.
4.  Envie suas alterações para o seu fork no GitHub: `git push origin minha-feature-ou-correcao`.
5.  Abra um Pull Request (PR) para o branch `main` (ou a branch de desenvolvimento principal) deste repositório, descrevendo suas alterações.

## 📧 Contato

Este projeto foi desenvolvido por:

**Yuri, Isaque e Gustavo**
* **E-mail:** yuribernardo@gmail.com
* **Localização:** Curitiba, Brasil

## 📜 Licença

Este projeto está licenciado sob a **Licença MIT**. Você é livre para usar, copiar, modificar, mesclar, publicar, distribuir, sublicenciar e/ou vender cópias deste software, desde que a notificação de direitos autorais e a permissão estejam incluídas em todas as cópias ou partes substanciais do Software. Veja o arquivo `LICENSE` (se aplicável) no repositório ou a descrição completa da licença MIT para mais detalhes.

