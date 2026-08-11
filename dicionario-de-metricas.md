# Métricas do Crédito Consignado Privado

Como PM, eu dividiria o acompanhamento em quatro perspectivas:

1. **Cliente:** consegue contratar com clareza, rapidez e segurança?
2. **Negócio:** o produto cresce e gera retorno sustentável?
3. **Risco:** a carteira mantém qualidade e perdas controladas?
4. **Operação:** desconto, escrituração, recolhimento e repasse funcionam corretamente?

## 1. Métricas de cliente

| Métrica                            | O que significa e como calcular                                                                                     | Como acompanharia                                                                                                                     |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **Conversão por etapa**            | Percentual que avança de uma etapa para a seguinte. `Usuários que avançaram ÷ usuários que chegaram à etapa × 100`. | Funil diário e semanal, segmentado por canal, dispositivo, banco, versão do app e motivo de erro. Procuraria a etapa com maior queda. |
| **Tempo até receber propostas**    | Tempo entre a solicitação do trabalhador e o recebimento da primeira proposta.                                      | Mediana e percentil 90, além da média. Separaria por instituição e horário para identificar bancos ou integrações lentas.             |
| **Click-to-cash**                  | Tempo entre o início da solicitação e o dinheiro disponível na conta.                                               | Mediana e P90. Decomporia em tempo de proposta, formalização, averbação e desembolso para localizar o gargalo.                        |
| **Taxa de falha biométrica**       | Percentual de tentativas de biometria que não foram concluídas. `Falhas ÷ tentativas × 100`.                        | Em tempo próximo do real, por fornecedor, aparelho, sistema operacional, qualidade da câmera e motivo da falha.                       |
| **CET**                            | Custo total do crédito, incluindo juros, IOF e demais custos incidentes.                                            | Distribuição do CET mensal e anual por instituição, perfil, prazo e canal. Compararia o CET exibido na proposta com o contratado.     |
| **Valor da parcela**               | Valor mensal que será descontado da remuneração.                                                                    | Parcela média e mediana, além da relação `parcela ÷ remuneração disponível`. Monitoraria concentração próxima ao limite da margem.    |
| **CES**                            | Customer Effort Score: mede o esforço percebido pelo cliente para realizar uma tarefa.                              | Pesquisa curta depois de etapas críticas, como simular, comparar propostas ou concluir biometria. Analisaria por etapa e canal.       |
| **CSAT**                           | Customer Satisfaction Score: mede satisfação com uma experiência específica.                                        | Pesquisa após contratação, atendimento ou solução de problema. Exemplo: `% de respostas 4 e 5 em escala de 1 a 5`.                    |
| **NPS**                            | Mede a disposição de recomendar. `Percentual de promotores − percentual de detratores`.                             | Após o desembolso e novamente após algumas parcelas, pois a percepção pode mudar quando começam os descontos.                         |
| **Reclamações**                    | Volume de reclamações relacionadas ao produto.                                                                      | Reclamações por mil ou dez mil contratos, classificadas por motivo, canal, instituição, gravidade, prazo de solução e reincidência.   |
| **Compreensão das condições**      | Mede se o cliente entendeu parcela, CET, total a pagar, prazo, garantias e consequências do desligamento.           | Perguntas objetivas após a proposta ou contratação. Exemplo: percentual de clientes que identifica corretamente o total a pagar.      |
| **Contratos com desconto parcial** | Contratos em que a folha não conseguiu descontar a parcela completa.                                                | `Contratos com desconto parcial ÷ contratos com desconto previsto`. Também acompanharia o valor não descontado e o motivo.            |

### Como interpretar em conjunto

Imagine que a conversão aumentou, mas também cresceram:

* as reclamações;
* a falha de compreensão;
* os descontos parciais;
* a renegociação precoce.

Nesse caso, o aumento de conversão pode representar uma contratação menos saudável, e não uma melhoria real do produto.

---

## 2. Métricas de negócio

