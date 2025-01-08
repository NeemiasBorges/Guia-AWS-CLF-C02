# 📚 Anotaçoes AWS Cloud Practitioner

## 📖 Glossário

- **On-premises**: Infraestrutura local, servidores físicos mantidos pela própria empresa
- **ASG (Auto Scaling Group)**: Grupo de auto dimensionamento para gerenciar recursos
- **ELB (Elastic Load Balancing)**: Sistema de balanceamento de carga elástico
- **Autogerido**: Serviço gerenciado pela própria AWS, não open source
- **Infraestrutura**: Conjunto de recursos computacionais, incluindo servidores

### 🏢 Estrutura AWS

**Região**: Conjunto de Zonas de disponibilidade (mínimo 2), geograficamente isoladas.

**Zona de disponibilidade (AZ)**: Data center ou grupo de data centers em uma Região, localizados a dezenas de quilômetros de distância para garantir baixa latência.

**Edge Locations**: Rede de distribuição de conteúdo (CDN) para acelerar a comunicação entre AZs distantes, realizando cache.

  
## 🌟 Introdução a Nuvem AWS

A nuvem é um conjunto de servidores hospedados em uma empresa terceira onde você paga somente pelo que utiliza. Os modelos de implantação podem ser:
- Híbrida (on premises + nuvem)
- 100% Nuvem 
- Local (nuvem privada - virtualização do servidor local)

### 🎯 Critérios para Escolha de Região
- Governança de dados e requisitos legais
- Latência
- Disponibilidade de serviços na região
- Preço (pode variar significativamente, ex: Brasil ~50% mais caro que Virginia)

### 🔄 Tipos de Interação com AWS
- CLI (Console)
- GUI (Interface Web)
- SDK

## 🖥️ Serviços de Computação

### 🚀 EC2 (Elastic Compute Cloud)
Máquinas virtuais dentro de um host compartilhado. Permite total controle sobre os recursos computacionais.

### ⚖️ Elastic Load Balancer (ELB)
Distribui automaticamente o tráfego entre vários recursos. Tipos:
- Application Load Balancer (camada 7 - HTTP/HTTPS)
- Network Load Balancer (camada 4 - TCP)

### 📈 Auto Scaling
Serviço que ajusta automaticamente a capacidade computacional baseado na demanda, aumentando ou reduzindo recursos conforme necessário.

### 💰 Instâncias Spot
Sistema de leilão para máquinas ociosas com desconto de até 90%, porém com possibilidade de interrupção.

## 🌐 Rede

### 🔒 VPC (Virtual Private Cloud)
Rede virtual privada na nuvem, permitindo criar sub-redes públicas e privadas.

### 🌍 Internet Gateway
Conexão entre VPC e internet.

### 🔌 Direct Connect
Conexão física dedicada e privada entre seu datacenter e AWS.

### 🛡️ Security Group
Firewall da rede que controla tráfego. Por padrão:
- Nenhum tráfego de entrada permitido
- Todo tráfego de saída permitido
- Apenas regras de "Permissão"

## 📦 Armazenamento

### 💾 EBS (Elastic Block Store)
Volumes de armazenamento em bloco para EC2. Características:
- Persistente e independente da instância
- Precisa estar na mesma AZ que o EC2
- Backup via Snapshots

### 📂 EFS (Elastic File System)
Sistema de arquivos escalável para Linux, permite montagem em múltiplas instâncias.

### ☁️ S3 (Simple Storage Service)
Armazenamento de objetos com limite de 5TB por arquivo. Classes:
- S3 Standard (acesso frequente)
- S3 Intelligent-Tiering (automático)
- S3 Standard-IA (acesso infrequente)
- S3 One Zone-IA (única AZ)
- Glacier (arquivamento)
- Glacier Deep Archive (arquivamento longo prazo)

## 🎲 Banco de Dados

### 🗄️ RDS (Relational Database Service)
Serviço gerenciado para bancos relacionais, automatiza:
- Provisionamento
- Patches
- Backup
- Configurações

### ⚡ DynamoDB
Banco NoSQL serverless:
- Auto-escalável
- Altamente performático
- Gerenciado pela AWS

### 📊 Redshift
Data warehouse para análise de big data.

## 🔐 Segurança

### 🛡️ Comparativo de Serviços de Segurança

| Serviço | Foco principal | Tipo de Proteção |
|---------|----------------|------------------|
| GuardDuty | Detecção de ameaças | Logs e eventos de segurança |
| Shield | Proteção contra DDoS | Ataques volumétricos |
| Inspector | Verificação de vulnerabilidades | EC2, contêineres |
| Detective | Investigação de incidentes | Análise detalhada |
| Trusted Advisor | Recomendações gerais | Segurança, custo, desempenho |

### 👥 IAM (Identity and Access Management)
Gerenciamento de acessos e identidades:
- Usuários
- Grupos
- Roles
- Policies

### 🛡️ AWS Shield
Proteção contra ataques DDoS:
- Standard (gratuito)
- Advanced (pago, com suporte 24/7)

### 🔍 Amazon Macie
Serviço de segurança que usa machine learning para descobrir e proteger dados sensíveis na AWS.

### 🔍 Detalhamento dos Serviços de Monitoramento e Segurança

- **GuardDuty**: Monitoramento contínuo de possíveis ameaças
- **Inspector**: Realiza varreduras ativas em instâncias EC2
- **CloudTrail**: Monitora ações de APIs e atividades dos serviços
- **Config**: Avalia estado e conformidade das configurações dos recursos

## 📊 Monitoramento e Análise

### 📈 CloudWatch
Monitoramento de recursos AWS:
- Métricas
- Logs
- Alarmes
- Eventos

### 📝 CloudTrail
Registro de atividade da conta AWS:
- Auditoria
- Conformidade
- Análise operacional
- 


## Repositorio Anki de cards para estudo:
- ![Link](https://ankiweb.net/shared/info/59479675)
- ![Link](https://ankiweb.net/shared/info/449552125)
- ![Link](https://ankiweb.net/shared/info/1469596231)

## 💡 Dicas para o Exame

- Mensageria sempre relacionada com algoMQ
- Questões focam bastante em Roles
- Carga de trabalho pode abranger múltiplas contas AWS
- URLs pré-assinadas para acesso a objetos S3
- DocumentDB é compatível com MongoDB para workloads corporativas

## 🎯 Preparação Final
Recomenda-se:
- Realizar diversos simulados
- Agendar exame após atingir >84% nos simulados
- Revisar conceitos principais
- Praticar questões similares

### 🔗 Recursos para Estudo
- [ExamTopics - Simulados](https://www.examtopics.com/exams/amazon/aws-certified-cloud-practitioner-clf-c02/view/)

## 🌟 Considerações Finais
A certificação requer conhecimento abrangente dos serviços AWS e suas interações. Foque em entender os conceitos fundamentais e casos de uso de cada serviço.
