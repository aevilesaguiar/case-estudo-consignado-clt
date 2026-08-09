### Resumo do Fluxo As-Is

A jornada do consignado pela CTPS Digital começa com a solicitação do trabalhador e o recebimento de ofertas das instituições financeiras. O principal ponto positivo ocorre na escolha da proposta, quando o cliente sente autonomia para comparar as condições e selecionar a melhor oferta.

O maior problema surge após essa escolha, quando o trabalhador precisa sair da CTPS Digital e continuar a contratação no canal da instituição financeira. Essa mudança gera insegurança, medo de fraude, espera pelo contato do banco e maior risco de **drop-off**.

**Drop-off**, ou taxa de abandono, acontece quando o usuário inicia uma jornada, mas desiste antes de concluí-la. Por exemplo: se 1.000 trabalhadores escolhem uma proposta na etapa 5, mas apenas 600 concluem a averbação na etapa 9, então 400 abandonaram o processo, representando uma taxa de drop-off de 40%.

No fluxo do consignado, as principais causas de abandono são:

* Troca de canal entre a CTPS Digital e a instituição financeira;
* Repetição de dados, autorizações, biometria e validações;
* Medo de golpes por WhatsApp, ligação ou e-mail;
* Demora no contato ou no processamento da proposta;
* Falta de clareza sobre CET, taxas, parcelas e condições;
* Instabilidades técnicas na CTPS Digital, Dataprev ou Serpro.

Para as instituições financeiras, existe ainda o risco de negar a proposta quando a análise detalhada identifica um perfil de crédito diferente do inicialmente previsto, pois a taxa ofertada não pode ser aumentada. Isso aumenta a frustração do trabalhador e pode comprometer sua confiança no processo.

A satisfação volta a crescer somente após a averbação e a liberação do dinheiro. Portanto, o principal gargalo está entre as etapas 6 e 8, onde a quebra de contexto, a burocracia, a insegurança e as falhas técnicas aumentam o drop-off e reduzem a conversão.

Reduzir essa taxa de abandono deve ser um dos principais objetivos das equipes de **Produto, UX e Otimização de Conversão (CRO)**, pois cada desistência representa a perda de um cliente que já havia demonstrado intenção real de contratar o crédito.


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/305ab085-3468-45be-82d1-c59273afad8d" />

O funil deve mostrar quantos trabalhadores avançam em cada etapa, onde abandonam e quanto tempo levam para concluir. No consignado via CTPS Digital, eu estruturaria assim:

**Acesso → Solicitação → Ofertas → Escolha → Transição para a IF → Autorização → Validação → Averbação → Crédito liberado**

## Métricas por etapa do funil

