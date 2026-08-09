# Crédito do Trabalhador — Glossário de Órgãos e Termos Técnicos
### O vocabulário que um PM/PO precisa dominar

---

## 1. Os órgãos e empresas envolvidos (quem é quem)

### 🏢 Dataprev
**Nome completo:** Empresa de Tecnologia e Informações da Previdência Social.

**O que é:** uma empresa pública de tecnologia, vinculada ao governo federal. É a "casa de máquinas" por trás do INSS e, agora, também do Crédito do Trabalhador.

**Papel no Crédito do Trabalhador:** é quem **opera tecnicamente a plataforma inteira**. Isso inclui:
- Receber e processar os dados de eSocial e CNIS para calcular a margem consignável
- Registrar (averbar) os contratos
- Disponibilizar as APIs que os bancos usam
- Fazer a conciliação entre o que foi descontado pelas empresas e o que foi repassado pela Caixa
- Homologar e habilitar tecnicamente as instituições financeiras

**Como pensar nisso:** a Dataprev não empresta dinheiro nem decide regras de negócio — ela é a infraestrutura técnica que faz o sistema inteiro conversar (banco ↔ trabalhador ↔ empresa ↔ governo). É comparável a um "provedor de plataforma B2B2C" no jargão de produto.

---

### 🏢 Serpro
**Nome completo:** Serviço Federal de Processamento de Dados.

**O que é:** outra empresa pública de tecnologia do governo federal — irmã "prima" da Dataprev, mas com foco diferente. Enquanto a Dataprev é mais ligada à Previdência/Trabalho, o Serpro historicamente processa dados fiscais, tributários (Receita Federal) e diversos sistemas do governo.

**Papel no Crédito do Trabalhador:** aparece especificamente na **notificação dos empregadores via DET** (Domicílio Eletrônico Trabalhista) — o documento oficial descreve essa notificação como feita "em integração com o Serpro". Ou seja, o Serpro é quem viabiliza tecnicamente o canal de comunicação oficial (DET) entre o governo e o empregador, enquanto a Dataprev cuida da parte de crédito/margem propriamente dita.

**Como pensar nisso:** é um fornecedor de infraestrutura de um pedaço específico do fluxo (notificação/comunicação oficial), não do produto de crédito em si.

---

### 🏦 CAIXA (Caixa Econômica Federal)
**O que é:** banco público federal — um dos maiores bancos do Brasil.

**Papel no Crédito do Trabalhador:** aqui a Caixa **não atua como banco que empresta** (ela pode ser uma das instituições financeiras habilitadas a conceder crédito, mas esse não é seu papel principal no fluxo). O papel documentado é o de **agente financeiro do repasse**: depois que a empresa paga a guia do FGTS Digital com o valor do consignado descontado, é a **Caixa que executa o repasse (TED) desse dinheiro para o banco que emprestou**, em D+2 (2 dias úteis depois do pagamento).

**Detalhe técnico importante:** esse repasse é feito **de forma agrupada por movimento diário**, não vinculado individualmente a cada contrato — por isso os bancos precisam fazer um trabalho de conciliação (cruzar CPF + dados de empregador) para saber exatamente qual repasse corresponde a qual contrato.

**Também relevante:** a Caixa é quem calcula, hoje, o percentual de garantia de verbas rescisórias (fórmula envolvendo a remuneração média do trabalhador) — ou seja, ela participa também da parte de regras de garantias, não só do repasse financeiro puro.

---

### 🏛️ MTE (Ministério do Trabalho e Emprego)
**O que é:** o ministério do governo federal responsável pela regulamentação trabalhista.

**Papel no Crédito do Trabalhador:** é quem **cria as regras do jogo** — publica as Portarias que definem margem, prazos, regras de garantia, critérios de habilitação de bancos. A Dataprev executa tecnicamente o que o MTE regulamenta. Também é o MTE quem analisa e aprova a habilitação de cada instituição financeira antes de ela poder operar.

**Como pensar nisso:** MTE = regulador/dono do produto do ponto de vista de política pública. Dataprev = squad de engenharia/plataforma que constrói e opera. Essa divisão (quem regula vs. quem constrói) é um padrão comum em produtos governamentais.

---

## 2. Termos técnicos do produto

### Averbação / Averbar
**Definição central que você pediu.** Averbar é o ato de **registrar formalmente um contrato de empréstimo na plataforma oficial**, criando a garantia de que aquele desconto vai acontecer na folha de pagamento do trabalhador.

Pense assim: o banco pode até "fechar negócio" com o trabalhador, mas enquanto o contrato não for **averbado**, ele não tem validade operacional dentro do sistema — não vai gerar desconto em folha, não vai aparecer para a empresa, não é reconhecido oficialmente. A averbação é o que transforma uma negociação em uma obrigação registrada e executável.

No Crédito do Trabalhador, a averbação acontece via uma chamada de API específica (`averbar-consignado-trabalhador`), e a partir dela o empréstimo entra no estado **"Ativo"** dentro do sistema.