| Métrica                     | O que significa e como calcular                                                                   | Como acompanharia                                                                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Volume originado**        | Soma do valor principal dos contratos desembolsados no período.                                   | Diário, semanal e mensal, comparando com períodos anteriores. Segmentar por canal, instituição, prazo, taxa e perfil.                              |
| **Contratos desembolsados** | Quantidade de contratos que concluíram a jornada e tiveram o dinheiro liberado.                   | Acompanharia junto à conversão. O volume pode crescer pelo aumento da quantidade ou do ticket médio.                                               |
| **Ticket médio**            | Valor médio liberado por contrato. `Volume originado ÷ contratos desembolsados`.                  | Por canal, prazo, faixa de renda e instituição. Verificaria se o crescimento vem de poucos contratos muito altos.                                  |
| **Saldo da carteira**       | Soma do principal ainda não amortizado de todos os contratos ativos.                              | Visão mensal do estoque, novas entradas, amortizações, quitações, portabilidades e perdas.                                                         |
| **Prazo médio**             | Quantidade média de parcelas contratadas.                                                         | Média simples e ponderada pelo saldo. Prazos longos podem aumentar receita, mas também exposição ao risco.                                         |
| **Receita de juros**        | Receita financeira reconhecida pela instituição ao longo dos contratos.                           | Mensalmente, separando receita contratada de receita efetivamente reconhecida. Compararia com funding, perdas e custos.                            |
| **Spread**                  | Diferença entre o retorno da carteira e o custo de captação.                                      | Por produto, safra, canal e segmento. Não trataria spread como lucro, pois ainda existem perdas, impostos, operação e capital.                     |
| **Custo de funding**        | Custo que a instituição paga para obter os recursos utilizados nos empréstimos.                   | Taxa média ponderada da captação e sua evolução. Um aumento pode reduzir a rentabilidade mesmo com volume maior.                                   |
| **CAC**                     | Custo de Aquisição de Cliente. `Custos de aquisição ÷ novos clientes ou contratos desembolsados`. | Por canal e campanha. Definiria claramente se o denominador é cliente novo, contrato ou desembolso.                                                |
| **Margem de contribuição**  | Quanto sobra da receita após os custos variáveis diretamente associados à operação.               | Por contrato, canal e safra. A fórmula exata depende da contabilidade interna, mas deve considerar funding, perdas, incentivos e custos variáveis. |
| **Portabilidade**           | Transferência do saldo do contrato entre instituições.                                            | Separaria entrada e saída: contratos recebidos, contratos perdidos, saldo portado, taxa e motivos.                                                 |
| **Quitação antecipada**     | Contratos pagos antes do prazo final.                                                             | `% de contratos quitados antecipadamente` e saldo quitado. Avaliaria se representa satisfação financeira ou perda de competitividade.              |
| **Refinanciamento**         | Reorganização ou substituição do contrato existente por uma nova operação.                        | Volume, quantidade, novo dinheiro liberado, mudança de prazo e taxa e desempenho posterior da nova operação.                                       |

### Exemplo de leitura de negócio

Se o volume originado aumentou 20%, eu perguntaria:

* cresceu a quantidade de contratos ou somente o ticket?
* o CAC aumentou?
* o CET ficou mais competitivo?
* o prazo médio aumentou?
* o risco da nova safra piorou?
* a margem de contribuição continua positiva?

Crescimento sem rentabilidade ou qualidade de carteira pode destruir valor.

---

## 3. Métricas de risco

