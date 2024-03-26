O conjunto de casos de uso para a plataforma de compra e venda de ingressos descreve as interações principais que os usuários (compradores, vendedores, e administradores) têm com o sistema. Cada caso de uso detalha um processo específico, fornecendo clareza sobre o funcionamento pretendido da plataforma.

### Casos de Uso Principais

#### 1. Compra de Ingresso
- **Ator Primário:** Comprador
- **Resumo:** O comprador procura eventos, seleciona ingressos e finaliza a compra.
- **Fluxo Principal:**
  1. O comprador acessa a plataforma e navega ou pesquisa eventos.
  2. Seleciona um evento e escolhe um ou mais ingressos disponíveis.
  3. Confirma a seleção e procede para o pagamento.
  4. Insere informações de pagamento e finaliza a compra.
  5. Recebe confirmação da compra por e-mail ou notificação push.

#### 2. Venda de Ingresso
- **Ator Primário:** Vendedor
- **Resumo:** O vendedor lista um ingresso para venda na plataforma.
- **Fluxo Principal:**
  1. O vendedor acessa sua conta e seleciona a opção para vender ingressos.
  2. Insere informações sobre o ingresso, incluindo evento, preço e detalhes do assento.
  3. Submete o ingresso para a plataforma.
  4. Recebe notificação quando o ingresso é vendido.
  5. Recebe o pagamento na sua conta da plataforma.

#### 3. Gerenciamento de Eventos (Administrador)
- **Ator Primário:** Administrador
- **Resumo:** O administrador adiciona, edita ou remove eventos na plataforma.
- **Fluxo Principal:**
  1. O administrador acessa o painel administrativo.
  2. Seleciona a opção para gerenciar eventos.
  3. Adiciona um novo evento ou seleciona um existente para edição ou remoção.
  4. Atualiza as informações do evento conforme necessário.
  5. Salva as alterações, atualizando o catálogo de eventos na plataforma.

#### 4. Autenticação de Ingresso no Evento
- **Ator Primário:** Organizador do Evento
- **Resumo:** O organizador do evento valida ingressos na entrada do evento.
- **Fluxo Principal:**
  1. O organizador usa um dispositivo para escanear o código do ingresso na entrada.
  2. O sistema verifica a autenticidade e o status do ingresso.
  3. O ingresso é marcado como usado, e o portador é admitido no evento.

#### 5. Gestão de Preferências de Notificação
- **Ator Primário:** Usuário (Comprador/Vendedor)
- **Resumo:** Usuários configuram suas preferências de notificação na plataforma.
- **Fluxo Principal:**
  1. O usuário acessa as configurações de conta.
  2. Seleciona preferências de notificação.
  3. Ajusta as configurações para receber notificações por e-mail e/ou push.
  4. Salva as alterações.

#### 6. Reembolso de Ingresso
- **Ator Primário:** Comprador
- **Resumo:** O comprador solicita reembolso para um ingresso comprado.
- **Fluxo Principal:**
  1. O comprador acessa o histórico de compras na plataforma.
  2. Seleciona o ingresso e solicita reembolso.
  3. O sistema verifica as políticas de reembolso do evento.
  4. Se aplicável, o reembolso é processado e o usuário é notificado.