**Por que existe:** sem esse registro central, poderia haver empréstimos "fantasmas" negociados fora do sistema, sem garantia real de desconto — a averbação é o que dá **segurança jurídica e operacional** de que o desconto realmente vai acontecer.

---

### Remuneração disponível
Não é o mesmo que "salário bruto". É um valor calculado especificamente para fins de consignado: pega o que você recebe de forma habitual (salário, adicionais, comissões) e subtrai descontos como faltas, pensão alimentícia e impostos. É sobre esse valor que se aplica o limite de 35%.

---

### Margem consignável
O valor **máximo em reais** que você pode comprometer por mês com parcelas de consignado — calculado como 35% da remuneração disponível.

---

### Competência
O "mês de referência" de um ciclo operacional. Não é exatamente igual ao mês do calendário — cada competência tem sua própria janela de 30 dias para operações (ex.: a competência de maio é operada entre 21 de março e 20 de abril).

---

### Rubrica
Um **código numérico padronizado** usado no eSocial para identificar o tipo de valor que está sendo lançado na folha de pagamento (salário, desconto de falta, empréstimo consignado etc.). Exemplos que você já viu:
- **9253** — desconto específico do Crédito do Trabalhador
- **9254** — desconto de empréstimo consignado "legado" (o modelo antigo, pré-2025)
- **9201** — Contribuição Previdenciária
- **9203** — Imposto de Renda

Pense na rubrica como uma "tag" ou "categoria" que o sistema usa para saber automaticamente o que fazer com aquele valor.

---

### Instituição consignatária
O nome técnico/formal para o **banco ou fintech habilitado** a oferecer o Crédito do Trabalhador. "Consignatária" vem de "consignado" — é a instituição que recebe o valor consignado (descontado) em folha.

---

### Agente operador de consignações
Termo regulatório (definido na Portaria MTE nº 433/2025) para a entidade que **opera tecnicamente** o sistema de consignações — no caso, é o papel que a Dataprev exerce.

---

### CBC (Código Bancário de Compensação)
Um código numérico que identifica de forma única cada instituição financeira dentro do sistema bancário brasileiro — é como um "CPF" da instituição, usado para saber para qual banco o dinheiro deve ser repassado.

---

### Portabilidade
O direito do trabalhador de **transferir a dívida de um banco para outro**, geralmente buscando uma taxa melhor. O banco original tem um prazo para tentar "segurar" o cliente oferecendo uma condição igual ou melhor antes de perder o contrato.

---

### Refinanciamento
Diferente de portabilidade: aqui você **renegocia com o mesmo banco** — troca o saldo que já pagou por dinheiro novo, geralmente estendendo o prazo de novo.

---

### Tombamento compulsório
Um tipo específico de operação de averbação que acontece de forma "forçada"/automática, geralmente ligada a processos de migração de contratos legados ou situações regulatórias específicas — é uma averbação que não segue o fluxo comercial normal (proposta → escolha → contrato).

---

### CCB (Cédula de Crédito Bancário)
O documento jurídico que formaliza a dívida — é o "contrato" propriamente dito, assinado digitalmente, que serve de prova legal da operação de crédito.

---

## 3. Termos operacionais que um PM/PO precisa ter no vocabulário

| Termo | O que significa aqui |
|---|---|
| **Elegibilidade de vínculo** | Se aquele trabalhador específico pode ou não contratar, com base em regras automáticas (está empregado? tem remuneração recente? já tem empréstimo legado?) |
| **Situação do empréstimo** | O "status" de um contrato dentro do sistema (Ativo, Suspenso, Encerrado, Excluído etc.) — uma máquina de estados |
| **Escrituração** | O ato de a empresa **registrar oficialmente** o desconto no eSocial. Escriturar ≠ pagar — são duas etapas separadas |
| **Repasse** | O dinheiro efetivamente chegando ao banco, depois que a empresa pagou a guia |
| **Conciliação** | O processo de "bater" as informações — confirmar que o que foi escriturado, pago e repassado são, de fato, a mesma coisa |
| **Habilitação** | O processo formal e burocrático que uma instituição financeira precisa passar antes de poder operar no sistema |
| **Homologação** | A fase de testes técnicos que uma instituição precisa passar (100% dos cenários) antes de ir para produção |
| **Legado** | Refere-se a contratos/dados do sistema **antigo** de consignado privado, anterior ao Crédito do Trabalhador — o produto precisou lidar com a migração desses dados |

---

## Resumo visual — quem faz o quê

```
MTE           → Regula (cria as regras / portarias)
Dataprev      → Constrói e opera a plataforma tecnicamente
Serpro        → Viabiliza o canal de notificação oficial (DET)
Empresa       → Executa o desconto na folha
CAIXA         → Repassa o dinheiro descontado ao banco
Banco/Fintech → Empresta o dinheiro e recebe o repasse
```
