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

Mostra quantos clientes conseguiram avançar.

[
\text{Conversão da etapa} =
\frac{\text{clientes que avançaram}}
{\text{clientes que entraram na etapa}}
\times 100
]

Exemplo: 1.000 clientes escolheram uma proposta e 900 chegaram ao canal da IF:

[
900 \div 1.000 = 90%
]

A conversão da etapa 5 para a 6 foi de **90%**.

---

### 2. Drop-off por etapa

Mostra quantos usuários desistiram ou foram impedidos de avançar.

[
\text{Drop-off} =
\frac{\text{clientes que entraram} - \text{clientes que avançaram}}
{\text{clientes que entraram}}
\times 100
]

No mesmo exemplo:

[
(1.000 - 900) \div 1.000 = 10%
]

O drop-off entre a escolha e a chegada ao canal da IF foi de **10%**.

O ideal é medir o abandono em cada passagem, principalmente:

* Etapa 5 → 6: mudança de canal;
* Etapa 6 → 7: espera e nova autorização;
* Etapa 7 → 8: biometria e validações;
* Etapa 8 → 9: aprovação e averbação.

---

### 3. Conversão pós-escolha

Essa é uma das métricas mais importantes para a instituição financeira, porque parte de clientes que já demonstraram intenção real de contratar.

[
\text{Conversão pós-escolha} =
\frac{\text{créditos liberados na etapa 9}}
{\text{propostas escolhidas na etapa 5}}
\times 100
]

Se 1.000 pessoas escolheram a proposta e 600 receberam o crédito:

[
600 \div 1.000 = 60%
]

A conversão pós-escolha foi de **60%**, com drop-off acumulado de **40%**.

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

Para a instituição financeira, a principal métrica de resultado seria a **conversão da proposta escolhida em crédito liberado — etapa 5 até a 9**. O **drop-off por etapa**, o **tempo para o primeiro contato** e o **Time to Cash** seriam as métricas de diagnóstico para explicar por que essa conversão aumenta ou diminui.

