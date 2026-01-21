# ☁️ Relatório de Implementação de Serviços AWS

**Data:** 21/01/2026  
**Empresa:** QIT Industries  
**Responsável:** Keite Mascena

---

## 1.  Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa **QIT Industries**, realizado por Keite Mascena. O objetivo do projeto foi elencar 4 serviços AWS, com a finalidade de realizar diminuição de custos imediatos e modernizar a infraestrutura de uma distribuidora farmacêutica.

## 2.  Descrição do Projeto (Soluções Propostas)

O foco estratégico é a migração do modelo **CAPEX** (investimento fixo em hardware) para **OPEX** (custo variável por uso).

### Etapa 1: Amazon EC2 Auto Scaling
* **Foco:** Otimização de Recursos Computacionais.
* **Caso de Uso:** A QIT possui picos de acesso apenas em horários específicos. A infraestrutura atual mantém servidores ligados 24h, gerando desperdício na madrugada. O **Auto Scaling** ajustará a capacidade automaticamente (ligando/desligando máquinas) conforme a demanda real.
* **Ganho:** Redução estimada de 40% nos custos de computação ociosa.

### Etapa 2: Amazon S3 Intelligent-Tiering
* **Foco:** Redução de custos de armazenamento e Compliance.
* **Caso de Uso:** O setor farmacêutico exige a guarda de logs e notas fiscais por 5 a 10 anos (Anvisa). Manter esses arquivos "frios" em discos rápidos é caro. O **S3 Intelligent-Tiering** moverá automaticamente arquivos não acessados por 30/90 dias para camadas de arquivamento (Glacier).
* **Ganho:** Economia de até 95% no armazenamento de longo prazo.

### Etapa 3: Amazon RDS (Aurora Serverless)
* **Foco:** Banco de Dados sob demanda.
* **Caso de Uso:** Eliminação de custos fixos com licenciamento de software (Oracle/SQL Server). O banco de dados **Aurora Serverless** ajusta sua capacidade baseado nas transações de estoque e "hiberna" quando não está em uso.
* **Ganho:** Eliminação de custos de licenciamento e redução operacional.

### Etapa 4: AWS Lambda
* **Foco:** Computação sem servidor (Serverless).
* **Caso de Uso:** Para a API de consulta de estoque disponibilizada às farmácias. O **AWS Lambda** cobra apenas pelo tempo de execução (milissegundos) da consulta. Se não houver chamadas, o custo é zero.
* **Ganho:** Custo zero de ociosidade para microsserviços.

---

## 3.  Conclusão e Projeção de Custos

A implementação dessas ferramentas permitirá à QIT Industries sair de um modelo de infraestrutura estática para um modelo elástico.

| Categoria de Custo | Infraestrutura Atual (On-Premise) | Nova Arquitetura (AWS) |
| :--- | :--- | :--- |
| **Modelo Financeiro** | Custo Fixo (CAPEX) | Custo Variável (OPEX) |
| **Manutenção Hardware** | Alto custo anual | Zero (Gerenciado pela AWS) |
| **Armazenamento** | Custo linear e alto | Custo decrescente (Tiering) |
| **Projeção 3 Anos** | ~ R$ 825.000,00 | ~ R$ 380.000,00 |
| **ECONOMIA TOTAL** | — | ** 54% de Redução** |

Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

---

Assinatura do Responsável pelo Projeto:

**Keite Mascena**
