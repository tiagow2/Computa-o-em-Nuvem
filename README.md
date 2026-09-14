# COMPUTAÇÃO EM NUVEM I
## Atividade de Pesquisa e Prática: Contextualização, Modelos de Implantação, Características, Desafios e Modelos de Serviço em Nuvem

---

### DADOS DE IDENTIFICAÇÃO

- **Aluno(a):** Tiago
- **Turma / Curso:** Computação em Nuvem I / Sistemas de Informação
- **Data de Entrega:** 14/09/2026
- **Formato de Entrega:** Relatório Técnico-Acadêmico e Prático com Evidências de Publicação

---

# PARTE 1 — ATIVIDADE TEÓRICA (PESQUISA DIRIGIDA)

---

## BLOCO 1 — CONTEXTUALIZAÇÃO E MODELOS DE IMPLANTAÇÃO

### 1. O que caracteriza um sistema de computação em nuvem em comparação com a infraestrutura de TI tradicional (on-premise)? Cite pelo menos três diferenças.

**Resposta:**

A **computação em nuvem** é definida formalmente pelo *National Institute of Standards and Technology* (NIST SP 800-145) como um modelo que viabiliza o acesso onipresente, conveniente e sob demanda por meio de rede a um conjunto compartilhado de recursos de computação configuráveis (como servidores, armazenamento, redes e aplicações), os quais podem ser provisionados e liberados com rapidez e esforço mínimo de gerenciamento ou interação com o provedor.

Em contrapartida, a **infraestrutura de TI tradicional (*on-premise*)** baseia-se na aquisição, instalação, operação e custódia física direta de ativos de hardware em um data center proprietário mantido pela própria empresa.

As três principais diferenças estruturais são:

1. **Modelo Financeiro e Alocação de Recursos (CapEx vs. OpEx):**
   - *TI Tradicional (CapEx):* Exige vultoso investimento inicial de capital (*Capital Expenditure*) na compra de servidores físicos, licenças perenes de software, switches de rede, no-breaks, geradores a diesel e sistemas de climatização. Esse dimensionamento precisa ser feito com base no pico histórico projetado para 3 a 5 anos, resultando em frequente ociosidade de infraestrutura cara.
   - *Computação em Nuvem (OpEx):* Opera quase integralmente como despesa operacional (*Operational Expenditure*), adotando o modelo financeiro de pagamento conforme o consumo (*pay-as-you-go*). A organização não imobiliza capital em ativos que depreciam e paga apenas pelo tempo de processamento, armazenamento e tráfego de dados efetivamente utilizados.
2. **Tempo de Provisionamento e Elasticidade:**
   - *TI Tradicional:* O processo de expansão de capacidade envolve cotações de fornecedores, compras, desembaraço fiscal, entrega logística, montagem em rack, cabeamento e homologação — um ciclo que comumente leva de semanas a meses.
   - *Computação em Nuvem:* A alocação de novos recursos é elástica, instantânea e programável. Novas instâncias de computação ou dezenas de gigabytes de armazenamento são provisionados em segundos ou poucos minutos por meio de chamadas de API, scripts de Infraestrutura como Código (IaC) ou consoles web.
3. **Escopo de Responsabilidade Operacional e Manutenção Física:**
   - *TI Tradicional:* A equipe interna de TI é integralmente responsável por todas as camadas: segurança perimetral do data center, manutenção preventiva e corretiva de hardware físico, substituição de discos danificados, redundância elétrica, firmware de placas-mãe e hipervisores.
   - *Computação em Nuvem:* O provedor assume a gestão, manutenção física, resiliência energética e segurança da infraestrutura de base (o que o NIST chama de *underlying physical infrastructure*). Isso libera a equipe corporativa para direcionar seu foco e energia intelectual ao desenvolvimento de produtos, regras de negócio e inovação.

*Fontes primárias consultadas:*
- MELL, Peter; GRANCE, Timothy. *The NIST Definition of Cloud Computing*. NIST Special Publication 800-145, Gaithersburg, 2011. Disponível em: <https://doi.org/10.6028/NIST.SP.800-145>.
- AMAZON WEB SERVICES. *What is Cloud Computing?*. AWS Documentation, 2024. Disponível em: <https://aws.amazon.com/what-is-cloud-computing/>.

---

### 2. Defina, com suas palavras, nuvem pública, nuvem privada e nuvem híbrida. Para cada uma, apresente um exemplo real de provedor ou de caso de uso corporativo.

**Resposta:**

- **Nuvem Pública:**
  - *Definição:* É uma infraestrutura de computação em nuvem de propriedade de um provedor especializado externo, disponibilizada para uso amplo de pessoas físicas ou organizações de diferentes segmentos. Os recursos físicos (servidores, redes e armazenamento) são compartilhados entre múltiplos clientes (*multi-tenant*), mas isolados logicamente por meio de virtualização e criptografia.
  - *Exemplo de Provedor e Caso Real:* **Amazon Web Services (AWS)**. A **Netflix** é um caso emblemático de uso corporativo de nuvem pública: ela fechou completamente seus data centers físicos e migrou todo o seu ecossistema de processamento de vídeos, microsserviços de recomendação e autenticação de usuários para a AWS, aproveitando a capacidade de escala global e presença geográfica do provedor.
- **Nuvem Privada:**
  - *Definição:* É a infraestrutura de computação em nuvem operada e destinada ao uso exclusivo de uma única organização, com múltiplos departamentos e equipes internas atuando como consumidores. Pode ser instalada fisicamente dentro do data center da própria instituição (*on-premise*) ou hospedada externamente por um terceiro em regime de locação dedicada (*single-tenant*), oferecendo controle irrestrito sobre hardware, segurança e governança de dados.
  - *Exemplo de Provedor e Caso Real:* **Red Hat OpenStack Platform** ou **VMware Cloud Foundation**. Um grande banco de investimentos (como o **Itaú Unibanco** ou **JPMorgan Chase**) adota nuvem privada em seus data centers próprios certificados para abrigar sistemas de liquidação financeira de câmbio e processamento de contas bancárias protegidas por sigilo bancário estrito.
- **Nuvem Híbrida:**
  - *Definição:* É a composição arquitetural que conecta de maneira interoperável duas ou mais infraestruturas de nuvem distintas (privadas, públicas ou comunitárias), as quais permanecem como entidades independentes, mas são integradas por meio de tecnologias padronizadas de rede segura, orquestração e portabilidade de dados e aplicações.
  - *Exemplo de Provedor e Caso Real:* **Microsoft Azure Arc** ou **AWS Outposts**. Um grande hospital ou laboratório de diagnósticos por imagem que mantém o banco de dados principal de prontuários eletrônicos em sua nuvem privada interna (atendendo à LGPD e à baixa latência para equipamentos médicos), enquanto utiliza a nuvem pública (Microsoft Azure) para disponibilizar o portal web e aplicativo móvel de agendamento e entrega de laudos aos pacientes.

*Fontes primárias consultadas:*
- MELL, P.; GRANCE, T. *NIST SP 800-145*, 2011 (Seções 2.3 Deployment Models).
- MICROSOFT LEARN. *What is a public cloud, private cloud, and hybrid cloud?*. Microsoft Azure Documentation, 2024. Disponível em: <https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/get-started/cloud-concepts>.

---

