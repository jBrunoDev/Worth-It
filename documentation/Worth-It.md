
![Worth-It_ See the real cost.png](Worth-It.assets/01a0f81f-5b09-7132-8801-a9a9385d0b76.png)

.
# Documentação do Sistema — Worth-It

| Item | Detalhe |
|---|---|
| **Versão** | 1.0 |
| **Status** | Planejamento e especificação |
| **Plataforma** | Mobile |
| **Mercado inicial** | Brasil |
| **Idioma inicial** | Português do Brasil (PT-BR) |

---

## Sumário

1. Introdução
2. Visão Geral do Sistema
3. Problema e Justificativa
4. Planejamento Estratégico em ADS
5. Público-Alvo
6. Objetivos
7. Escopo do Projeto
8. Levantamento das Necessidades
9. Definição das Soluções de TI
10. Priorização do Projeto
11. Requisitos Funcionais
12. Requisitos Não Funcionais
13. Regras de Negócio
14. Casos de Uso
15. Fluxos do Sistema
16. Arquitetura do Sistema
17. Modelagem do Banco de Dados
18. API e Endpoints
19. Autenticação e Contas
20. Cadastro e Identificação de Produtos
21. Sistema Tributário
22. Sistema de Horas de Trabalho
23. Wishlists
24. Sistema de Decisão de Compra
25. Purchase Score
26. Período Anti-Impulso
27. Inteligência Artificial
28. Histórico e Estatísticas
29. Comparação de Preços
30. Investimentos
31. Notificações
32. Segurança, Privacidade e LGPD
33. Tratamento de Erros
34. Testes
35. Deploy e Ambientes
36. Logs e Monitoramento
37. Limitações
38. Roadmap
39. Diagramas UML
40. Glossário

---

## 1. Introdução

O **Worth-It** é um aplicativo mobile voltado à **educação financeira**, **compreensão de impostos** e **apoio à tomada de decisões de compra**.

A proposta do sistema é permitir que o usuário enxergue uma compra além de seu preço monetário. Ao analisar um produto, o Worth-It poderá mostrar informações como:

- o valor estimado de impostos;
- a quantidade de horas de trabalho necessárias para adquiri-lo;
- a comparação de preços;
- uma análise sobre a necessidade da compra.

O aplicativo também introduz um período de reflexão antes da decisão final, denominado **período anti-impulso**, calculado a partir das características da compra e de um **Purchase Score**.

> O Worth-It **não** tem como objetivo decidir pelo usuário se determinado produto deve ou não ser comprado. O sistema apresenta informações, análises e recomendações para auxiliar o usuário a tomar **sua própria decisão**.

---

## 2. Visão Geral do Sistema

O Worth-It será inicialmente desenvolvido **exclusivamente para o mercado brasileiro** e terá como plataforma principal **dispositivos móveis**.

O aplicativo permitirá que o usuário informe um produto manualmente ou utilize uma fotografia de uma etiqueta para identificar informações como nome, preço e categoria.

A partir dessas informações, o sistema poderá calcular:

- impostos estimados;
- valor estimado do produto sem tributos;
- horas de trabalho equivalentes;
- Purchase Score;
- período recomendado de reflexão;
- comparação com outros preços encontrados;
- histórico de decisões;
- evolução do poder de compra do usuário.

O sistema também permitirá a criação de **múltiplas wishlists** e o acompanhamento das decisões relacionadas aos produtos.

---

## 3. Problema e Justificativa

Ao realizar uma compra, normalmente o consumidor visualiza apenas o **preço final** do produto.

Um produto de R$ 1.000,00, por exemplo, representa mais do que simplesmente R$ 1.000,00. Esse valor pode representar determinada quantidade de **horas de trabalho** e conter uma parcela significativa de **tributos**.

Além disso, compras podem ocorrer **por impulso**, sem que fatores como necessidade, frequência de uso e impacto financeiro sejam considerados.

O Worth-It busca solucionar esse problema transformando o preço em informações mais compreensíveis.

**Em vez de apresentar apenas:**

```
R$ 1.000,00
```

**o sistema poderá apresentar:**

```
R$ 1.000,00
Equivalente a aproximadamente 20 horas do seu trabalho.
Aproximadamente R$ 310,00 correspondem a tributos estimados.
Purchase Score: 72/100.
Período recomendado de reflexão: 3 dias.
```