| Etapa do fluxo                  | Métrica principal                        | Como calcular                                                             | O que ela indica                                                 |
| ------------------------------- | ---------------------------------------- | ------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| **1 → 2. Acesso e solicitação** | **Taxa de início da jornada**            | Solicitações realizadas ÷ acessos à jornada                               | Se o usuário entende como começar e encontra valor na proposta   |
| **2 → 3. Envio para as IFs**    | **Taxa de processamento da solicitação** | Solicitações enviadas às IFs ÷ solicitações realizadas                    | Falhas técnicas, indisponibilidade ou problemas de elegibilidade |
| **3 → 4. Retorno das IFs**      | **Taxa de recebimento de ofertas**       | Clientes que receberam oferta ÷ clientes consultados                      | Capacidade das IFs de responder às solicitações                  |
| **3 → 4. Retorno das IFs**      | **Tempo para receber a primeira oferta** | Horário da primeira oferta − horário da solicitação                       | Lentidão das instituições e impacto da espera na jornada         |
| **4. Ofertas recebidas**        | **Quantidade média de ofertas**          | Total de ofertas ÷ clientes que receberam ofertas                         | Nível de concorrência e possibilidade real de comparação         |
| **4 → 5. Escolha**              | **Taxa de seleção da oferta**            | Clientes que escolheram uma proposta ÷ clientes que receberam ofertas     | Atratividade das taxas, CET, prazo e parcelas                    |
| **5 → 6. Mudança de canal**     | **Taxa de sucesso no handoff**           | Clientes que chegaram ao canal da IF ÷ clientes que escolheram a proposta | Eficiência da transição entre CTPS Digital e banco               |
| **5 → 6. Mudança de canal**     | **Drop-off na transição**                | Clientes que não chegaram à IF ÷ clientes que escolheram a proposta       | Perda causada por troca de canal, medo de golpe ou demora        |
| **6. Contato da IF**            | **Tempo para o primeiro contato**        | Horário do contato − horário da escolha                                   | Se o lead está sendo atendido antes de perder o interesse        |
| **6 → 7. Autorização**          | **Taxa de conclusão da autorização**     | Autorizações concluídas ÷ clientes direcionados à IF                      | Impacto da repetição de permissões e da burocracia               |
| **7 → 8. Validação**            | **Taxa de sucesso da validação**         | Validações concluídas ÷ autorizações realizadas                           | Funcionamento da biometria, token e validação do vínculo         |
| **7 → 8. Validação**            | **Taxa de falha na biometria**           | Biometrias com falha ÷ tentativas de biometria                            | Quanto a tecnologia está impedindo o avanço do cliente           |
| **8. Análise detalhada**        | **Taxa de aprovação**                    | Propostas aprovadas ÷ propostas analisadas                                | Qualidade da oferta inicial e aderência ao risco real            |
| **8. Análise detalhada**        | **Taxa de recusa**                       | Propostas negadas ÷ propostas analisadas                                  | Perdas por risco, vínculo, margem ou regras de crédito           |
| **8 → 9. Averbação**            | **Taxa de sucesso na averbação**         | Contratos averbados ÷ propostas aprovadas                                 | Eficiência da integração com Dataprev/Serpro                     |
| **9. Crédito liberado**         | **Taxa de conversão final**              | Créditos liberados ÷ jornadas iniciadas                                   | Resultado completo do funil                                      |
| **1 → 9 ou 5 → 9**              | **Time to Cash**                         | Data/hora da liberação − início da jornada                                | Tempo total necessário para o dinheiro chegar ao trabalhador     |

## As métricas mais importantes

### 1. Taxa de conversão por etapa

<img width="737" height="212" alt="image" src="https://github.com/user-attachments/assets/79bb05ed-1cbe-4ad5-a940-982e9c73c4ea" />

---

### 2. Drop-off por etapa

<img width="772" height="363" alt="image" src="https://github.com/user-attachments/assets/6e194023-0ef7-4d46-8c7e-5af23084aa56" />


---

### 3. Conversão pós-escolha

<img width="777" height="231" alt="image" src="https://github.com/user-attachments/assets/40e7d9e8-39de-4b19-8d5d-bf99ef3e2ab7" />


---

### 4. Tempo para o primeiro contato

Mede quanto tempo a instituição demora para abordar o trabalhador depois da escolha.

Essa métrica se aplica principalmente na transição da **etapa 5 para a 6**. Quanto maior o tempo, maior a possibilidade de o cliente:

* Esfriar o interesse;
* Desconfiar do contato;
* Escolher outro canal;
* Desistir da contratação.

É importante acompanhar a **mediana** e o **percentil 90**, não apenas a média, para identificar clientes que estão esperando tempo excessivo.

---

### 5. Time to Cash

Mede o tempo entre o início da jornada e o dinheiro na conta.

Pode ser analisado de duas maneiras:

* **Time to Cash completo:** etapa 1 → etapa 9;
* **Time to Cash da IF:** etapa 5 → etapa 9.

Ele mostra a velocidade real da contratação e ajuda a localizar esperas entre contato, validação, análise e averbação.

## Exemplo resumido do funil