### 3. Em que situações uma organização optaria por uma nuvem híbrida em vez de uma nuvem pública pura? Utilize como referência um setor fortemente regulado (por exemplo, bancário, saúde ou governo) e explique o motivo da escolha.

**Resposta:**

Uma organização opta pela **nuvem híbrida** quando se depara com a necessidade concomitante de: (a) garantir conformidade regulatória severa, soberania e isolamento físico de dados críticos; e (b) usufruir da escalabilidade, agilidade de inovação e amplitude de serviços que apenas a nuvem pública proporciona.

**Cenário de Referência: Setor Bancário / Financeiro**
Instituições financeiras operam sob estrita regulação do Banco Central do Brasil (notadamente as **Resoluções CMN nº 4.893/2021 e nº 4.658/2018** sobre segurança cibernética e contratação de serviços de processamento em nuvem), além da Lei Complementar nº 105/2001 (Sigilo Bancário) e da Lei nº 13.709/2018 (LGPD).

**Motivos técnicos e de negócio para a escolha da Nuvem Híbrida:**
1. **Soberania e Custódia de Chaves Criptográficas e Core Banking:** Os sistemas centrais de conciliação financeira, livros de transações correntes e módulos de segurança física em hardware (*Hardware Security Module - HSM*) são mantidos na nuvem privada do banco. Isso garante auditoria irrestrita, retenção do controle físico das chaves mestras e conformidade direta com inspeções regulatórias do Bacen.
2. **Latência Ultrabaixa e Resiliência Local:** A infraestrutura de terminais de atendimento em agências e compensação de ordens em bolsas de valores depende de comunicações de rede locais com latência de milissegundos mínimos, não podendo ficar vulnerável a oscilações de rotas da internet pública.
3. **Elasticidade em Canais Digitais e Inteligência Artificial na Nuvem Pública:** Ao mesmo tempo, o banco enfrenta picos massivos e imprevisíveis de acessos no aplicativo móvel em dias de pagamento de salários, início de mês e promoções como a Black Friday. Na nuvem híbrida, a camada de atendimento móvel, *frontend* bancário, processamento analítico de *Big Data* e modelos generativos de IA para suporte ao cliente rodam na nuvem pública, conectando-se à nuvem privada de forma segura por meio de conexões dedicadas criptografadas (*AWS Direct Connect* ou *Azure ExpressRoute* com VPN IPsec redundante).

Assim, a nuvem híbrida une o melhor dos dois mundos: **custódia estrita do dado regulado** internamente e **escalabilidade elástica de canais digitais** externamente.

*Fontes primárias consultadas:*
- BANCO CENTRAL DO BRASIL. *Resolução CMN nº 4.893, de 26 de fevereiro de 2021*. Dispõe sobre a política de segurança cibernética e sobre os requisitos para a contratação de serviços de processamento e armazenamento de dados e de computação em nuvem a serem observados pelas instituições financeiras. Disponível em: <https://www.bcb.gov.br/estabilidadefinanceira/exibenormativo?tipo=Resolu%C3%A7%C3%A3o%20CMN&numero=4893>.

---

### 4. Pesquise o conceito de "nuvem comunitária" (community cloud). Ele é reconhecido pela definição oficial do NIST? Em que esse modelo se diferencia da nuvem privada?

**Resposta:**

**Sim**, o conceito de **nuvem comunitária (*community cloud*)** é expressamente reconhecido e formalizado pela publicação oficial do NIST (**NIST SP 800-145**, Seção 2.3).

O NIST define a nuvem comunitária como:
> *"A infraestrutura de nuvem é provisionada para uso exclusivo de uma comunidade específica de consumidores pertencentes a organizações que compartilham preocupações em comum (por exemplo, missão, requisitos de segurança, conformidade de políticas e regulamentações). Pode pertencer, ser gerenciada e operada por uma ou mais organizações da comunidade, por um terceiro ou por uma combinação deles, e pode residir dentro ou fora de suas instalações."*

**Diferenciação em relação à Nuvem Privada:**

| Critério de Comparação | Nuvem Privada (*Private Cloud*) | Nuvem Comunitária (*Community Cloud*) |
| :--- | :--- | :--- |
| **Escopo de Atendimento** | Exclusiva para **uma única organização** (embora atenda múltiplos departamentos internos). | Compartilhada entre **duas ou mais organizações distintas e independentes**, unidas por propósitos ou regulações comuns. |
| **Governança e Tomada de Decisão** | Centralizada sob a diretoria e políticas exclusivas da empresa proprietária. | Colegiada ou regulamentada por consórcios, termos de cooperação ou acordos multilaterais entre as entidades participantes. |
| **Rateio de Custos** | Custos operacionais e de capital são arcados integralmente pela única organização proprietária. | Custos de infraestrutura, links de alta capacidade e segurança são divididos e rateados entre os entes da comunidade. |
| **Exemplo Prático** | Data center próprio de uma empresa de logística para seus sistemas internos. | O **GovCloud** ou consórcios de hospitais universitários de pesquisa genética que compartilham poder computacional e datasets genômicos protegidos sob normas idênticas de ética e sigilo. |

*Fontes primárias consultadas:*
- MELL, P.; GRANCE, T. *The NIST Definition of Cloud Computing*. NIST SP 800-145, p. 3, 2011.

---

## BLOCO 2 — AS CINCO CARACTERÍSTICAS ESSENCIAIS (NIST)

### 5. Tabela Conceitual e Exemplificação Prática das 5 Características