Dessa maneira, o usuário recebe mais contexto antes de realizar sua escolha.

---

## 4. Planejamento Estratégico em ADS

O planejamento estratégico do Worth-It organiza o desenvolvimento do sistema a partir do problema identificado, das necessidades dos usuários e das tecnologias necessárias para construir a solução.

### 4.1 Missão

Desenvolver uma aplicação que ajude consumidores brasileiros a compreender o impacto financeiro de suas compras por meio de informações **simples, acessíveis e contextualizadas**.

### 4.2 Visão

Transformar o Worth-It em uma ferramenta de apoio à **educação financeira** e ao **consumo consciente**.

### 4.3 Proposta de valor

A proposta de valor está baseada em quatro perguntas principais:

| Pergunta | Resposta do sistema |
|---|---|
| **Quanto estou realmente pagando?** | Apresenta uma estimativa dos impostos presentes no preço. |
| **Quanto tempo trabalhei por isso?** | Converte o preço em horas de trabalho. |
| **Essa compra faz sentido para mim?** | Analisa necessidade, valor, utilização e aspecto emocional. |
| **Preciso comprar agora?** | Calcula um período de reflexão antes da decisão final. |

### 4.4 Estratégia de desenvolvimento

O projeto seguirá **desenvolvimento incremental**:

```
Planejamento
     ↓
Levantamento de necessidades
     ↓
Definição dos requisitos
     ↓
Modelagem
     ↓
Desenvolvimento do MVP
     ↓
Testes
     ↓
Validação
     ↓
Evolução
```

---

## 5. Público-Alvo

O Worth-It será destinado inicialmente a **usuários brasileiros**.

O público será composto principalmente por **adolescentes, jovens adultos e adultos** interessados em compreender melhor suas decisões financeiras.

O sistema atenderá diferentes situações financeiras:

| Perfil | Descrição |
|---|---|
| **5.1 Usuário trabalhador** | Poderá cadastrar salário, jornada de trabalho e informações relacionadas à sua modalidade profissional. O Worth-It utilizará essas informações para calcular o equivalente de cada produto em horas de trabalho. |
| **5.2 Profissional PJ ou autônomo** | Poderá informar sua remuneração ou diretamente seu valor/hora. O cálculo será baseado principalmente no **valor da hora trabalhada**. |
| **5.3 Adolescente ou usuário sem emprego** | Poderá informar uma mesada ou outra renda periódica. Poderá utilizar normalmente as funcionalidades financeiras do aplicativo, mas o cálculo em horas de trabalho será destinado aos usuários que efetivamente informarem dados profissionais suficientes. |

---

## 6. Objetivos

### 6.1 Objetivo geral

Desenvolver uma aplicação mobile capaz de auxiliar usuários brasileiros a compreender melhor o impacto financeiro de suas compras.

### 6.2 Objetivos específicos

O Worth-It deverá possibilitar:

- identificar produtos por imagem;
- cadastrar produtos manualmente;
- estimar tributos;
- calcular o equivalente do preço em horas trabalhadas;
- criar múltiplas wishlists;
- comparar preços;
- acompanhar possíveis compras;
- avaliar decisões através de questionário;
- calcular Purchase Score;
- definir períodos de reflexão;
- acompanhar compras realizadas e reconsideradas;
- apresentar estatísticas financeiras;
- acompanhar evolução do poder de compra;
- apresentar informações sobre ativos financeiros;
- enviar notificações relacionadas às decisões.

---

## 7. Escopo do Projeto

### 7.1 Dentro do escopo

A primeira versão será uma aplicação mobile com **autenticação obrigatória**.

O sistema terá funcionalidades relacionadas a produtos, impostos, wishlists, decisões de compra, histórico, estatísticas, IA, notificações e organização financeira.

### 7.2 Fora do escopo inicial

Não fazem parte do objetivo principal do MVP:

- aplicação web completa;
- compra de ações ou investimentos dentro do Worth-It;
- funcionamento como banco ou corretora;
- processamento de pagamentos;
- marketplace próprio;
- venda de produtos;
- cálculo do lucro real de uma loja;
- contabilidade ou consultoria tributária;
- substituição de orientação financeira profissional.

---

## 8. Levantamento das Necessidades