| Etapa                   | Clientes | Conversão para a próxima etapa | Drop-off |
| ----------------------- | -------: | -----------------------------: | -------: |
| Escolheram a proposta   |    1.000 |                            90% |      10% |
| Chegaram ao canal da IF |      900 |                          86,7% |    13,3% |
| Autorizaram a consulta  |      780 |                          89,7% |    10,3% |
| Foram aprovados         |      700 |                          85,7% |    14,3% |
| Receberam o crédito     |      600 |                              — |        — |

Nesse exemplo, a conversão pós-escolha é de **60%**. O maior abandono percentual acontece entre a aprovação e a averbação, mas também existe uma perda relevante na autorização.

## Indicadores prioritários para um dashboard

Eu priorizaria:

1. **Conversão total da jornada:** etapa 1 → 9;
2. **Conversão pós-escolha:** etapa 5 → 9;
3. **Drop-off por etapa e motivo;**
4. **Taxa de sucesso no handoff:** etapa 5 → 6;
5. **Tempo para o primeiro contato da IF;**
6. **Taxa de conclusão da autorização;**
7. **Taxa de sucesso da biometria e validação;**
8. **Taxa de aprovação e motivos de recusa;**
9. **Taxa de sucesso na averbação;**
10. **Time to Cash.**

Para a instituição financeira, a principal métrica de resultado seria a **conversão da proposta escolhida em crédito liberado — etapa 5 até a 9**. O **drop-off por etapa**, o **tempo para o primeiro contato** e o **Time 


Como PM, sua principal mudança de atuação é sair de **“como o time está entregando”** para assumir **“qual problema devemos resolver, para quem e qual resultado de negócio queremos mudar”**.

No consignado via CTPS Digital, eu focaria no problema entre as etapas **5 e 9**, especialmente na mudança de canal da CTPS para a instituição financeira.

## 1. Defina claramente o problema de produto

Uma boa formulação seria:

> Trabalhadores que já escolheram uma proposta na CTPS Digital não conseguem concluir a contratação devido à quebra de contexto, demora no contato, medo de fraude, repetição de autorizações e falhas nas validações. Isso aumenta o drop-off, reduz a conversão da instituição financeira e prejudica a confiança do cliente.

Essa formulação conecta:

* Problema do cliente;
* Problema operacional;
* Impacto no negócio;
* Etapas do funil afetadas.

## 2. Estruture o funil e encontre o verdadeiro gargalo

Antes de propor uma solução, você precisa descobrir onde a perda realmente acontece.

| Passagem do funil | Pergunta que você deve responder                         |
| ----------------- | -------------------------------------------------------- |
| Etapa 1 → 2       | Quantos usuários acessam, mas não solicitam proposta?    |
| Etapa 2 → 4       | Quantos solicitam, mas não recebem ofertas?              |
| Etapa 4 → 5       | Quantos recebem ofertas, mas não escolhem nenhuma?       |
| **Etapa 5 → 6**   | Quantos escolhem o banco, mas não chegam ao canal da IF? |
| **Etapa 6 → 7**   | Quantos são contatados, mas não autorizam a consulta?    |
| **Etapa 7 → 8**   | Quantos abandonam ou falham na biometria e validação?    |
| **Etapa 8 → 9**   | Quantos são aprovados, mas não conseguem averbar?        |

Não basta saber que a conversão final é baixa. Como PM, você precisa identificar:

* Em qual etapa acontece a maior perda;
* Qual o volume perdido;
* Quais são os motivos;
* Quais problemas estão sob controle da instituição;
* Quais dependem de CTPS, MTE, Dataprev, Serpro ou parceiros.

## 3. Escolha uma métrica principal

Para esse problema, eu utilizaria como métrica principal:

> **Taxa de conversão da proposta escolhida em crédito liberado — etapa 5 até a etapa 9.**