| Métrica                                 | O que significa e como calcular                                                   | Como acompanharia                                                                                                                         |
| --------------------------------------- | --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Fraude confirmada**                   | Contratos comprovadamente fraudulentos após investigação.                         | `Contratos fraudulentos ÷ contratos desembolsados`. Segmentar por canal, dispositivo, correspondente, tipo de fraude e regra de detecção. |
| **Perda por fraude**                    | Valor financeiro não recuperado em contratos fraudulentos.                        | Valor absoluto e em pontos-base do volume originado: `Perda líquida ÷ volume originado`.                                                  |
| **DPD**                                 | Days Past Due: quantidade de dias que uma obrigação está atrasada.                | Distribuir contratos por faixas: adimplente, 1–30, 31–60, 61–90 e acima de 90 dias.                                                       |
| **DPD30/60/90**                         | Percentual de contratos ou saldo acima de 30, 60 ou 90 dias de atraso.            | Acompanharia por saldo e quantidade, deixando claro o critério interno. Segmentar por safra, canal e motivo do atraso.                    |
| **Inadimplência por safra**             | Compara o desempenho dos contratos originados no mesmo período.                   | Agrupar por mês de desembolso e acompanhar a inadimplência nos meses seguintes. Exemplo: safra de janeiro após 1, 3 e 6 meses.            |
| **Vintage**                             | Método de análise que acompanha cada safra ao longo do tempo.                     | Curvas por mês de originação. Compararia safras antes e depois de mudanças de política, canal ou experiência.                             |
| **Roll rate**                           | Percentual que migra de uma faixa de atraso para outra.                           | Exemplo: saldo que estava em 1–30 dias e passou para 31–60 dias no mês seguinte. Ajuda a prever deterioração.                             |
| **Cure rate**                           | Percentual de contratos atrasados que voltaram a ficar em dia.                    | `Contratos regularizados ÷ contratos atrasados no início do período`. Segmentar por ação de cobrança e motivo.                            |
| **Perda esperada**                      | Estimativa de quanto a carteira pode perder. Simplificadamente: `PD × LGD × EAD`. | Por contrato, safra e segmento. A modelagem pertence à área de Risco, mas o PM deve acompanhar seu impacto nas decisões do produto.       |
| **Provisionamento**                     | Reserva contábil constituída para cobrir possíveis perdas.                        | Valor provisionado e cobertura da carteira problemática. Compararia com inadimplência, perda esperada e recuperação.                      |
| **Renegociação precoce**                | Contratos renegociados pouco tempo depois do desembolso.                          | Definiria uma janela, como os primeiros meses, e acompanharia por safra. Pode indicar parcela inadequada ou concessão pouco sustentável.  |
| **Contratos afetados por desligamento** | Contratos vinculados a trabalhadores cujo vínculo terminou.                       | `Contratos com desligamento ÷ contratos ativos`. Acompanharia saldo, garantias acionadas, redirecionamento e renegociação.                |

### PD, LGD e EAD

| Sigla   | Significado                                                     | Exemplo   |
| ------- | --------------------------------------------------------------- | --------- |
| **PD**  | Probabilidade de o cliente entrar em inadimplência              | 5%        |
| **LGD** | Percentual que seria perdido depois de garantias e recuperações | 40%       |
| **EAD** | Saldo exposto no momento da inadimplência                       | R$ 10.000 |

Exemplo simplificado:

```text
Perda esperada = 5% × 40% × R$ 10.000
Perda esperada = R$ 200
```

### Atenção no consignado

Nem todo pagamento ausente deve ser classificado imediatamente como inadimplência do trabalhador. Pode ser:

* margem insuficiente;
* afastamento sem remuneração;
* desligamento;
* desconto realizado e não escriturado;
* guia não paga pelo empregador;
* falha de repasse;
* falha de baixa no banco.

Por isso, risco e operação precisam ser analisados conjuntamente.

---

## 4. Métricas operacionais

| Métrica                                | O que significa e como calcular                                               | Como acompanharia                                                                                                           |
| -------------------------------------- | ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **Sucesso das APIs**                   | Percentual de requisições concluídas técnica e funcionalmente.                | `Requisições bem-sucedidas ÷ total de requisições`. Separaria erro técnico, timeout e rejeição de negócio.                  |
| **Latência das APIs**                  | Tempo de resposta das integrações.                                            | Mediana, P95 e P99 por serviço. A média pode esconder usuários com tempos muito altos.                                      |
| **Rejeições no eSocial**               | Eventos recusados por erro de cadastro, rubrica, contrato ou leiaute.         | `Eventos rejeitados ÷ eventos enviados`. Quebraria por código de erro, empresa, folha e causa-raiz.                         |
| **Divergência contrato × folha**       | Diferença entre a parcela prevista e o valor processado pela folha.           | Quantidade de registros divergentes e diferença financeira. Classificar como parcial legítimo ou erro.                      |
| **Desconto integral**                  | Folha conseguiu descontar todo o valor previsto.                              | `Contratos com desconto integral ÷ contratos com parcela prevista`.                                                         |
| **Desconto parcial**                   | Folha descontou apenas parte da parcela.                                      | Quantidade, valor não descontado, motivo e reincidência por trabalhador ou empregador.                                      |
| **Desconto não realizado**             | Nenhum valor foi descontado naquela competência.                              | Percentual sobre parcelas previstas, segmentado por ausência de remuneração, afastamento, desligamento ou erro operacional. |
| **Guias pagas no prazo**               | Percentual de guias ou valores quitados antes do vencimento.                  | Por quantidade e valor: `Valor pago no prazo ÷ valor total devido`.                                                         |
| **Divergência descontado × repassado** | Diferença entre o que saiu da folha e o que chegou à instituição financeira.  | Valor absoluto, percentual e tempo em aberto. Usaria uma fila de exceções por competência e contrato.                       |
| **Tempo de conciliação**               | Tempo necessário para confirmar toda a cadeia financeira.                     | Do fechamento da competência até a baixa no banco. Acompanharia mediana e P90.                                              |
| **Incidentes**                         | Falhas que afetam clientes, empregadores ou a operação.                       | Quantidade por gravidade, sistema, causa, recorrência e clientes afetados.                                                  |
| **Cumprimento de SLA**                 | Percentual de incidentes ou solicitações resolvidos dentro do prazo acordado. | `Itens resolvidos no SLA ÷ total de itens`. Separaria por severidade e responsável.                                         |
| **MTTR**                               | Tempo médio para restaurar o serviço ou resolver o incidente.                 | Por tipo e severidade. Acompanharia também reincidência, porque resolver rápido sem eliminar a causa não é suficiente.      |