Durante o levantamento foram identificadas as seguintes necessidades principais:

| Código | Necessidade | Descrição |
|---|---|---|
| **8.1** | Compreensão do custo | O usuário precisa compreender quanto determinado produto representa em relação à sua própria situação financeira. |
| **8.2** | Compreensão dos tributos | O usuário precisa visualizar de maneira simples quanto do preço corresponde aproximadamente a tributos. |
| **8.3** | Identificação simplificada | O cadastro de um produto não deve exigir preenchimento excessivo. O usuário poderá escolher entre fotografia e formulário manual. |
| **8.4** | Reflexão sobre compras | O sistema deve oferecer ferramentas para reduzir decisões impulsivas, sem impedir o usuário de realizar suas próprias escolhas. |
| **8.5** | Organização | Possíveis compras precisam ser organizadas em diferentes wishlists. |
| **8.6** | Histórico | Produtos removidos das listas não devem necessariamente desaparecer do histórico. |
| **8.7** | Evolução financeira | O usuário deve conseguir comparar o impacto de determinado preço em diferentes momentos de sua vida financeira. |

---

## 9. Definição das Soluções de TI

A arquitetura utilizará tecnologias separadas por responsabilidade.

| Camada | Tecnologia | Responsabilidade |
|---|---|---|
| **Aplicação** | React Native + Expo | Aplicação mobile para Android e iOS. |
| **Backend** | FastAPI + Python | Regras de negócio, cálculos, validações e comunicação segura com serviços externos. |
| **Banco de dados** | Supabase PostgreSQL | Dados estruturados. |
| **Arquivos** | Supabase Storage | Principalmente imagens de produtos e avatares. |
| **Autenticação** | Clerk | Contas, login por e-mail/senha, Google e sessões. |
| **Inteligência Artificial** | OpenRouter | Camada de acesso a modelos de IA, permitindo trocar o modelo sem mudanças significativas na arquitetura. |
| **Tributação** | IBPTax | Tabelas tributárias usadas como referência para estimativas. |
| **Notificações** | Expo Notifications | Notificações push. |

---

## 10. Priorização do Projeto

| Prioridade | Itens |
|---|---|
| **Alta — MVP** | Autenticação, perfil financeiro, produtos, cálculo de horas, Tax Check, IBPTax, wishlists, Purchase Score, período anti-impulso, histórico e decisões. |
| **Média** | Comparação automática de preços, métricas avançadas, streak, notificações e evolução financeira. |
| **Futura** | Recursos mais avançados envolvendo ativos financeiros, histórico de preços, análises mais sofisticadas e novas fontes de dados. |

---

## 11. Requisitos Funcionais

