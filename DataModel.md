Para a etapa de **Projeto de Sistema e Software** da plataforma de compra e venda de ingressos, focaremos no modelo de dados completo, que é fundamental para iniciar o desenvolvimento do sistema. Este modelo será representado através de um Diagrama Entidade-Relacionamento (ER), detalhando as entidades principais, seus atributos e os relacionamentos entre elas.

### Modelo de Dados

#### Entidades e Atributos

1. **Tenant**
   - **TenantID** (PK): Identificador único do tenant.
   - **Nome**: Nome do tenant.
   - **InformaçõesDeContato**: Informações de contato do tenant.
   - **ConfiguraçõesEspecíficas**: Configurações específicas do tenant, como preferências de pagamento e notificação.

2. **Usuário**
   - **UserID** (PK): Identificador único do usuário.
   - **TenantID** (FK): Identificador do tenant ao qual o usuário pertence.
   - **Nome**: Nome do usuário.
   - **Email**: E-mail do usuário.

3. **Evento**
   - **EventoID** (PK): Identificador único do evento.
   - **TenantID** (FK): Identificador do tenant ao qual o evento pertence.
   - **NomeDoEvento**: Nome do evento.
   - **Tipo**: Tipo do evento (ex: festa, show, teatro).
   - **Localização**: Localização do evento.
   - **DataEHora**: Data e hora do evento.

4. **Ticket**
   - **TicketID** (PK): Identificador único do ticket.
   - **EventoID** (FK): Identificador do evento associado.
   - **TenantID** (FK): Identificador do tenant ao qual o ticket pertence.
   - **PreçoOriginal**: Preço original do ticket.
   - **IDDoVendedor** (FK): Identificador do usuário que é o vendedor do ticket.
   - **CódigoÚnicoDeVerificação**: Código para verificação da autenticidade do ticket.
   - **Status**: Status do ticket (disponível, reservado, vendido).

5. **Transação**
   - **TransaçãoID** (PK): Identificador único da transação.
   - **TenantID** (FK): Identificador do tenant ao qual a transação pertence.
   - **IDDoComprador** (FK): Identificador do usuário que é o comprador do ticket.
   - **IDDoTicket** (FK): Identificador do ticket associado.
   - **PreçoDeVenda**: Preço de venda do ticket.
   - **DataDaTransação**: Data em que a transação foi realizada.
   - **StatusDaTransação**: Status da transação (pendente, concluída, cancelada).

6. **PreferênciasDeNotificação**
   - **PreferênciasID** (PK): Identificador único das preferências de notificação.
   - **UserID** (FK): Identificador do usuário associado.
   - **ReceberEmails**: Indica se o usuário deseja receber e-mails.

#### Relacionamentos

- **Tenant** ↔ **Usuário**: Um-para-muitos.
- **Usuário** ↔ **Ticket** (como vendedor): Um-para-muitos.
- **Usuário** ↔ **Transação** (como comprador): Um-para-muitos.
- **Evento** ↔ **Ticket**: Um-para-muitos.
- **Ticket** ↔ **Transação**: Um-para-um.
- **Usuário** ↔ **PreferênciasDeNotificação**: Um-para-um.