### API: sucesso técnico não é sucesso de negócio

Uma API pode devolver HTTP 200, mas responder que:

* contrato não foi encontrado;
* margem está indisponível;
* número do contrato é inválido;
* instituição financeira é divergente.

Por isso, eu separaria:

1. disponibilidade técnica;
2. latência;
3. taxa de erro técnico;
4. rejeição de negócio;
5. conclusão real da ação.

---

# Como estruturaria o acompanhamento

## 1. Dashboard executivo

Poucas métricas para mostrar a saúde geral:

* contratos desembolsados;
* volume originado;
* conversão;
* click-to-cash;
* margem de contribuição;
* fraude;
* inadimplência da safra;
* primeira parcela corretamente descontada e conciliada.

Uma boa métrica de resultado operacional poderia ser:

> **Percentual de contratos desembolsados cuja primeira parcela foi descontada, escriturada, recolhida e conciliada corretamente.**

Ela conecta contratação com a execução real do produto.

## 2. Dashboard de funil e experiência

```text
Elegíveis
→ autorização
→ simulação
→ propostas recebidas
→ propostas visualizadas
→ proposta selecionada
→ biometria
→ formalização
→ averbação
→ desembolso
```

Para cada etapa, acompanharia:

* volume;
* conversão;
* abandono;
* erros;
* tempo;
* canal;
* dispositivo;
* instituição financeira.

## 3. Dashboard de operação

```text
Parcela prevista
→ calculada na folha
→ descontada
→ enviada ao eSocial
→ reconhecida no FGTS Digital
→ guia paga
→ repassada
→ baixada no banco
```

Para cada contrato, usaria uma chave com:

* CPF;
* vínculo;
* instituição financeira;
* número do contrato;
* competência;
* valor.

## 4. Dashboard de risco e safra

Acompanharia cada mês de originação como uma safra:

| Safra     |     Mês 1 |     Mês 2 |     Mês 3 |     Mês 6 |
| --------- | --------: | --------: | --------: | --------: |
| Janeiro   | Indicador | Indicador | Indicador | Indicador |
| Fevereiro | Indicador | Indicador | Indicador |         — |
| Março     | Indicador | Indicador |         — |         — |

Isso permite avaliar se uma alteração de jornada, política, canal ou público melhorou a conversão, mas piorou o risco.

---

# Cadência recomendada

| Frequência           | Métricas                                                                     |
| -------------------- | ---------------------------------------------------------------------------- |
| **Tempo real**       | APIs, indisponibilidade, latência, biometria e incidentes críticos           |
| **Diária**           | Funil, conversão, propostas, formalizações, averbações e desembolsos         |
| **Semanal**          | Drop-off, click-to-cash, reclamações, CES, CSAT, erros e fraude              |
| **Mensal**           | Originação, carteira, receita, margem, funding, folha, guias e conciliação   |
| **Mensal por safra** | DPD, vintage, roll rate, cure rate, perda esperada e renegociação            |
| **Trimestral**       | NPS, rentabilidade, estratégia, comportamento da carteira e revisão de metas |

# Ideal

> “Eu acompanharia o consignado em quatro dimensões: cliente, negócio, risco e operação. No cliente, olharia conversão, esforço, tempo e compreensão. No negócio, crescimento da carteira e rentabilidade. Em risco, fraude, inadimplência e comportamento das safras. E, na operação, verificaria se a parcela prevista foi corretamente descontada, escriturada, recolhida e repassada. Não avaliaria nenhuma dessas dimensões isoladamente, porque aumentar a conversão piorando risco, reclamações ou descontos parciais não representa crescimento sustentável.”