| Código | Requisito |
|---|---|
| **RF001** | O sistema deve permitir criação de conta. |
| **RF002** | O sistema deve permitir autenticação por e-mail e senha. |
| **RF003** | O sistema deve permitir autenticação utilizando Google. |
| **RF004** | O sistema deve exigir autenticação para utilização das funcionalidades pessoais. |
| **RF005** | O usuário deve poder editar seu perfil. |
| **RF006** | O usuário deve poder informar sua situação profissional. |
| **RF007** | O usuário trabalhador deve poder informar renda e jornada. |
| **RF008** | O usuário PJ deve poder informar remuneração ou valor/hora. |
| **RF009** | O usuário sem emprego deve poder informar mesada ou renda periódica. |
| **RF010** | O sistema deve calcular o valor da hora de trabalho quando existirem informações suficientes. |
| **RF011** | O usuário deve poder cadastrar um produto manualmente. |
| **RF012** | O usuário deve poder fotografar uma etiqueta de produto. |
| **RF013** | O sistema deve utilizar IA para interpretar a fotografia. |
| **RF014** | O sistema deve identificar nome, preço e categoria quando possível. |
| **RF015** | O usuário deve poder corrigir informações identificadas automaticamente. |
| **RF016** | O sistema deve permitir associação de EAN/GTIN ao produto. |
| **RF017** | O sistema deve estimar os tributos relacionados ao produto. |
| **RF018** | O sistema deve apresentar o valor estimado dos tributos em reais. |
| **RF019** | O sistema deve apresentar a porcentagem estimada de tributos. |
| **RF020** | O sistema deve apresentar o valor estimado sem tributos. |
| **RF021** | O sistema deve converter o preço em horas de trabalho. |
| **RF022** | O usuário deve poder criar múltiplas wishlists. |
| **RF023** | O usuário deve poder adicionar produtos às wishlists. |
| **RF024** | O usuário deve poder remover produtos das wishlists. |
| **RF025** | Produtos removidos poderão permanecer no histórico. |
| **RF026** | O usuário deve poder informar preços encontrados em diferentes lojas. |
| **RF027** | O sistema poderá pesquisar preços externos. |
| **RF028** | O preço informado pelo usuário deve continuar sendo a referência principal da análise original. |
| **RF029** | O sistema deve permitir iniciar uma análise de decisão de compra. |
| **RF030** | A IA deve adaptar perguntas ao contexto do produto e do usuário. |
| **RF031** | A IA deve atribuir notas para Need, Value, Usage e Emotional. |
| **RF032** | O backend deve calcular o Purchase Score. |
| **RF033** | O sistema deve calcular um período anti-impulso. |
| **RF034** | A IA poderá aumentar justificadamente o período de reflexão. |
| **RF035** | O usuário deve poder marcar uma decisão como *Comprei*. |
| **RF036** | O usuário deve poder marcar uma decisão como *Desisti*. |
| **RF037** | O sistema deve permitir que a decisão continue como *Pensando*. |
| **RF038** | O sistema deve manter histórico das decisões. |
| **RF039** | O sistema deve calcular Taxes Uncovered. |
| **RF040** | O sistema deve calcular Taxes Paid. |
| **RF041** | O sistema deve calcular Purchases. |
| **RF042** | O sistema deve calcular Reconsidered. |
| **RF043** | O sistema deve calcular Thoughtful Streak. |
| **RF044** | O sistema deve enviar notificações push. |
| **RF045** | O usuário deve poder excluir registros de seu histórico quando permitido. |
| **RF046** | Estatísticas devem ser recalculadas após exclusões relevantes. |
| **RF047** | O usuário deve poder excluir sua conta. |
| **RF048** | O sistema deve manter snapshots das análises financeiras. |
| **RF049** | O sistema deve comparar o custo histórico em horas com o custo atual. |
| **RF050** | O sistema deve permitir visualizar informações de ativos financeiros reais. |

---

## 12. Requisitos Não Funcionais

| Código | Requisito |
|---|---|
| **RNF001** | A aplicação deve possuir interface adaptada a dispositivos móveis. |
| **RNF002** | A interface inicial deve estar disponível em PT-BR. |
| **RNF003** | As comunicações devem utilizar HTTPS. |
| **RNF004** | Credenciais e chaves privadas não devem ser armazenadas no aplicativo. |
| **RNF005** | O backend deve validar autenticação antes de operações protegidas. |
| **RNF006** | Usuários não devem acessar informações privadas de outros usuários. |
| **RNF007** | O banco deve utilizar políticas adequadas de controle de acesso. |
| **RNF008** | O sistema deve possuir tratamento de indisponibilidade dos serviços externos. |
| **RNF009** | Falhas da IA não devem impedir acesso a dados já armazenados. |
| **RNF010** | Informações históricas devem permanecer consistentes após mudanças no perfil financeiro. |
| **RNF011** | O sistema deve possuir suporte a tema claro e escuro. |
| **RNF012** | O usuário deve poder ajustar o tamanho do texto quando disponibilizado. |
| **RNF013** | O sistema deve seguir princípios de acessibilidade mobile. |
| **RNF014** | Dados pessoais devem ser minimizados ao necessário para as funcionalidades. |
| **RNF015** | O usuário deve possuir mecanismos para exclusão de sua conta e dados associados conforme as regras aplicáveis. |

---

## 13. Regras de Negócio

### RN001 — Conta obrigatória

O usuário precisa estar autenticado para utilizar as funcionalidades pessoais do Worth-It.

### RN002 — Produto global

Um produto deve possuir uma **identidade global** sempre que for possível identificá-lo corretamente.

**Exemplo:**

```
AirPods Pro 2
EAN: XXXXXXXXXXXXX
```

Esse produto **não** deve ser duplicado para cada usuário.

Os dados pessoais relacionados ao produto — wishlist, preço observado, análise e decisão — continuam pertencendo ao usuário.

### RN003 — Preço principal