[
\text{Conversão pós-escolha} =
\frac{\text{créditos liberados}}
{\text{propostas escolhidas}}
\times 100
]

Essa métrica é poderosa porque considera clientes que já demonstraram intenção real de contratar.

Como métricas de apoio:

* Drop-off em cada etapa;
* Taxa de sucesso na transição para a IF;
* Tempo para o primeiro contato;
* Taxa de conclusão da autorização;
* Taxa de sucesso da biometria;
* Taxa de aprovação;
* Taxa de sucesso da averbação;
* Time to Cash;
* Motivos de abandono e recusa.

Como métricas de proteção — para não melhorar conversão aumentando risco:

* Fraudes;
* Inadimplência;
* Reclamações;
* Contestações;
* Erros de contratação;
* Incidentes regulatórios;
* Qualidade da carteira.

## 4. Faça Discovery antes de definir o To-Be

Você deve investigar tanto o comportamento do cliente quanto os bastidores operacionais.

### Com trabalhadores

Pesquise:

* Como reconheceram o contato verdadeiro da instituição?
* O que sentiram ao sair da CTPS Digital?
* Entenderam que precisariam continuar em outro canal?
* Por que abandonaram a jornada?
* Tiveram dificuldades com biometria ou autenticação?
* Entenderam CET, taxa, parcelas e valor liberado?
* Sabiam acompanhar o status da proposta?

### Com áreas internas

Converse com:

* Atendimento e call center;
* Operações de crédito;
* Risco;
* Prevenção a fraudes;
* Compliance e Jurídico;
* Tecnologia e arquitetura;
* Marketing e CRM;
* Correspondentes, quando aplicável;
* Times responsáveis pelas integrações externas.

Procure evidências em:

* Analytics do funil;
* Logs técnicos;
* Motivos de recusa;
* Reclamações;
* Ligações para a central;
* Falhas de biometria;
* Tempo entre as etapas;
* Propostas paradas ou expiradas.

## 5. Transforme as dores em hipóteses

Evite começar dizendo “precisamos criar uma nova tela”. Comece com hipóteses de resultado.

### Hipótese 1 — Transição confiável

> Se o trabalhador receber uma confirmação oficial e um direcionamento autenticado para o canal da IF, então o medo de golpe e o abandono entre as etapas 5 e 6 diminuirão.

Possíveis soluções:

* Deep link autenticado;
* Notificação oficial dentro da CTPS;
* Código de confirmação da proposta;
* Identificação clara da instituição escolhida;
* Tela explicando os próximos passos;
* Comunicação padronizada e verificável.

### Hipótese 2 — Contato mais rápido

> Se a IF realizar o primeiro contato em poucos minutos, aumentará a conversão antes que o cliente perca o interesse.

Possíveis soluções:

* Automação do recebimento do lead;
* SLA para primeiro contato;
* Priorização de propostas com maior intenção;
* Alerta de proposta parada;
* Retomada automática da jornada.

### Hipótese 3 — Redução de retrabalho

> Se dados, consentimentos e validações puderem ser reaproveitados dentro das regras legais, o esforço do cliente e as falhas de autenticação serão reduzidos.

Possíveis soluções:

* Pré-preenchimento;
* Reutilização de consentimento, quando permitida;
* Menos solicitações de dados repetidos;
* Biometria com alternativas de recuperação;
* Continuidade da sessão.

### Hipótese 4 — Acompanhamento da proposta

> Se o trabalhador conseguir visualizar o status e o próximo passo, diminuirão a ansiedade, os contatos na central e o abandono.

Possíveis status:

* Proposta escolhida;
* Aguardando contato;
* Validação pendente;
* Em análise;
* Aguardando averbação;
* Crédito liberado;
* Proposta recusada, com motivo compreensível.

## 6. Priorize por impacto, esforço e risco

Eu começaria por melhorias que tenham alto impacto na conversão e menor dependência externa:

1. Explicação dos próximos passos após a escolha;
2. Comunicação confiável e padronizada;
3. SLA para o primeiro contato;
4. Monitoramento do funil e motivos de abandono;
5. Acompanhamento do status da proposta;
6. Recuperação de jornadas abandonadas;
7. Redução de dados e autorizações repetidas;
8. Integrações estruturais com CTPS, Dataprev ou Serpro.

As primeiras iniciativas podem ser mais rápidas. Já o reaproveitamento de consentimento ou identidade exige análise técnica, jurídica, regulatória e de segurança.

## O que você deve estudar

### 1. Negócio de crédito consignado

Entenda:

* Margem consignável;
* Elegibilidade;
* CET;
* Taxa de juros;
* Prazo e parcela;
* Averbação;
* Liquidação;
* Portabilidade e refinanciamento;
* Vínculo empregatício;
* Risco de crédito;
* Inadimplência;
* Spread;
* Custo de funding;
* Ticket médio;
* Receita e rentabilidade da operação.

### 2. Crédito do Trabalhador e seus atores

Mapeie o papel de:

* Trabalhador;
* CTPS Digital;
* Ministério do Trabalho;
* Empregador;
* eSocial;
* Instituição financeira;
* Dataprev/Serpro;
* Áreas de risco, fraude e compliance;
* Operação e atendimento.

Você não precisa decorar todas as regras. Precisa entender como elas afetam a jornada, a conversão, o risco e as decisões do produto.

### 3. Funil e Product Analytics

Aprofunde:

* Conversão;
* Drop-off;
* Taxa de aprovação;
* Taxa de averbação;
* Time to Cash;
* Tempo por etapa;
* Coortes;
* Segmentação;
* Eventos de produto;
* Motivos de abandono;
* Testes A/B;
* Dashboards de funil.

### 4. Discovery e experiência do usuário

Estude:

* JTBD;
* Jornada do cliente;
* Service Blueprint;
* Entrevistas com usuários;
* Problem Framing;
* Opportunity Solution Tree;
* Testes de usabilidade;
* CES, CSAT e NPS;
* Hipóteses e experimentação.

O **Service Blueprint** é especialmente importante, pois permite mostrar o que o cliente vê e tudo o que acontece nos bastidores da IF.

### 5. Tecnologia e integrações

Como PM, você não precisa programar a solução, mas deve compreender:

* APIs;
* Webhooks;
* Processamento síncrono e assíncrono;
* Timeout e indisponibilidade;
* Retentativas;
* Idempotência;
* SLA;
* Logs e rastreabilidade;
* Monitoramento;
* Integrações com sistemas externos;
* Tratamento de falhas e contingência.

### 6. Segurança e regulamentação

Estude os conceitos relacionados a:

* LGPD e consentimento;
* KYC;
* Biometria;
* Prevenção a fraudes;
* Autenticação;
* Segurança na troca de canal;
* Transparência do CET;
* Registro de evidências;
* Regras de concessão e averbação.

## Seu foco principal como PM

Para esse case, eu concentraria sua narrativa em cinco pontos:

1. **Problema:** abandono depois da escolha da proposta;
2. **Evidência:** funil, drop-off, tempo e motivos;
3. **Oportunidade:** melhorar a continuidade entre CTPS e IF;
4. **Solução:** transição confiável, rápida e com menos retrabalho;
5. **Resultado:** aumentar a conversão pós-escolha sem elevar fraude, inadimplência ou risco regulatório.

Sua experiência como Agile Coach já ajuda muito em fluxo, indicadores, dependências e facilitação. Para fortalecer sua atuação como PM, aprofunde principalmente **cliente, negócio de crédito, estratégia, experimentação e impacto financeiro**. O diferencial será mostrar que você não está apenas organizando a entrega: está escolhendo o problema certo e conduzindo o produto para um resultado mensurável.
to Cash** seriam as métricas de diagnóstico para explicar por que essa conversão aumenta ou diminui.