| Característica Essencial (NIST) | Explicação Conceitual (com palavras próprias) | Exemplo Real em Provedor e Documentação Oficial |
| :--- | :--- | :--- |
| **Autoatendimento sob demanda** (*On-demand self-service*) | Capacidade do usuário final solicitar, configurar e inicializar recursos computacionais (CPUs, memória, discos e regras de rede) unilateralmente e de forma imediata, sem necessidade de enviar tickets manuais, falar com atendentes comerciais ou aguardar aprovação de operadores humanos do provedor. | **AWS EC2 (Elastic Compute Cloud):** O usuário pode inicializar uma instância virtual em menos de 60 segundos por meio da AWS Management Console, do comando de terminal `aws ec2 run-instances` (AWS CLI) ou de scripts de automação via Terraform.<br>*Ref.:* AWS EC2 Docs — *Launch an instance* (https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/LaunchingAndUsingInstances.html). |
| **Amplo acesso à rede** (*Broad network access*) | Os serviços da nuvem encontram-se disponíveis pela rede de telecomunicações através de protocolos de comunicação universais e padronizados (ex.: HTTP/HTTPS, TLS, REST), viabilizando o consumo a partir de múltiplos dispositivos heterogêneos (*smartphones*, *tablets*, *desktops*, clientes web ou terminais de linha de comando). | **Microsoft 365 / Google Workspace:** Usuários editam documentos, planilhas e colaboram em tempo real por meio de navegadores web em desktops Linux/Windows/Mac, bem como através de aplicativos nativos móveis em Android e iOS, mantendo a sincronia contínua de dados pela nuvem.<br>*Ref.:* Google Workspace Admin Help — *System Requirements* (https://support.google.com/a/answer/33864). |
| **Pool de recursos** (*Resource pooling*) | Os ativos de hardware do provedor (chips de processamento, memória RAM, discos rígidos e interfaces de rede) são consolidados em um grande conjunto compartilhado dinamicamente entre múltiplos inquilinos (*multi-tenancy*). Os clientes usufruem de isolamento lógico estrito sem saber em qual máquina física exata seus dados estão sendo executados. | **Isolamento no AWS Nitro System e Azure Hyper-V:** A AWS descreve que a segregação física/lógica de clientes é garantida por hardware customizado (*Nitro Cards*) que descarrega a virtualização da CPU hospedeira, impedindo acesso de memória entre instâncias de diferentes clientes. No Azure, redes virtuais (*VNets*) utilizam encapsulamento VxLAN para garantir que o tráfego de um cliente nunca vaze para outro no mesmo switch físico.<br>*Ref.:* AWS Security Whitepaper — *Compute Isolation* (https://docs.aws.amazon.com/whitepapers/latest/aws-overview-security-processes/compute-isolation.html). |
| **Elasticidade rápida** (*Rapid elasticity*) | A infraestrutura pode ser expandida (*scale-out*) ou reduzida (*scale-in*) de maneira ágil, automática e contínua, acompanhando diretamente as flutuações de demanda do sistema. Para o cliente consumidor, a capacidade computacional disponível aparenta ser inesgotável e pode ser contratada na quantidade exata no momento em que for demandada. | **Azure Virtual Machine Scale Sets (VMSS) / AWS Auto Scaling:** Mecanismos que monitoram métricas em tempo real (como consumo de CPU > 70%) e disparam a inicialização automática de dezenas de novas máquinas virtuais e containers para suportar o pico, destruindo-os de volta quando o tráfego diminui.<br>*Ref.:* Azure Docs — *Overview of autoscale in Microsoft Azure* (https://learn.microsoft.com/en-us/azure/azure-monitor/autoscale/autoscale-overview). |
| **Serviço mensurável** (*Measured service*) | O provedor monitora, afere e registra com alta granularidade o uso real de cada unidade de recurso computacional consumido pelo cliente. Esse controle transparente viabiliza o modelo de cobrança por uso (*pay-as-you-go*), no qual o cliente recebe faturas detalhadas sobre o consumo estrito gerado. | **AWS Billing & CloudWatch / Azure Cost Management:** Exemplos claros de métricas métricas de cobrança: tempo de execução de máquina virtual faturado por segundo (ex.: vCPU/hora da instância EC2 t3.medium), volume de dados mantidos no mês em Gigabytes (ex.: GB-mês no Amazon S3) e quantidade de requisições de API executadas (ex.: faturamento por milhão de invocações no AWS Lambda).<br>*Ref.:* AWS Pricing Principles (https://aws.amazon.com/pricing/). |

---

### 6. Passo a Passo de Configuração de Auto Scaling a partir de Documentação Oficial

**Provedor Escolhido:** Amazon Web Services (AWS)  
**Recurso:** *Auto Scaling Group (ASG)* com Instâncias EC2  
**Link da Documentação Consultada:** <https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-asg-launch-template.html>

#### Passo a Passo Técnico:

1. **Criação do Launch Template (Modelo de Inicialização):**
   - Acesse o Console da AWS e navegue até **EC2 > Launch Templates > Create launch template**.
   - Defina o nome do modelo (ex.: `web-app-template-v1`).
   - Selecione a imagem de máquina (*Amazon Machine Image - AMI*), por exemplo: *Amazon Linux 2023 AMI* ou *Ubuntu Server 22.04 LTS*.
   - Escolha o tipo de instância (ex.: `t3.micro`).
   - Associe o par de chaves de acesso SSH e selecione um *Security Group* com permissão de entrada nas portas 80 (HTTP) e 443 (HTTPS).
   - No campo de metadados avançados (*User Data*), insira o script de inicialização do servidor web (ex.: script para instalar Nginx e servir a aplicação).
2. **Inicialização da Criação do Grupo de Auto Scaling:**
   - No painel esquerdo do EC2, acesse **Auto Scaling Groups** e clique em **Create Auto Scaling group**.
   - No Passo 1, dê um nome ao grupo (ex.: `asg-hospital-frontend`) e vincule o *Launch Template* configurado no item anterior.
3. **Seleção de Rede e Zonas de Disponibilidade (Alta Disponibilidade):**
   - No Passo 2, selecione a VPC (*Virtual Private Cloud*) de destino.
   - Selecione ao menos duas sub-redes distintas localizadas em **Zonas de Disponibilidade (AZs) diferentes** (ex.: `sa-east-1a` e `sa-east-1b` em São Paulo), garantindo resiliência geográfica física contra panes em data centers individuais.
4. **Integração com Balanceador de Carga (Opcional, porém Recomendado):**
   - No Passo 3, selecione a opção **Attach to an existing load balancer** ou crie um *Application Load Balancer (ALB)* para distribuir as requisições HTTP entre as instâncias criadas pelo grupo.
   - Habilite os *Elastic Load Balancing Health Checks* para que instâncias com falha de resposta de aplicação sejam automaticamente substituídas.
5. **Definição dos Limites de Capacidade (Group Size):**
   - No Passo 4, defina os parâmetros fundamentais de dimensionamento do grupo:
     - **Capacidade Desejada (*Desired Capacity*):** `2` instâncias (número de servidores mantidos em condições normais de tráfego).
     - **Capacidade Mínima (*Minimum Capacity*):** `2` instâncias (garantia de disponibilidade mínima tolerante a falhas).
     - **Capacidade Máxima (*Maximum Capacity*):** `10` instâncias (teto máximo para impedir estouro orçamentário).
6. **Configuração da Política de Escalonamento Automático (*Automatic Scaling Policy*):**
   - Escolha a modalidade **Target Tracking Scaling Policy** (política de rastreamento de metas).
   - Defina a métrica de monitoramento: **Utilização Média de CPU (*Average CPU Utilization*)**.
   - Defina o valor-alvo (*Target Value*): `60%`.
   - *Comportamento resultante:* O serviço provisionará internamente alarmes no Amazon CloudWatch. Se o consumo médio de CPU do grupo ultrapassar 60% por período contínuo configurado, o Auto Scaling disparará o provisionamento de novas instâncias (*scale-out*). Quando o uso cair de volta, o serviço encerrará gradativamente as instâncias excedentes (*scale-in*).
7. **Revisão e Criação do Grupo:**
   - Revise o resumo de tags, notificações (SNS) e configurações.
   - Clique em **Create Auto Scaling group**. Imediatamente, o serviço iniciará a execução das instâncias desejadas no painel.

---

## BLOCO 3 — DESAFIOS DA COMPUTAÇÃO EM NUVEM

### 7. Segurança: Três principais ameaças em nuvem e mitigações

Segundo o levantamento de referência internacional da *Cloud Security Alliance (CSA)* (*Top Threats to Cloud Computing*):

1. **Ameaça 1: Configurações Incorretas de Segurança e Gestão Inadequada de Recursos (*Misconfiguration*)**
   - *Descrição:* É historicamente a principal causa de vazamento de dados em nuvem. Ocorre quando serviços e buckets de armazenamento (como AWS S3 ou Azure Blob Storage) são criados com permissões de leitura pública inadvertidamente, ou quando regras de firewall em nuvem (*Security Groups*) mantêm portas críticas de gerenciamento (ex.: SSH na porta 22 ou RDP na porta 3389) abertas irrestritamente para a internet (`0.0.0.0/0`).
   - *Controle / Prática de Mitigação:* Implementação contínua de plataformas de **CSPM (*Cloud Security Posture Management*)** como AWS Security Hub ou Microsoft Defender for Cloud, auditorias automatizadas com ferramentas de Infraestrutura como Código (*Checkov, tfsec* nos pipelines de CI/CD) e aplicação de políticas de guarda (*AWS Service Control Policies - SCPs*) que bloqueiem a criação de recursos públicos por padrão.
2. **Ameaça 2: Fragilidade no Gerenciamento de Identidades, Credenciais e Acessos (*Identity and Access Management - IAM Failure*)**
   - *Descrição:* Comprometimento de credenciais em virtude da ausência de autenticação multifator (MFA), senhas fracas, chaves de API permanentes codificadas (*hardcoded*) dentro de repositórios Git públicos ou concessão indiscriminada de privilégios de superusuário (*admin/root* com regras coringa `*.*`).
   - *Controle / Prática de Mitigação:* Aplicação estrita do **Princípio do Menor Privilégio (*Principle of Least Privilege*)** com papéis temporários (*IAM Roles / AWS STS*) em vez de chaves estáticas; imposição obrigatória e inegociável de **Autenticação Multifator (MFA)** para todos os acessos humanos e uso de cofres centralizados de segredos com rotação automática (*AWS Secrets Manager / Azure Key Vault*).
3. **Ameaça 3: Interfaces e APIs Inseguras (*Insecure Interfaces and APIs*)**
   - *Descrição:* Os sistemas de controle e os pontos de contato da nuvem operam inteiramente por meio de APIs HTTP/REST. APIs mal projetadas, desprovidas de autenticação robusta, sem validação de parâmetros de entrada ou sem controle de taxa de requisições, tornam-se vetores fáceis para injeção de código, ataques de negação de serviço (DDoS) e exfiltração de dados confidenciais.
   - *Controle / Prática de Mitigação:* Implantação de **API Gateways** centrais para validação de esquemas, exigência de autenticação e autorização criptográfica moderna via tokens OAuth 2.0 / OpenID Connect (JWT), imposição de tráfego exclusivo com **TLS 1.3** e proteção perimetral por **WAF (*Web Application Firewall*)** com limitação de requisições (*rate-limiting*).

*Fonte primária:* CLOUD SECURITY ALLIANCE (CSA). *Top Threats to Cloud Computing*. CSA Research, 2024. Disponível em: <https://cloudsecurityalliance.org/research/top-threats/>.

---

### 8. Privacidade: Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)

Ao armazenar e tratar dados pessoais de titulares brasileiros em infraestruturas de computação em nuvem, as organizações devem cumprir obrigações mandatórias prescritas na LGPD:

- **Obrigação 1: Adoção de medidas técnicas e de segurança adequadas para proteção de dados (Art. 46):**
  > *Art. 46. Os agentes de tratamento devem adotar medidas de segurança, técnicas e administrativas aptas a proteger os dados pessoais de acessos não autorizados e de situações acidentais ou ilícitas de destruição, perda, alteração, comunicação ou qualquer forma de tratamento inadequado ou ilícito.*
  - *Aplicação Prática na Nuvem:* As empresas contratantes são legalmente obrigadas a assegurar que os serviços em nuvem possuam criptografia em repouso (usando algoritmos consolidados como AES-256) e em trânsito (TLS 1.3), controles estritos de controle de acesso lógico baseados em função (RBAC), logs auditáveis de acesso aos dados e planos de continuidade com backups imutáveis à prova de *ransomware*.
- **Obrigação 2: Comunicação tempestiva de incidentes de segurança à autoridade e aos titulares (Art. 48):**
  > *Art. 48. O controlador deverá comunicar à autoridade nacional e aos titulares a ocorrência de incidente de segurança que possa acarretar risco ou dano relevante aos titulares.*
  - *Aplicação Prática na Nuvem:* Em caso de violação de dados ou ataque cibernético que afete o ambiente em nuvem, a empresa controladora não pode ocultar o evento; ela é compelida a protocolar comunicação formal junto à ANPD (Autoridade Nacional de Proteção de Dados) e alertar os usuários impactados dentro de prazo razoável, discriminando a natureza dos dados vazados, as medidas de contingência adotadas e os riscos decorrentes.

*Fonte primária:* BRASIL. *Lei nº 13.709, de 14 de agosto de 2018*. Lei Geral de Proteção de Dados Pessoais (LGPD). Diário Oficial da União, Brasília, DF, 2018. Disponível em: <http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm>.

---

### 9. Sistemas Legados: Modelo dos "6 Rs" da migração para nuvem

O framework dos "6 Rs" foi concebido para estruturar a jornada de modernização de portfólios corporativos legados para a nuvem. Selecionamos três deles:

1. **Rehost ("Lift and Shift" — Migrar e Hospedar):**
   - *Significado:* Consiste em migrar aplicações e bancos de dados do ambiente local diretamente para instâncias virtuais na nuvem (IaaS) praticamente sem nenhuma modificação no código-fonte, na arquitetura ou no sistema operacional. Trata-se de "copiar e colar" a carga de trabalho no novo provedor.
   - *Cenário mais indicado:* Projetos com prazos operacionais críticos e inegociáveis (ex.: encerramento iminente de contrato de locação de data center físico ou fim de vida de hardware corporativo), bem como para sistemas legados consolidados cuja equipe não possui conhecimento profundo do código-fonte para arriscar refatorações imediatas.
2. **Replatform ("Lift, Tinker and Shift" — Migrar e Ajustar):**
   - *Significado:* Realiza adaptações e substituições pontuais em componentes da arquitetura para aproveitar os benefícios de serviços gerenciados em nuvem (PaaS), sem contudo alterar a lógica essencial e o código principal da aplicação.
   - *Cenário mais indicado:* Migração de bancos de dados relacionais legados executados em servidores físicos (ex.: Oracle, PostgreSQL, Microsoft SQL Server) para plataformas PaaS totalmente gerenciadas (como Amazon RDS, Azure SQL Database ou Google Cloud SQL). Elimina de imediato a carga de trabalho operacional com rotinas manuais de *patching*, replicação e backups, mantendo a compatibilidade do software intacta.
3. **Refactor / Re-architect (Refatorar e Rearquitetar):**
   - *Significado:* Reimaginação e reescrita profunda da solução com princípios de desenvolvimento nativo em nuvem (*Cloud-Native*), decompondo sistemas monolíticos em microsserviços desacoplados, contêineres e arquiteturas serverless orientadas a eventos.
   - *Cenário mais indicado:* Aplicações de missão crítica que representam o diferencial competitivo da empresa (ex.: sistema de pagamentos de um e-commerce ou telemedicina), cujos requisitos exigem extrema elasticidade sob demanda, tempos mínimos de resposta e deploys contínuos sem indisponibilidade de versão.

*Fonte primária:* AWS PRESCRIPTIVE GUIDANCE. *Migration strategy: 6 Rs of cloud migration*. Amazon Web Services, 2024. Disponível em: <https://docs.aws.amazon.com/prescriptive-guidance/latest/migration-strategies/welcome.html>.

---

### 10. Cultura Organizacional: Caso real de resistência à nuvem

**Caso Escolhido:** Adoção de Nuvem no Setor Financeiro Brasileiro (Grandes Bancos e Bancos Tradicionais) e o caso da plataforma de streaming **Netflix**.

- **Fatores Geradores de Resistência:**
  - *No Setor Bancário Tradicional:* Historicamente, diretorias executivas, conselhos de administração e equipes técnicas de infraestrutura mantinham forte resistência à nuvem pública devido ao receio arraigado de violações de segurança e vazamentos que acarretassem penalidades regulatórias extremas e dano à reputação. Adicionalmente, as equipes operacionais de data center temiam a obsolescência de suas funções e perda de controle sobre o ambiente técnico.
  - *No caso da Netflix (2008):* Em agosto de 2008, uma corrupção catastrófica de banco de dados em seu data center físico próprio paralisou o envio de DVDs por três dias seguidos. Quando a liderança de engenharia decidiu fechar os data centers e migrar toda a operação para a AWS, houve forte ceticismo interno e externo: a indústria acreditava ser impraticável rodar um negócio de streaming de vídeo massivo sobre a infraestrutura elástica de terceiros, temendo que quedas do provedor aniquilassem o serviço.
- **Como a Resistência foi Superada:**
  - *Marco Regulatório e Governança no Brasil:* A resistência do setor bancário foi dirimida quando o Banco Central formalizou parâmetros rígidos de segurança e governança de dados na nuvem (Resoluções nº 4.658/2018 e nº 4.893/2021). Os bancos criaram centros de excelência em nuvem (*Cloud Centers of Excellence - CCoE*) e desenvolveram modelos híbridos onde a posse e a custódia das chaves criptográficas de segurança máxima ficam sob o domínio exclusivo do banco (*Bring Your Own Key - BYOK* / HSM dedicado), impedindo que até o próprio provedor de nuvem leia os dados transacionais.
  - *Engenharia do Caos na Netflix:* A Netflix superou o ceticismo criando uma nova cultura de engenharia e confiabilidade, pioneira na técnica batizada de *Chaos Engineering* (com ferramentas de código aberto como o *Chaos Monkey*). Em vez de esperar que a nuvem nunca falhasse, desenharam seus sistemas assumindo que instâncias e zonas falhariam a qualquer momento, testando deliberadamente desligamentos em produção para provar a resiliência arquitetural. Ao mesmo tempo, capacitaram intensamente seu corpo de desenvolvedores, transformando a computação em nuvem no motor propulsor da sua expansão global.

*Fontes primárias:*
- COCKCROFT, Adrian. *Completing the Netflix Cloud Migration*. Netflix TechBlog, 2016. Disponível em: <https://netflixtechblog.com/completing-the-netflix-cloud-migration-350c3f3252d4>.
- BANCO CENTRAL DO BRASIL. *Resolução CMN nº 4.893/2021*.

---

## BLOCO 4 — MODELOS DE SERVIÇO: IAAS, PAAS E SAAS

### 11. Tabela Comparativa de Modelos de Serviço

A separação de papéis na computação em nuvem orienta-se pelo **Modelo de Responsabilidade Compartilhada (*Shared Responsibility Model*)**:

| Critério Analisado | Infraestrutura como Serviço (**IaaS**) | Plataforma como Serviço (**PaaS**) | Software como Serviço (**SaaS**) |
| :--- | :--- | :--- | :--- |
| **O que o Cliente Gerencia** | Sistema Operacional, *runtime*, middleware, configurações de rede interna/firewall, dados da aplicação, rotinas de backup e o código da aplicação. | O código-fonte da aplicação, dados de negócio, parametrizações e integrações da aplicação. | Apenas configurações de conta de usuário, preferências pessoais e permissões internas de acesso aos dados. |
| **O que o Provedor Gerencia** | Virtualização, servidores físicos, armazenamento de blocos/rede, infraestrutura de data center e climatização/energia física. | Virtualização, hardware físico, data centers, além de todo o Sistema Operacional, instalação de *patches*, *runtimes* de linguagem e escalabilidade da máquina. | Absolutamente toda a pilha tecnológica: hardware, SO, banco de dados, rede, atualizações do sistema, código do software e correções de segurança da aplicação. |
| **Nível de Flexibilidade** | **Altíssimo:** O cliente detém controle total para instalar qualquer versão de SO, kernels customizados, softwares de rede e utilitários específicos de baixo nível. | **Médio:** O cliente foca no desenvolvimento do código, devendo respeitar as linguagens, versões de *runtime* e ecossistemas homologados pela plataforma. | **Baixo:** A flexibilidade restringe-se às opções de customização e interfaces disponibilizadas nativamente pelo fabricante do software. |
| **Responsabilidade do Cliente pela Segurança** | **Alta:** O cliente deve aplicar atualizações (*patches*) de segurança no SO, configurar firewalls de software, proteger portas e criptografar discos manualmente. | **Média:** O cliente é responsável por mitigar vulnerabilidades no seu código-fonte (ex.: SQL Injection, XSS) e gerenciar identidades e acessos (IAM). | **Mínima:** O cliente zela apenas pela segurança de suas credenciais de acesso (senhas fortes e uso de MFA) e permissões de usuários. |

---

### 12. Dois Provedores Diferentes para Cada Modelo de Serviço

Abaixo, fornecedores consolidados no mercado tecnológico global que divergem dos exemplos básicos de sala de aula:

1. **Infraestrutura como Serviço (IaaS):**
   - *Provedor 1:* **DigitalOcean** (Serviço: *DigitalOcean Droplets*) — Provedor focado em desenvolvedores e empresas de tecnologia que oferece instâncias de máquinas virtuais sob demanda com escolha do sistema operacional Linux, IPs dedicados e discos SSD NVMe com precificação previsível.
   - *Provedor 2:* **Oracle Cloud Infrastructure - OCI** (Serviço: *OCI Compute*) — Oferece instâncias bare-metal dedicadas e máquinas virtuais flexíveis de alta performance, bastante utilizadas para cargas de bancos de dados empresariais e modelos de treinamento de IA.
2. **Plataforma como Serviço (PaaS):**
   - *Provedor 1:* **Render** (Serviço: *Render Web Services & PostgreSQL*) — Plataforma em nuvem totalmente gerenciada que automatiza o *build* e o *deploy* contínuo de código diretamente do GitHub/GitLab, provisionando containers e certificados TLS automaticamente sem intervenção em servidores.
   - *Provedor 2:* **Google App Engine** (Google Cloud) — Plataforma clássica de PaaS que permite aos desenvolvedores implantar aplicações monolíticas ou microsserviços em linguagens como Python, Java e Go com provisionamento automático de balanceadores de carga e escala automática a zero.
3. **Software como Serviço (SaaS):**
   - *Provedor 1:* **Salesforce Sales Cloud** — Principal plataforma global de CRM (*Customer Relationship Management*), totalmente acessada pelo navegador ou aplicativo para gestão completa de clientes, pipeline de vendas e funis de marketing sem que a empresa gerencie servidores.
   - *Provedor 2:* **Slack Technologies (Salesforce)** — Plataforma corporativa de colaboração e mensageria em tempo real, fornecida integralmente como serviço na nuvem com criptografia de ponta e integrações com ecossistemas externos.

---

### 13. Function as a Service (FaaS) / Computação Serverless

**Conceito:**  
*Function as a Service* (FaaS) — amplamente conhecido como computação *serverless* (ex.: AWS Lambda, Azure Functions, Google Cloud Run/Functions) — é um modelo de computação em nuvem orientado a eventos (*event-driven*). Nele, o desenvolvedor escreve blocos isolados e modulares de código (funções atômicas e *stateless*) que são executadas exclusivamente quando acionadas por um evento externo específico (por exemplo: uma requisição HTTP, o upload de um arquivo para um bucket de armazenamento ou uma mensagem recebida em uma fila). Não há servidores virtuais persistentemente ativos sob a gestão do cliente; a plataforma orquestra e inicializa o container de execução sob demanda e cobra apenas pela quantidade de milissegundos em que o código esteve em processamento ativo.

**Aproximação com os Modelos de Serviço:**  
O modelo FaaS aproxima-se primordialmente do **PaaS (Plataforma como Serviço)**, sendo classificado pela literatura e pelo mercado como uma evolução direta e especializada do PaaS (frequentemente denominado *Event-driven PaaS* ou *Serverless PaaS*).

**Justificativa Técnica:**
- Assim como no PaaS clássico, o FaaS **elimina por completo a necessidade de gerenciar o sistema operacional, patches de segurança de kernel, hardware ou capacidade de provisionamento de instâncias**.
- Em ambos os modelos, a responsabilidade do cliente está restrita unicamente à lógica do código da aplicação.
- A principal distinção entre o PaaS convencional e o FaaS é a granularidade e o ciclo de vida: enquanto o PaaS tradicional normalmente hospeda uma aplicação web de execução contínua aguardando requisições em uma porta de rede, o FaaS opera em granularidade de microfunções temporárias que **escalam a zero (*scale to zero*)** quando ociosas, não gerando qualquer custo de máquina virtual parada.

---

# PARTE 2 — ATIVIDADE PRÁTICA

---

## PRÁTICA 1 — MATRIZ COMPARATIVA DE PROVEDORES

Abaixo, a pesquisa comparativa detalhada estruturada a partir da documentação técnica primária de três grandes provedores de nuvem globais:

| Critério de Comparação | Provedor 1: Amazon Web Services (AWS) | Provedor 2: Microsoft Azure | Provedor 3: Google Cloud Platform (GCP) |
| :--- | :--- | :--- | :--- |
| **Modelos de implantação oferecidos (pública / privada / híbrida)** | **Pública:** AWS Global Cloud.<br>**Privada/Híbrida:** AWS Outposts (hardware AWS no data center do cliente), AWS Local Zones e AWS Wavelength. | **Pública:** Azure Global Cloud.<br>**Privada/Híbrida:** Azure Arc (gestão unificada on-premise/multicloud) e Azure Stack Hub (execução de IaaS/PaaS local). | **Pública:** Google Cloud Global.<br>**Privada/Híbrida:** Google Distributed Cloud (GDC) e GKE Enterprise (antigo Anthos) para gestão de clusters híbridos. |
| **Principal serviço IaaS** | **Amazon EC2 (Elastic Compute Cloud):** Fornecimento de instâncias de máquinas virtuais configuráveis e escaláveis. | **Azure Virtual Machines (Azure VMs):** Máquinas virtuais sob demanda para Linux e Windows Server. | **Google Compute Engine (GCE):** Máquinas virtuais flexíveis de alta velocidade com discos persistentes. |
| **Principal serviço PaaS** | **AWS Elastic Beanstalk** / **AWS App Runner:** Orquestração e deploy automático de aplicações web conteinerizadas. | **Azure App Service:** Plataforma gerenciada para hospedar aplicações web, APIs RESTful e backends móveis. | **Google App Engine** / **Cloud Run:** Plataforma totalmente gerenciada que executa containers sob demanda com escala a zero. |
| **Principal serviço SaaS (se houver)** | **Amazon WorkSpaces** (Virtual Desktop) e **Amazon Connect** (Contact Center em nuvem omnichannel). | **Microsoft 365** (Word, Excel, Teams, Exchange Online) e **Dynamics 365** (ERP/CRM). | **Google Workspace** (Gmail, Google Docs, Drive, Meet, Planilhas). |
| **Existe camada gratuita (Free Tier)? Quais limites?** | **Sim.** Possui 3 categorias:<br>• *12 meses grátis:* 750 horas/mês de EC2 `t2.micro` ou `t3.micro`, 5 GB de armazenamento Amazon S3 Standard e 750 horas de banco Amazon RDS.<br>• *Sempre grátis:* 1 milhão de requisições mensais no AWS Lambda e 10 métricas de monitoramento no CloudWatch.<br>*Ref.:* aws.amazon.com/free | **Sim.** Possui 3 categorias:<br>• *12 meses grátis:* 750 horas/mês de VMs B1s (Linux e Windows), 5 GB de armazenamento Azure Blob LRS e 250 GB de Azure SQL Database.<br>• *Sempre grátis:* 1 milhão de chamadas no Azure Functions e até 10 apps no Azure App Service F1 tier.<br>• *Crédito inicial:* US$ 200 para os primeiros 30 dias.<br>*Ref.:* azure.microsoft.com/free | **Sim.** Possui 2 categorias:<br>• *Sempre grátis:* 1 instância VM `e2-micro` (com 1 GB de RAM e 30 GB de disco na região dos EUA), 2 milhões de invocações Cloud Functions e 5 GB de Cloud Storage regional.<br>• *Crédito de teste:* US$ 300 para novos clientes gastarem em 90 dias.<br>*Ref.:* cloud.google.com/free |
| **Regiões de data center disponíveis no Brasil** | **Região América do Sul (São Paulo):** Identificador técnico `sa-east-1`, composta por **3 Zonas de Disponibilidade (AZs)** fisicamente isoladas na Grande São Paulo, operando desde 2011. | **Região Brazil South (São Paulo):** Operando em São Paulo com suporte a múltiplas Zonas de Disponibilidade, complementada pela região secundária *Brazil Southeast* (Rio de Janeiro). | **Região southamerica-east1 (São Paulo):** Inaugurada em 2017, composta por **3 Zonas de Disponibilidade (AZs)**, com data centers em São Paulo e Vinhedo (SP). |

---

## PRÁTICA 2 — PUBLICANDO NA NUVEM (HANDS-ON)

Para atender a esta prática sem exigência de cadastro de cartão de crédito, utilizou-se uma plataforma moderna de **PaaS / Jamstack (GitHub Pages / Vercel / Netlify)** para publicar uma página web estática com identificação acadêmica e síntese sobre computação em nuvem.

### 1. Código-fonte da Página Web Publicada (`index.html`)

O código abaixo foi desenvolvido com padrão HTML5/CSS3 responsivo e moderno, pronto para hospedagem:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Computação em Nuvem I - Atividade Prática</title>
    <style>
        :root {
            --bg: #0f172a;
            --surface: #1e293b;
            --text: #f8fafc;
            --text-muted: #94a3b8;
            --border: #334155;
            --accent: #38bdf8;
        }
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
        body { background-color: var(--bg); color: var(--text); line-height: 1.6; padding: 2rem 1rem; }
        .container { max-width: 800px; margin: 0 auto; }
        header { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; padding: 2rem; margin-bottom: 2rem; }
        h1 { color: var(--accent); font-size: 1.8rem; margin-bottom: 0.5rem; }
        .meta { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem; margin-top: 1.5rem; padding-top: 1rem; border-top: 1px solid var(--border); }
        .meta-item span { display: block; font-size: 0.85rem; color: var(--text-muted); text-transform: uppercase; }
        .meta-item strong { font-size: 1.05rem; color: var(--text); }
        .card { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; padding: 2rem; margin-bottom: 1.5rem; }
        h2 { color: var(--accent); font-size: 1.4rem; margin-bottom: 1rem; }
        p { margin-bottom: 1rem; color: #cbd5e1; }
        .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem; margin-top: 1.5rem; }
        .feature-box { background: rgba(15, 23, 42, 0.6); border: 1px solid var(--border); border-radius: 8px; padding: 1rem; }
        .feature-box h3 { color: #38bdf8; font-size: 1rem; margin-bottom: 0.5rem; }
        .feature-box p { font-size: 0.9rem; color: var(--text-muted); margin-bottom: 0; }
        footer { text-align: center; margin-top: 2rem; font-size: 0.85rem; color: var(--text-muted); }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Computação em Nuvem I</h1>
            <p>Atividade de Pesquisa e Prática — Publicação na Nuvem (Hands-On)</p>
            <div class="meta">
                <div class="meta-item">
                    <span>Estudante</span>
                    <strong>Tiago</strong>
                </div>
                <div class="meta-item">
                    <span>Turma / Período</span>
                    <strong>Computação em Nuvem I</strong>
                </div>
                <div class="meta-item">
                    <span>Ambiente de Hospedagem</span>
                    <strong>GitHub Pages (PaaS)</strong>
                </div>
            </div>
        </header>

        <section class="card">
            <h2>O que é Computação em Nuvem?</h2>
            <p>
                Segundo o <strong>NIST SP 800-145</strong>, a computação em nuvem é um modelo para viabilizar o acesso sob demanda e via rede a um pool compartilhado de recursos computacionais configuráveis (servidores, armazenamento e redes) que podem ser rapidamente provisionados com o mínimo de esforço de gerenciamento.
            </p>
            <div class="features-grid">
                <div class="feature-box">
                    <h3>1. Autoatendimento sob Demanda</h3>
                    <p>Provisionamento autônomo e imediato sem interação com operadores humanos.</p>
                </div>
                <div class="feature-box">
                    <h3>2. Amplo Acesso à Rede</h3>
                    <p>Acessibilidade multiplataforma por protocolos universais de comunicação.</p>
                </div>
                <div class="feature-box">
                    <h3>3. Pool de Recursos</h3>
                    <p>Infraestrutura multi-inquilino com alocação dinâmica e isolamento seguro.</p>
                </div>
                <div class="feature-box">
                    <h3>4. Elasticidade Rápida</h3>
                    <p>Capacidade de escalabilidade contínua e automática acompanhando o tráfego.</p>
                </div>
                <div class="feature-box">
                    <h3>5. Serviço Mensurável</h3>
                    <p>Telemetria e controle de uso para faturamento transparente por consumo.</p>
                </div>
            </div>
        </section>
        <footer>
            <p>&copy; 2026 — Atividade Acadêmica de Computação em Nuvem I</p>
        </footer>
    </div>
</body>
</html>
```

### 2. Instruções de Deploy Rápido (100% Gratuito e sem Cartão):
- **Passo 1:** No [GitHub](https://github.com), crie um repositório público chamado `nuvem-pratica`.
- **Passo 2:** Faça o upload do arquivo `index.html` (ou adicione via git).
- **Passo 3:** No repositório, acesse **Settings > Pages**. Em *Build and deployment*, na opção *Source*, selecione a branch `main` e a pasta `/(root)`, clicando em **Save**.
- **Passo 4:** Em cerca de 1 minuto, o link público será gerado no topo da página.

### 3. Informações da Aplicação Publicada:
- **Link Público:** `https://tiagow2.github.io/Computa-o-em-Nuvem/` *(ou link Vercel/Netlify correspondente)*
- **Evidência de Publicação:** *(Anexe aqui o print de tela do painel do GitHub Pages / Vercel com status "Deployed" com data e hora visíveis).*

### 4. Parágrafo Explicativo Técnico Obrigatório:
> A plataforma de publicação utilizada (**GitHub Pages**) representa essencialmente o modelo de serviço **PaaS (Plataforma como Serviço)** focado em hospedagem de aplicações web estáticas. Nesse modelo, a minha responsabilidade enquanto usuário/desenvolvedor restringiu-se exclusivamente à concepção e estruturação do código-fonte (`index.html`) e ao apontamento da branch de publicação no repositório. Por outro lado, todo o restante da pilha operacional ficou sob encargo integral do provedor: o provisionamento do servidor web (Nginx), a configuração e emissão automatizada do certificado criptográfico SSL/TLS para HTTPS, a orquestração do pipeline de integração contínua (CI/CD via GitHub Actions), a distribuição global do conteúdo em nós de CDN (*Content Delivery Network*) com proteção contra ataques de negação de serviço (DDoS), bem como toda a manutenção do sistema operacional subjacente e da infraestrutura física do data center.

---

## PRÁTICA 3 — ESTUDO DE CASO: DESENHO DE ARQUITETURA HÍBRIDA

### O Cenário do Hospital:
> *Um hospital de médio porte deseja modernizar sua infraestrutura de TI. Ele precisa manter os prontuários eletrônicos de pacientes (dados sensíveis, sujeitos à LGPD) sob total controle interno, mas também quer usar aplicações de agendamento online e um sistema de telemedicina que apresentam picos de acesso variáveis ao longo do dia.*

---

### a. Quais partes do sistema você colocaria em nuvem privada, e quais em nuvem pública? Justifique com base nas características de privacidade e elasticidade estudadas.

**Proposta de Divisão Arquitetural:**

1. **Componentes Alocados na Nuvem Privada (Data Center Interno do Hospital):**
   - **Banco de Dados Central de Prontuários Eletrônicos dos Pacientes (PEP):** Histórico clínico, laudos médicos, prescrições farmacológicas e exames diagnósticos de alta resolução (PACS/DICOM).
   - **Servidor de Chaves Criptográficas (HSM):** Armazenamento de chaves mestras e controle estrito de autenticação de médicos e equipe assistencial.
   - **Justificativa de Privacidade (LGPD):** Dados relativos à saúde são classificados legalmente pelo Art. 5º, inciso II da LGPD como **dados pessoais sensíveis**, exigindo rigor máximo de proteção. Manter o repositório central na nuvem privada garante ao hospital a custódia e o controle físico irrestrito das mídias de armazenamento, auditoria local direta e garantia de que nenhum dado sensível sairá da jurisdição física institucional sem autorização prévia. Além disso, a rede local hospitalar assegura latência ultrabaixa (< 5ms) para acesso a imagens médicas pesadas nos computadores de centros cirúrgicos e UTIs, sem vulnerabilidade a eventuais interrupções de links externos de internet.

2. **Componentes Alocados na Nuvem Pública (ex.: AWS, Azure ou Google Cloud):**
   - **Portal Web e Aplicativo Mobile de Agendamento de Consultas:** Interface pública de autoatendimento para pacientes.
   - **Plataforma de Videoconferência e Salas Virtuais de Telemedicina:** Serviços de *streaming* de áudio/vídeo WebRTC, salas de espera virtual e fila de triagem remota.
   - **Microsserviço de Notificações:** Disparo de lembretes e confirmações por WhatsApp/SMS e e-mail.
   - **Justificativa de Elasticidade:** Aplicações voltadas ao público externo apresentam padrões de acessos com **picos sazonais extremos e imprevisíveis** (por exemplo: abertura de agendas de especialistas no primeiro dia do mês ou campanhas de vacinação). A nuvem pública oferece o pilar da **elasticidade rápida** (*Auto Scaling* e balanceamento de carga), provisionando novos contêineres e largura de banda instantaneamente durante os picos e encolhendo os recursos na madrugada, evitando desperdício de investimentos em servidores locais que ficariam ociosos a maior parte do tempo.

---

### b. Essa arquitetura seria classificada como nuvem híbrida? Explique por quê.

**Sim.** A solução desenhada enquadra-se rigorosamente na definição clássica de **Nuvem Híbrida** estabelecida pelo NIST SP 800-145.

**Justificativa Técnica:**
A arquitetura é composta pela coexistência de duas infraestruturas de nuvem conceitualmente distintas:
- Uma **nuvem privada** (executada no data center do hospital para governança dos dados sensíveis do PEP); e
- Uma **nuvem pública** (hospedada em provedor externo para executar as aplicações elásticas de agendamento e telemedicina).

Elas permanecem como entidades operacionais únicas e autônomas, mas são **intrinsecamente interligadas e orquestradas por meio de canais de comunicação seguros e padronizados** — especificamente um túnel de VPN IPsec corporativo com criptografia AES-GCM-256 redundante ou link dedicado direto (*AWS Direct Connect* / *Azure ExpressRoute*). 

O sistema de agendamento na nuvem pública comunica-se com a nuvem privada exclusivamente por meio de chamadas de API autenticadas e controladas por um *API Gateway* com regras de validação rigorosas. Dessa forma, há troca fluida e portabilidade de fluxos de trabalho entre os dois ambientes sem que a base de dados interna fique diretamente exposta à internet pública.

---

### c. Que desafios (dos quatro estudados: segurança, privacidade, legado, cultura) você espera que essa migração enfrente no hospital, e como mitigá-los?

| Eixo de Desafio | Descrição do Desafio Específico no Hospital | Plano de Mitigação Técnico e Organizacional |
| :--- | :--- | :--- |
| **1. Segurança** | O elo de comunicação que integra a nuvem pública à nuvem privada interna (APIs de telemedicina e agendamento) torna-se um alvo atrativo para ataques cibernéticos, injeção de comandos maliciosos e sequestro de dados (*ransomware*). | • Estabelecer arquitetura **Zero Trust** (nenhum componente confia cegamente no outro).<br>• Tráfego de interconexão canalizado estritamente por túnel VPN criptografado com TLS 1.3 / IPsec dedicado.<br>• Posicionamento de um *Web Application Firewall (WAF)* e *API Gateway* com autenticação mútua (mTLS) e limitação de taxa (*rate limiting*).<br>• Criptografia total de ponta a ponta dos dados em trânsito e em repouso. |
| **2. Privacidade (LGPD)** | Risco de vazamento de dados de prontuários médicos durante as transmissões de telemedicina ou armazenamento inadvertido de dados de pacientes em caches/logs da nuvem pública em desconformidade com a LGPD. | • Implementar técnicas de **anonimização ou pseudonimização** de identificadores de pacientes na camada pública (o portal web trafega apenas IDs aleatórios e *tokens*, nunca o CPF ou histórico clínico descriptografado).<br>• Configuração estrita de regras de retenção nos serviços da nuvem pública para apagar logs transitórios imediatamente após a conclusão da consulta remota.<br>• Elaboração formal do Relatório de Impacto à Proteção de Dados Pessoais (RIPD). |
| **3. Sistemas Legados** | O sistema de prontuário eletrônico antigo do hospital comumente opera em arquitetura monolítica, cliente-servidor tradicional ou em bancos relacionais antigos sem suporte nativo a chamadas de API modernas (REST/JSON), gerando atrito de integração. | • Adoção da estratégia de migração **Replatform** ou **Refactor parcial**, criando uma camada intermediária de microsserviços desacoplados (*BFF — Backend for Frontend* ou padrão *Strangler Fig*).<br>• Essa camada atua como adaptador / ponte de tradução, convertendo as consultas das APIs modernas em instruções que o banco legado compreende sem necessidade de substituir o software hospitalar imediatamente. |
| **4. Cultura Organizacional** | Resistência do corpo clínico (médicos e enfermeiros) ao uso de novas interfaces de telemedicina e agendamento, aliada ao receio da equipe interna de TI do hospital de perder relevância e controle com a terceirização de parte dos sistemas para a nuvem. | • Instituir um comitê de Gestão de Mudança (*Change Management*), envolvendo médicos-chave desde a fase de testes e prototipagem da telemedicina para garantir ergonomia de uso.<br>• Promover programas de capacitação e reciclagem técnica para os analistas de TI locais em computação em nuvem e DevOps, demonstrando que eles se tornarão gestores estratégicos de nuvem híbrida e segurança, e não apenas operadores de hardware. |

---

# REFERÊNCIAS BIBLIOGRÁFICAS (NORMAS ABNT)

1. AMAZON WEB SERVICES (AWS). **Overview of Amazon Web Services: AWS Whitepapers**. Seattle: Amazon, 2024. Disponível em: <https://docs.aws.amazon.com/whitepapers/latest/aws-overview/aws-overview.pdf>. Acesso em: 14 set. 2026.
2. BANCO CENTRAL DO BRASIL (BACEN). **Resolução CMN nº 4.893, de 26 de fevereiro de 2021**. Dispõe sobre a política de segurança cibernética e sobre os requisitos para a contratação de serviços de processamento e armazenamento de dados e de computação em nuvem a serem observados pelas instituições financeiras. Brasília: Diário Oficial da União, 2021.
3. BRASIL. **Lei nº 13.709, de 14 de agosto de 2018**. Dispõe sobre o tratamento de dados pessoais, inclusive nos meios digitais (Lei Geral de Proteção de Dados Pessoais - LGPD). Brasília: Diário Oficial da União, 2018. Disponível em: <http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm>. Acesso em: 14 set. 2026.
4. CLOUD SECURITY ALLIANCE (CSA). **Top Threats to Cloud Computing**. CSA Research, 2024. Disponível em: <https://cloudsecurityalliance.org/research/top-threats/>. Acesso em: 14 set. 2026.
5. COCKCROFT, Adrian. **Completing the Netflix Cloud Migration**. Netflix Technology Blog, 2016. Disponível em: <https://netflixtechblog.com/completing-the-netflix-cloud-migration-350c3f3252d4>. Acesso em: 14 set. 2026.
6. ERL, Thomas; PUTTINI, Ricardo; MAHMOOD, Zaigham. **Cloud Computing: Concepts, Technology & Architecture**. Upper Saddle River: Prentice Hall / Pearson, 2013.
7. GOOGLE CLOUD. **Google Cloud documentation and architecture center**. Google, 2024. Disponível em: <https://cloud.google.com/docs>. Acesso em: 14 set. 2026.
8. MELL, Peter; GRANCE, Timothy. **The NIST Definition of Cloud Computing**. NIST Special Publication 800-145. Gaithersburg: National Institute of Standards and Technology (NIST), U.S. Department of Commerce, 2011. Disponível em: <https://doi.org/10.6028/NIST.SP.800-145>. Acesso em: 14 set. 2026.
9. MICROSOFT AZURE. **Microsoft Azure Documentation and Architecture Guidelines**. Redmond: Microsoft, 2024. Disponível em: <https://learn.microsoft.com/en-us/azure/>. Acesso em: 14 set. 2026.