O preço informado ou capturado pelo usuário será considerado o **preço principal** daquela análise.

### RN004 — Imposto não representa lucro

O Worth-It **não** deve apresentar:

```
Preço - impostos = lucro da loja
```

Essa conclusão seria incorreta porque o sistema não possui os custos reais do vendedor. Deve ser apresentado **valor estimado sem tributos**, e não lucro.

### RN005 — Taxes Uncovered

Toda análise tributária válida poderá contribuir para **Taxes Uncovered**, independentemente da compra ter sido realizada.

### RN006 — Taxes Paid

Somente produtos posteriormente marcados como `PURCHASED` contribuem para a estimativa de **Taxes Paid**.

### RN007 — Reconsidered

Quando o usuário indicar que desistiu da compra:

```
status = RECONSIDERED
```

### RN008 — Purchase

Um produto que entra no fluxo de intenção de compra passa a representar uma **possível compra**.

### RN009 — Thoughtful Streak

A entrada válida no aplicativo em **dias consecutivos** mantém a sequência.

**Exemplo:**

| Dia | Entrou? | Streak |
|---|---|---|
| Dia 1 | Sim | 1 |
| Dia 2 | Sim | 2 |
| Dia 3 | Não | — |
| Dia 4 | Sim | 1 |

A sequência anterior poderá permanecer no histórico, embora a sequência atual seja reiniciada.

### RN010 — Snapshot

Toda análise relevante deve armazenar o **contexto financeiro utilizado naquele momento**. Um resultado histórico não deve ser sobrescrito após alteração salarial.

### RN011 — Evolução financeira

O sistema poderá recalcular o impacto atual para comparação.

**Exemplo:**

> Há 3 meses este produto representava **20 horas** do seu trabalho. Hoje representa **10 horas**.

---

## 14. Sistema de Decisão de Compra

A análise de compra é uma das **funcionalidades centrais** do Worth-It.

O fluxo será:

```
Produto
   ↓
Questionário adaptativo
   ↓
Interpretação pela IA
   ↓
Need
Value
Usage
Emotional
   ↓
Fórmula do Purchase Score
   ↓
Score 0–100
   ↓
Período anti-impulso
   ↓
Recomendação
   ↓
Pensando
   ↓
Comprei / Desisti
```

> A IA **não** tomará a decisão pelo usuário.

---

## 15. Purchase Score

A análise utiliza quatro dimensões:

| Dimensão | Peso |
|---|---|
| **Need** | 2 |
| **Value** | 1 |
| **Usage** | 2 |
| **Emotional** | 1 |

A IA analisa o contexto e atribui uma nota entre **0 e 100** para cada dimensão. O backend calcula:

$$
Score = \frac{(Need \times 2) + (Value) + (Usage \times 2) + (Emotional)}{6}
$$

### Exemplo

Supondo:

| Dimensão | Nota |
|---|---|
| Need | 90 |
| Value | 75 |
| Usage | 95 |
| Emotional | 70 |

O cálculo será:

$$
\frac{180 + 75 + 190 + 70}{6} = 85{,}83
$$

O sistema poderá apresentar:

```
Purchase Score: 86/100
```

> O resultado matemático **não** será escolhido diretamente pela IA.

---

## 16. Período Anti-Impulso

O Purchase Score será utilizado para determinar o **período mínimo recomendado de reflexão**. A fórmula será:

$$
DiasBase = \left\lceil \frac{100 - Score}{10} \right\rceil
$$

### Exemplos

| Score | Dias base |
|---|---|
| 95 | 1 |
| 86 | 2 |
| 80 | 2 |
| 72 | 3 |
| 60 | 4 |
| 50 | 5 |
| 35 | 7 |
| 20 | 8 |
| 10 | 9 |
| 0 | 10 |

### 16.1 Ajuste pela IA

Após o cálculo, a IA poderá adicionar de **0 a 4 dias**.

$$
PeriodoFinal = DiasBase + AcrescimoIA
$$

- A IA **não** poderá reduzir o período base.
- Qualquer aumento deverá possuir **justificativa**.

**Exemplo:**

| Item | Valor |
|---|---|
| Purchase Score | 20/100 |
| Período base | 8 dias |
| Ajuste da IA | +2 dias |
| **Período recomendado** | **10 dias** |

