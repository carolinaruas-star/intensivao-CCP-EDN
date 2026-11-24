<div align="center">

# ☁️ Intensivão AWS Certified Cloud Practitioner (CLF-C02)

[![AWS](https://img.shields.io/badge/AWS-Certified%20Cloud%20Practitioner-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/certification/certified-cloud-practitioner/)
[![Escola da Nuvem](https://img.shields.io/badge/Escola%20da%20Nuvem-Intensiv%C3%A3o%20CCP-232F3E?style=for-the-badge)](https://escoladanuvem.org/)
[![Markdown](https://img.shields.io/badge/Formato-Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)](https://www.markdownguide.org/)
[![Status](https://img.shields.io/badge/Status-Em%20Andamento-10B981?style=for-the-badge)](#cronograma-do-intensivão)

Repositório de anotações, resumos detalhados, listas de revisão, simulado e cronograma de estudos para a certificação **AWS Certified Cloud Practitioner (CLF-C02)** pela **Escola da Nuvem**.

</div>

---

## 🎯 Sobre o Repositório

Este repositório reúne o material de revisão e estudo estruturado a partir das aulas do **Intensivão AWS Certified Cloud Practitioner (CLF-C02)** da **Escola da Nuvem**, ministradas pelo instrutor **Anderson Buquer** com moderação/apoio da equipe (como **Carry** e a coordenadora **Jaqueline**).

O objetivo é consolidar os conceitos fundamentais, serviços *core*, princípios arquiteturais, boas práticas de segurança, governança e custos para a prova oficial.

---

## 📋 Visão Geral do Exame (CLF-C02)

* **Quantidade de questões:** 65 questões (múltipla escolha e múltipla resposta — atenção às questões que pedem mais de uma alternativa correta).
* **Pontuação:** 50 questões contam para a nota e 15 questões não são avaliadas (não identificadas durante a prova; recomenda-se responder todas com atenção).
* **Documento de referência:** Guia oficial do exame (*Exam Guide*, incluindo o *Appendix* com lista de serviços e conceitos) e documentação oficial da AWS.

### Domínios e Pesos na Prova

| Domínio | Tema | Peso no Exame |
| :--- | :--- | :---: |
| **Domínio 1** | Conceitos de Nuvem | **24%** |
| **Domínio 2** | Segurança e Conformidade | **30%** |
| **Domínio 3** | Tecnologia e Serviços da Nuvem | **34%** |
| **Domínio 4** | Cobrança, Preços e Suporte | **12%** |

---

## 📚 Conteúdo e Arquivos de Estudo

### 1. Resumo — Aula 1: Conceitos de Nuvem (`aula_01_conceitos_nuvem.md`)
* **Estrutura e estratégia do exame:** *Exam Guide*, *Appendix*, pirâmide invertida das certificações AWS e pesos dos domínios.
* **Panorama de serviços *core*:** Computação (EC2, EC2 Auto Scaling, Elastic Beanstalk, Lambda), Redes e Entrega de Conteúdo (VPC, Route 53, CloudFront, Elastic Load Balancing), Monitoramento e Governança (CloudWatch, Trusted Advisor, CloudFormation, Config, CloudTrail), Bancos de Dados (RDS, Aurora, DynamoDB, Redshift), Segurança e Conformidade (IAM, WAF, Shield, Artifact), Custos (Pricing Calculator, Cost Explorer, Budgets) e Armazenamento (S3, S3 Glacier, EBS, família Snow — com nota sobre a descontinuação do Snowmobile e serviços que saíram do exame).
* **Definição e vantagens da nuvem:** Entrega sob demanda via internet, troca de *CapEx* por *OpEx*, economias de escala, fim do "achismo" de capacidade, velocidade e agilidade, foco no negócio/cliente e atuação global.
* **Modelos de serviço:** *On-premises*, *IaaS*, *PaaS* e *SaaS* (incluindo a analogia da pizza), além de recursos gerenciados vs. não gerenciados.
* **Infraestrutura global:** Regiões, Zonas de Disponibilidade (*AZs*) e Pontos de Presença (*Edge Locations*).
* **AWS Well-Architected Framework:** Os 6 pilares (*Excelência Operacional*, *Segurança*, *Confiabilidade*, *Eficiência de Performance*, *Otimização de Custos* e *Sustentabilidade*), princípios de design e conceito de baixo acoplamento.
* **AWS Cloud Adoption Framework (CAF):** Estratégia de adoção à nuvem e as 6 perspectivas (*Negócios*, *Pessoas*, *Governança*, *Plataforma*, *Segurança* e *Operações*).
* **Conexão e acesso:** Console, CLI e SDKs; diferença entre *autenticação* e *autorização*.
* **Aprofundamento em Amazon EC2:** Anatomia do nome da instância (`tipo` + `geração` = `família` + `.tamanho`), categorias (*Uso Geral*, *Otimizadas para Computação*, *Otimizadas para Memória*, *Otimizadas para Armazenamento*), *Free Tier* e cobrança sob demanda (mínimo de 60s para Linux e cobrança por hora para Windows).

### 2. Resumo — Aula 2: Segurança e Conformidade (`aula_02_seguranca_conformidade.md`)
* **Modelo de Responsabilidade Compartilhada:** Divisão entre segurança *da* nuvem (AWS: infraestrutura física, hardware, regiões, AZs, *edge locations*) e segurança *na* nuvem (cliente: dados, aplicações, identidades/acessos, SO/rede conforme o serviço).
* **AWS IAM:** Serviço gratuito a nível de conta; usuários, grupos (não aninhados) e *roles* (acesso temporário sem credenciais permanentes); políticas em JSON (`Effect`, `Action`, `Resource`, `Principal`); boas práticas (não usar o usuário `root` no dia a dia, aplicar *privilégio mínimo* e habilitar *MFA*).
* **Proteção de aplicações e DDoS:** **AWS WAF** (Camada 7, bloqueio por regras/países/taxa) e **AWS Shield** (*Standard* gratuito na conta vs. *Advanced* com suporte 24/7 e proteção ampliada).
* **Monitoramento, auditoria e conformidade:** **Amazon CloudWatch** (métricas, logs, alarmes, dashboards), **AWS CloudTrail** (registro de chamadas de API/auditoria a nível de conta), **AWS Config** (registro e avaliação de configurações de recursos, regional), **AWS Organizations** (*consolidated billing*, *OUs* e *SCPs*, global) e **AWS Artifact** (relatórios e certificações sob demanda, como SOC, PCI/cartões de crédito e ISO).
* **AWS Trusted Advisor:** Recomendações em otimização de custos, desempenho, segurança, tolerância a falhas, limites de serviço e excelência operacional (com variação conforme o plano de suporte).

### 3. Lista de Exercícios de Revisão — BRSAO (`exercicios_revisao_brsao.md`)
* Lista com **27 questões** formatadas com caixas de seleção (`[ ]`) para marcação e gabarito comentado cobrindo Responsabilidade Compartilhada, modelos de serviço, Amazon S3 e suas classes de armazenamento, Amazon EC2, volumes persistentes vs. temporários e modelos de compra.

### 4. Simulado AWS Certified Cloud Practitioner (CLF-C02)
* Simulado com **49 questões** abordando *Reserved Instances* conversíveis, planos de suporte (ex.: *Developer*), alocação de custos por marcação de recursos, *AWS Artifact*, *CloudTrail*, *Config*, *Macie*, *Shield Advanced*, *IAM roles*, usuário *root*, *CodePipeline*, *Route 53*, *EBS*, *Multi-AZ* no RDS, *Redshift*, *Control Tower*, *Transit Gateway*, *Elastic Load Balancing*, *ECS*, *Trusted Advisor*, *Snowball*, *Internet Gateway*, *Well-Architected Framework*, elasticidade e tolerância a falhas.

---

## 🗓️ Cronograma do Intensivão

| Data | Modalidade / Etapa | Atividade | Horário |
| :--- | :--- | :--- | :--- |
| 11 de Novembro de 2026 | Online | Onboard | 19h às 22h |
| 17 de Novembro de 2026 | Síncrona 1 | Revisão intensiva 1 | 19h às 22h |
| 18 de Novembro de 2026 | Assíncrono | Material de estudo e questões | - |
| 19 de Novembro de 2026 | Síncrona 2 | Revisão intensiva 2 | 19h às 22h |
| 20 de Novembro de 2026 | Assíncrono | Material de estudo | - |
| 23 de Novembro de 2026 | Assíncrono | Material de estudo | - |
| 24 de Novembro de 2026 | Síncrona 3 | Revisão intensiva 3 | 19h às 22h |
| 25 de Novembro de 2026 | Assíncrono | Material de estudo | - |
| 26 de Novembro de 2026 | Síncrona 4 | Revisão final | 19h às 22h |
| 27 de Novembro de 2026 | Simulado | Revisão individual e simulado final | - |
| 30 de Novembro de 2026 | Marco | Distribuição dos vouchers | - |
| 1 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 2 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 3 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 4 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 7 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 8 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 9 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 10 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 11 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 14 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 15 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 16 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 17 de Dezembro de 2026 | Individual | Realização da certificação AWS | - |
| 18 de Dezembro de 2026 | Marco | Prazo final para certificação | - |

---

<div align="center">

Anotações de estudo — **AWS Certified Cloud Practitioner (CLF-C02)** ☁️📚 

Rumo à certificação! 🚀

</div>