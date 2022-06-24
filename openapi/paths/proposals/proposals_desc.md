## Criar Proposta
Para criar uma proposta você terá que passar parâmetros específicos no **JSON Body**:  

| Parâmetro | Função | Obrigatório? | Observações |
| --------- | ------ | ------------ | ----------- |
| psPaymentMethodId | Tipo de Pagamento de Produto e Serviço (PS) | **Não** | *Sem Observações* |
| mrrPaymentMethodId | Tipo de Pagamento Recorrente (MRR) | **Não** | *Sem Observações* |
| title | Título da Proposta | **Não** | *Sem Observações* |
| description | Descrição da Proposta | **Não** | *Sem Observações* |
| signature | Assinatura da Proposta | **Não** | *Sem Observações* |
| validAt | A partir de que data a proposta será válida | **Não** | *A data precisa estar no formato **ISO 8601**, Exemplo: **2022-06-15T14:40:12-04:00**  É separado em Data "**2022-06-15**" dividido por um "**T**" depois o Tempo é passado "**14:40:12**" e por último o Fuso Horário é passado "**-04:00***"*, existe um site para fazer essa conversão, aqui está a URL: https://dencode.com/en/date/iso8601 |
| totalPrice | Preço total da proposta | **Não** | *O valor deverá ser colocado na forma Americana, Exemplo:```{ "totalPrice": 399.99 } ```* |
| psTermOfFirstInstallment | Termo de Primeira Instalação do Produto e Serviço (PS) da Proposta | **Não** | *Sem Observações* |
| psTermOfInstallments | Termo de Intalação do Produto e Serviço (PS) da Proposta | **Não** | *Sem Observações* |
| psMaxInstallments | Maximo de Instalações do Produte e Serviço (PS) da Proposta | **Não** | *Sem Observações* |
| psTotalPrice | Preço Total do Produto e Serviço (PS) da Proposta | **Não** | *O valor deverá ser colocado na forma Americana, Exemplo:```{ "totalPrice": 399.99 } ```* |
| mrrFirstPayment | Primeiro Pagamento Recorrente (MRR) | **Não** | *O valor deverá ser colocado na forma Americana, Exemplo:```{ "totalPrice": 399.99 } ```* |
| mrrExpirationDay | Data de Expiração do Pagamento Recorrente (MRR) da Proposta | **Não** | *A data precisa estar no formato **ISO 8601**, existe um site para fazer essa conversão, aqui está a URL: https://dencode.com/en/date/iso8601* |
| mrrTotalPrice | Preço Total do Pagamento Recorrent (MRR) da Proposta | **Não** | *Sem Observações* |
| organizationId | ID da sua organização, exemplo: "Dog King é a minha organização de ID 27" | **Não** | *Sem Observações* |
| status | Status da Proposta | **Não** | *O Status é um Enumerator, ou seja, tem valores fixos, no caso do status, o Status pode ser: "ABERTO", "GANHO", "PERDIDO", "CONGELADO" ou "CANCELADO".* |
| contactId | ID do Contato, Exemplo: "Dog King tem o contato de ID 12" | **Não** | *Sem Observações* |
| psFirstPayment | Primeiro Pagamento de Produto e Serviço (PS) da Proposta | **Não** | *Sem Observações* |
| installments | Instalações | **Não** | *Sem Observações* |
| nextContactDate | Próxima data de Contato da Proposta | **Não** | *Sem Observações* |
| goal | Sua Meta | **Não** | *Sem Observações* |
| userId | O ID do seu Usuário, Exemplo: "Meu usuário M1gu3l0001 é o de ID 3" | **Não** | *Sem Observações* |
| followUpType | Tipo de "Acompanhamento" | **Não** | *O followUpType é um Enumerator, ou seja, tem valores fixos, no caso do followUpType, o Tipo pode ser: "Tarefa", "Compromisso" ou "Lembrete".* |
| pipelineId | ID da Pipeline, Exemplo: A Pipeline | **Não** | *Sem Observações* |
| stageId | Id do estágio | **Não** | *Sem Observações* |
| closingForecast | A Previsão de Encerramento da Proposta  | **Não** | *Sem Observações* |
| temperature | A "Temperatura" da Proposta | **Não** | *A temperature é um Enumerator, ou seja, tem valores fixos, no caso da temperature, a temperatura pode ser: "Frio", "Morno", "Quente", "Muito Quente".* |
| probability | A probabilidade da Proposta dar certo | **Não** | *A probability é um Enumerator, ou seja, tem valores fixos, no caso da probability, os valores ficam entre 10% e 100%, Obs: Não existem valores tipo 27% ou 82%, são valores terminados em 0 por exemplo 30%, 60%.* |