A justificativa poderá informar que a análise identificou baixo uso esperado ou forte componente emocional.

### 16.2 Final do período

Ao terminar o período, o sistema poderá perguntar:

> Ainda está pensando nessa compra?
> Você comprou, desistiu ou quer continuar pensando?

As opções serão:

| Opção | Valor |
|---|---|
| Comprei | `COMPREI` |
| Desisti | `DESISTI` |
| Continuar pensando | `CONTINUAR PENSANDO` |

---

## 17. Modelagem Inicial do Banco de Dados

O banco principal será **PostgreSQL** através do **Supabase**.

### `users`

| Campo |
|---|
| `id` |
| `clerk_user_id` |
| `username` |
| `display_name` |
| `avatar_url` |
| `state_code` |
| `created_at` |
| `updated_at` |

### `financial_profiles`

| Campo |
|---|
| `id` |
| `user_id` |
| `income_type` |
| `monthly_income` |
| `allowance_amount` |
| `hourly_rate` |
| `weekly_work_hours` |
| `overtime_enabled` |
| `overtime_rate` |
| `created_at` |
| `updated_at` |

### `user_preferences`

| Campo |
|---|
| `id` |
| `user_id` |
| `theme` |
| `text_size` |
| `notifications_enabled` |
| `recommendations_enabled` |
| `currency` |
| `updated_at` |

### `products`

| Campo |
|---|
| `id` |
| `ean_gtin` |
| `name` |
| `brand` |
| `category` |
| `description` |
| `created_at` |
| `updated_at` |

### `stores`

| Campo |
|---|
| `id` |
| `name` |
| `website_url` |
| `created_at` |

### `product_prices`

| Campo |
|---|
| `id` |
| `product_id` |
| `user_id` |
| `store_id` |
| `price` |
| `source_type` |
| `source_url` |
| `captured_at` |

### `product_images`

| Campo |
|---|
| `id` |
| `product_id` |
| `user_id` |
| `storage_path` |
| `image_type` |
| `created_at` |

### `wishlists`

| Campo |
|---|
| `id` |
| `user_id` |
| `name` |
| `description` |
| `created_at` |
| `updated_at` |

### `wishlist_items`

| Campo |
|---|
| `id` |
| `wishlist_id` |
| `product_id` |
| `price_id` |
| `status` |
| `priority` |
| `added_at` |
| `removed_at` |

### `tax_analyses`

| Campo |
|---|
| `id` |
| `user_id` |
| `product_id` |
| `price` |
| `tax_rate` |
| `tax_amount` |
| `product_value_without_tax` |
| `state_code` |
| `ibpt_code` |
| `ibpt_version` |
| `created_at` |

### `purchase_decisions`

| Grupo | Campos |
|---|---|
| **Identificação** | `id`, `user_id`, `product_id`, `wishlist_item_id` |
| **Notas** | `need_score`, `value_score`, `usage_score`, `emotional_score`, `purchase_score` |
| **Reflexão** | `base_reflection_days`, `ai_extra_days`, `final_reflection_days`, `ai_reason` |
| **Período** | `reflection_started_at`, `reflection_ends_at` |
| **Decisão** | `decision`, `decided_at` |
| **Snapshot** | `hourly_rate_snapshot`, `work_hours_snapshot` |
| **Controle** | `created_at`, `updated_at` |

### `decision_answers`

| Campo |
|---|
| `id` |
| `decision_id` |
| `question` |
| `answer` |
| `question_category` |
| `created_at` |

### `ai_analyses`

| Campo |
|---|
| `id` |
| `user_id` |
| `product_id` |
| `analysis_type` |
| `model` |
| `prompt_version` |
| `input_hash` |
| `response` |
| `created_at` |

### `daily_activity`

| Campo |
|---|
| `id` |
| `user_id` |
| `activity_date` |
| `created_at` |

### `investment_assets`

| Campo |
|---|
| `id` |
| `symbol` |
| `name` |
| `asset_type` |
| `current_price` |
| `updated_at` |

### `notifications`

| Campo |
|---|
| `id` |
| `user_id` |
| `type` |
| `title` |
| `message` |
| `scheduled_at` |
| `sent_at` |
| `read_at` |
| `created_at` |

---

## 18. Armazenamento de Imagens

As imagens **não** serão armazenadas diretamente nas colunas do PostgreSQL.

