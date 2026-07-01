# Dicionário de Dados - desafio_nps_fase1_processado.csv


## Variáveis
| Campo | Tipo | Descrição |
| :--- | :--- | :--- |
| `customer_id` | INT | Identificador único do clientes. |
| `customer_age` | INT | Idade do cliente. |
| `customer_region` | STR | Região geográfica do cliente. |
| `customer_tenure_months` | INT | Tempor de relacionamento com o cliente com a empresa (em meses). |
| `order_id` | INT | Identificador único do pedido. |
| `order_value` | FLOAT | Valor total do pedido. |
| `items_quantity` | INT | Quantidade de itens no pedido. |
| `discount_value` | FLOAT | Valor do desconto aplicado ao pedido. |
| `payments_installments` | INT | Número de parcelas do pagamento. |
| `delivery_time_days` | INT | Tempo total de entrega (em dias). |
| `delivery_delay_days` | INT | Quantidade de dias de atraso na entrega. |
| `freight_values` | FLOAT | Valor do frete. |
| `delivery_attempts` | INT | Número de tentativas de entrega. |
| `customer_service_contacts` | INT | Número de contatos do cliente com o atendimento. |
| `resolution_time_days` | INT | Tempo para resolução do problema (em dias). |
| `nps_score` | FLOAT | Nota de satisfação do cliente (NPS), variando de 0 a 10, coletada após a experiência de compra. |
| `repeat_purchase_30d` | INT | Indica se houve recompra em até 30 dias após o pedido (0 = não, 1 = sim). |
| `complaints_count` | INT | Número de reclamações registradas pelo cliente. |
| `csat_internal_score` | FLOAT | Score interno de satisfação do cliente. |
| `nps_category` | STR | Classificação NPS: Detrator (0-6.9), Neutro (7-8.9) ou Promotor (9-10). |
| `faixa_atraso` | STR | Agrupamento de delivery_delays_days (ex: 2 dias, 4+ dias) |
| `faixa_reclamacoes` | STR | Agrupamento de complaints_count (ex: 3 reclamações, 6+ reclamações). |
| `faixa_contatos` | STR | Agrupamento de customer_service_contacts (ex: 0 contatos, 3+ contatos). |
| `faixa_resolucao` | STR | Agrupamento de resolution_time_days (ex: 3-5 dias, 8+ dias) |
| `faixa_csat` | STR | Classificação NPS: Baixo (0-3), Médio (3.1-6) , Alto (6.1-8) ou Muito Alto (8.1-10). |
| `faixa_etaria` | STR | Agrupamento do customer_age (ex: Até 25, 46-60 anos). |
| `grupo_risco` | STR | Classificação de risco de detratores (ex: Alto risco, Demais clientes).|