O Supabase Storage poderá utilizar inicialmente:

```
avatars/
product-images/
```

O banco armazenará apenas a **referência ao arquivo**.

### Política de exclusão

- Remover um produto da wishlist **não** remove automaticamente sua imagem, pois o produto poderá continuar no histórico.
- Caso o registro seja definitivamente excluído e nenhuma outra entidade utilize a imagem, o arquivo poderá ser removido do Storage.
- A exclusão de conta deverá iniciar também o processo de remoção dos dados pessoais e arquivos associados, conforme as regras de retenção aplicáveis.

---

## 19. Arquitetura

A arquitetura lógica principal será:

```
                 ┌───────────────┐
                 │     Clerk     │
                 │     Auth      │
                 └───────▲───────┘
                         │
                         │ Auth
                         │
┌──────────────┐   HTTPS │   ┌──────────────┐
│              │─────────┼──►│              │
│  Mobile App  │         │   │   FastAPI    │
│ React Native │─────────────►│  API Server  │
│    + Expo    │             │              │
└──────────────┘             └──────┬───────┘
                                    │
                 ┌──────────────────┼──────────────────┐
                 │                  │                  │
                 ▼                  ▼                  ▼
          ┌────────────┐     ┌────────────┐     ┌────────────┐
          │ OpenRouter │     │   IBPTax   │     │  Supabase  │
          │     AI     │     │ Tax Tables │     │ PostgreSQL │
          └────────────┘     └────────────┘     │ + Storage  │
                                                └────────────┘
```

> O aplicativo **não** deverá possuir diretamente chaves privadas de OpenRouter ou outros serviços sensíveis.

---

## 20. API — Estrutura Inicial

A API poderá ser organizada por domínio:

| Rota base |
|---|
| `/api/v1/auth` |
| `/api/v1/users` |
| `/api/v1/profile` |
| `/api/v1/products` |
| `/api/v1/prices` |
| `/api/v1/taxes` |
| `/api/v1/wishlists` |
| `/api/v1/decisions` |
| `/api/v1/history` |
| `/api/v1/statistics` |
| `/api/v1/investments` |
| `/api/v1/notifications` |

### Exemplos de endpoints

| Domínio | Método | Endpoint |
|---|---|---|
| **Perfil** | `GET` | `/api/v1/profile` |
| | `PATCH` | `/api/v1/profile` |
| **Produtos** | `POST` | `/api/v1/products` |
| | `GET` | `/api/v1/products/{id}` |
| | `POST` | `/api/v1/products/analyze-image` |
| **Impostos** | `POST` | `/api/v1/taxes/calculate` |
| **Wishlists** | `GET` | `/api/v1/wishlists` |
| | `POST` | `/api/v1/wishlists` |
| | `POST` | `/api/v1/wishlists/{id}/items` |
| | `DELETE` | `/api/v1/wishlists/{id}/items/{item_id}` |
| **Decisões** | `POST` | `/api/v1/decisions` |
| | `POST` | `/api/v1/decisions/{id}/answers` |
| | `POST` | `/api/v1/decisions/{id}/evaluate` |
| | `PATCH` | `/api/v1/decisions/{id}/purchase` |
| | `PATCH` | `/api/v1/decisions/{id}/reconsider` |
| | `PATCH` | `/api/v1/decisions/{id}/continue` |
| **Estatísticas e histórico** | `GET` | `/api/v1/statistics` |
| | `GET` | `/api/v1/history` |

---

## 21. Inteligência Artificial

A integração utilizará **OpenRouter** com **modelo configurável**. Isso significa que a arquitetura não ficará presa a um modelo específico.

A IA será utilizada principalmente para:

```
Imagem da etiqueta
        ↓
Extração de informações

Produto + usuário
        ↓
Criação/adaptação das perguntas

Respostas
        ↓
Interpretação
        ↓
Need / Value / Usage / Emotional
        ↓
Explicação do resultado
        ↓
Possível acréscimo no período de reflexão
```

A IA **não** deverá ser responsável por operações determinísticas que podem ser realizadas pelo backend.

**Exemplos:**

| Quem | Responsabilidade |
|---|---|
| **IA** | Interpreta respostas. |
| **Backend** | Aplica os pesos e calcula o Purchase Score. |
| **IA** | Recomenda +2 dias. |
| **Backend** | Verifica se o valor está dentro de 0–4 e calcula o período final. |

---

## 22. Histórico e Estatísticas

### Principais métricas

| Métrica | Descrição |
|---|---|
| **Taxes Uncovered** | Soma das estimativas tributárias descobertas nas análises. |
| **Taxes Paid** | Soma estimada dos tributos presentes apenas nos produtos marcados como comprados. |
| **Purchases** | Quantidade de produtos registrados como possíveis compras. |
| **Decisions Made** | Quantidade de decisões efetivamente concluídas conforme a regra de decisão do sistema. |
| **Reconsidered** | Quantidade de compras abandonadas após reflexão. |
| **Thoughtful Streak** | Quantidade atual de dias consecutivos em que o usuário acessou o aplicativo. |

### Evolução financeira

O histórico poderá comparar o valor/hora utilizado originalmente com o atual.

**Exemplo:**

| Item | Valor |
|---|---|
| **Produto** | Notebook |
| **Preço analisado** | R$ 4.000 |
| **Abril** | 40 horas de trabalho |
| **Outubro** | 25 horas de trabalho |

> O snapshot original continua preservado.

---

## 23. Segurança e Privacidade

A arquitetura deverá seguir o princípio de que o aplicativo mobile **nunca é considerado uma fonte confiável** para autorizar operações sensíveis.

- O backend deve validar as requisições autenticadas antes de acessar dados privados.
- Informações sensíveis não devem ser enviadas ou armazenadas desnecessariamente.
- O sistema deverá utilizar conexões criptografadas em trânsito e controles de acesso no banco.

Chaves como:

```
OPENROUTER_API_KEY
SUPABASE_SERVICE_ROLE_KEY
```

**não** deverão estar presentes no código distribuído do aplicativo.

> Como o público inclui adolescentes, a implementação final também deverá considerar cuidadosamente os requisitos legais e de privacidade aplicáveis ao tratamento de dados de menores no Brasil.

---

## 24. Estados Principais

Um item de wishlist poderá utilizar estados semelhantes a:

| Estado | Significado |
|---|---|
| `SAVED` | Salvo na lista |
| `THINKING` | Em reflexão |
| `READY` | Pronto para decisão |
| `PURCHASED` | Comprado |
| `RECONSIDERED` | Desistência após reflexão |
| `REMOVED` | Removido da lista, sem necessariamente apagar o histórico |

### Fluxo principal

```
SAVED
  │
  ▼
THINKING
  │
  ├──────────────► PURCHASED
  │
  ├──────────────► RECONSIDERED
  │
  └──────────────► THINKING
                   (continuar pensando)
```

---

## 25. Limitações Conhecidas

A primeira versão terá algumas limitações importantes:

- A identificação de produtos por imagem pode apresentar erros e deverá permitir correção pelo usuário.
- As estimativas tributárias **não** representam cálculo fiscal individual exato.
- A pesquisa de preços poderá não encontrar exatamente a mesma variante do produto.
- Resultados produzidos por modelos de IA podem variar e, por isso, regras matemáticas importantes serão executadas pelo backend.
- O Worth-It não saberá o custo operacional real de uma loja e, portanto, **não** apresentará o valor sem impostos como lucro do vendedor.
- Informações sobre investimentos terão caráter informativo e organizacional; o Worth-It **não** executará ordens de compra ou venda.

---

## 26. Roadmap Inicial

| Fase | Nome | Entregas |
|---|---|---|
| **Fase 1** | Fundação | Projeto mobile, FastAPI, Supabase, Clerk e estrutura inicial do banco. |
| **Fase 2** | Produto | Cadastro manual, imagem, catálogo, preços e cálculo de horas. |
| **Fase 3** | Tributação | Integração com IBPTax e Tax Check. |
| **Fase 4** | Organização | Wishlists, histórico e estados dos produtos. |
| **Fase 5** | Decisão | Questionário adaptativo, Purchase Score, IA e período anti-impulso. |
| **Fase 6** | Engajamento | Notificações, Thoughtful Streak e estatísticas. |
| **Fase 7** | Inteligência financeira | Comparação histórica, pesquisa de preços e informações sobre ativos. |
| **Fase 8** | Refinamento | Testes, acessibilidade, segurança, desempenho e publicação. |