# COMPUTAÃ‡ÃƒO EM NUVEM I
## Atividade de Pesquisa e PrÃ¡tica: ContextualizaÃ§Ã£o, Modelos de ImplantaÃ§Ã£o, CaracterÃ­sticas, Desafios e Modelos de ServiÃ§o em Nuvem

---

### DADOS DE IDENTIFICAÃ‡ÃƒO

- **Aluno(a):** Tiago
- **Turma / Curso:** ComputaÃ§Ã£o em Nuvem I / [Insira seu Curso / PerÃ­odo]
- **Data de Entrega:** 14/09/2026
- **Formato de Entrega:** RelatÃ³rio TÃ©cnico-AcadÃªmico e PrÃ¡tico com EvidÃªncias de PublicaÃ§Ã£o

---

# PARTE 1 â€” ATIVIDADE TEÃ“RICA (PESQUISA DIRIGIDA)

---

## BLOCO 1 â€” CONTEXTUALIZAÃ‡ÃƒO E MODELOS DE IMPLANTAÃ‡ÃƒO

### 1. O que caracteriza um sistema de computaÃ§Ã£o em nuvem em comparaÃ§Ã£o com a infraestrutura de TI tradicional (on-premise)? Cite pelo menos trÃªs diferenÃ§as.

**Resposta:**

A **computaÃ§Ã£o em nuvem** Ã© definida formalmente pelo *National Institute of Standards and Technology* (NIST SP 800-145) como um modelo que viabiliza o acesso onipresente, conveniente e sob demanda por meio de rede a um conjunto compartilhado de recursos de computaÃ§Ã£o configurÃ¡veis (como servidores, armazenamento, redes e aplicaÃ§Ãµes), os quais podem ser provisionados e liberados com rapidez e esforÃ§o mÃ­nimo de gerenciamento ou interaÃ§Ã£o com o provedor.

Em contrapartida, a **infraestrutura de TI tradicional (*on-premise*)** baseia-se na aquisiÃ§Ã£o, instalaÃ§Ã£o, operaÃ§Ã£o e custÃ³dia fÃ­sica direta de ativos de hardware em um data center proprietÃ¡rio mantido pela prÃ³pria empresa.

As trÃªs principais diferenÃ§as estruturais sÃ£o:

1. **Modelo Financeiro e AlocaÃ§Ã£o de Recursos (CapEx vs. OpEx):**
   - *TI Tradicional (CapEx):* Exige vultoso investimento inicial de capital (*Capital Expenditure*) na compra de servidores fÃ­sicos, licenÃ§as perenes de software, switches de rede, no-breaks, geradores a diesel e sistemas de climatizaÃ§Ã£o. Esse dimensionamento precisa ser feito com base no pico histÃ³rico projetado para 3 a 5 anos, resultando em frequente ociosidade de infraestrutura cara.
   - *ComputaÃ§Ã£o em Nuvem (OpEx):* Opera quase integralmente como despesa operacional (*Operational Expenditure*), adotando o modelo financeiro de pagamento conforme o consumo (*pay-as-you-go*). A organizaÃ§Ã£o nÃ£o imobiliza capital em ativos que depreciam e paga apenas pelo tempo de processamento, armazenamento e trÃ¡fego de dados efetivamente utilizados.
2. **Tempo de Provisionamento e Elasticidade:**
   - *TI Tradicional:* O processo de expansÃ£o de capacidade envolve cotaÃ§Ãµes de fornecedores, compras, desembaraÃ§o fiscal, entrega logÃ­stica, montagem em rack, cabeamento e homologaÃ§Ã£o â€” um ciclo que comumente leva de semanas a meses.
   - *ComputaÃ§Ã£o em Nuvem:* A alocaÃ§Ã£o de novos recursos Ã© elÃ¡stica, instantÃ¢nea e programÃ¡vel. Novas instÃ¢ncias de computaÃ§Ã£o ou dezenas de gigabytes de armazenamento sÃ£o provisionados em segundos ou poucos minutos por meio de chamadas de API, scripts de Infraestrutura como CÃ³digo (IaC) ou consoles web.
3. **Escopo de Responsabilidade Operacional e ManutenÃ§Ã£o FÃ­sica:**
   - *TI Tradicional:* A equipe interna de TI Ã© integralmente responsÃ¡vel por todas as camadas: seguranÃ§a perimetral do data center, manutenÃ§Ã£o preventiva e corretiva de hardware fÃ­sico, substituiÃ§Ã£o de discos danificados, redundÃ¢ncia elÃ©trica, firmware de placas-mÃ£e e hipervisores.
   - *ComputaÃ§Ã£o em Nuvem:* O provedor assume a gestÃ£o, manutenÃ§Ã£o fÃ­sica, resiliÃªncia energÃ©tica e seguranÃ§a da infraestrutura de base (o que o NIST chama de *underlying physical infrastructure*). Isso libera a equipe corporativa para direcionar seu foco e energia intelectual ao desenvolvimento de produtos, regras de negÃ³cio e inovaÃ§Ã£o.

*Fontes primÃ¡rias consultadas:*
- MELL, Peter; GRANCE, Timothy. *The NIST Definition of Cloud Computing*. NIST Special Publication 800-145, Gaithersburg, 2011. DisponÃ­vel em: <https://doi.org/10.6028/NIST.SP.800-145>.
- AMAZON WEB SERVICES. *What is Cloud Computing?*. AWS Documentation, 2024. DisponÃ­vel em: <https://aws.amazon.com/what-is-cloud-computing/>.

---

### 2. Defina, com suas palavras, nuvem pÃºblica, nuvem privada e nuvem hÃ­brida. Para cada uma, apresente um exemplo real de provedor ou de caso de uso corporativo.

**Resposta:**

- **Nuvem PÃºblica:**
  - *DefiniÃ§Ã£o:* Ã‰ uma infraestrutura de computaÃ§Ã£o em nuvem de propriedade de um provedor especializado externo, disponibilizada para uso amplo de pessoas fÃ­sicas ou organizaÃ§Ãµes de diferentes segmentos. Os recursos fÃ­sicos (servidores, redes e armazenamento) sÃ£o compartilhados entre mÃºltiplos clientes (*multi-tenant*), mas isolados logicamente por meio de virtualizaÃ§Ã£o e criptografia.
  - *Exemplo de Provedor e Caso Real:* **Amazon Web Services (AWS)**. A **Netflix** Ã© um caso emblemÃ¡tico de uso corporativo de nuvem pÃºblica: ela fechou completamente seus data centers fÃ­sicos e migrou todo o seu ecossistema de processamento de vÃ­deos, microsserviÃ§os de recomendaÃ§Ã£o e autenticaÃ§Ã£o de usuÃ¡rios para a AWS, aproveitando a capacidade de escala global e presenÃ§a geogrÃ¡fica do provedor.
- **Nuvem Privada:**
  - *DefiniÃ§Ã£o:* Ã‰ a infraestrutura de computaÃ§Ã£o em nuvem operada e destinada ao uso exclusivo de uma Ãºnica organizaÃ§Ã£o, com mÃºltiplos departamentos e equipes internas atuando como consumidores. Pode ser instalada fisicamente dentro do data center da prÃ³pria instituiÃ§Ã£o (*on-premise*) ou hospedada externamente por um terceiro em regime de locaÃ§Ã£o dedicada (*single-tenant*), oferecendo controle irrestrito sobre hardware, seguranÃ§a e governanÃ§a de dados.
  - *Exemplo de Provedor e Caso Real:* **Red Hat OpenStack Platform** ou **VMware Cloud Foundation**. Um grande banco de investimentos (como o **ItaÃº Unibanco** ou **JPMorgan Chase**) adota nuvem privada em seus data centers prÃ³prios certificados para abrigar sistemas de liquidaÃ§Ã£o financeira de cÃ¢mbio e processamento de contas bancÃ¡rias protegidas por sigilo bancÃ¡rio estrito.
- **Nuvem HÃ­brida:**
  - *DefiniÃ§Ã£o:* Ã‰ a composiÃ§Ã£o arquitetural que conecta de maneira interoperÃ¡vel duas ou mais infraestruturas de nuvem distintas (privadas, pÃºblicas ou comunitÃ¡rias), as quais permanecem como entidades independentes, mas sÃ£o integradas por meio de tecnologias padronizadas de rede segura, orquestraÃ§Ã£o e portabilidade de dados e aplicaÃ§Ãµes.
  - *Exemplo de Provedor e Caso Real:* **Microsoft Azure Arc** ou **AWS Outposts**. Um grande hospital ou laboratÃ³rio de diagnÃ³sticos por imagem que mantÃ©m o banco de dados principal de prontuÃ¡rios eletrÃ´nicos em sua nuvem privada interna (atendendo Ã  LGPD e Ã  baixa latÃªncia para equipamentos mÃ©dicos), enquanto utiliza a nuvem pÃºblica (Microsoft Azure) para disponibilizar o portal web e aplicativo mÃ³vel de agendamento e entrega de laudos aos pacientes.

*Fontes primÃ¡rias consultadas:*
- MELL, P.; GRANCE, T. *NIST SP 800-145*, 2011 (SeÃ§Ãµes 2.3 Deployment Models).
- MICROSOFT LEARN. *What is a public cloud, private cloud, and hybrid cloud?*. Microsoft Azure Documentation, 2024. DisponÃ­vel em: <https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/get-started/cloud-concepts>.

---

### 3. Em que situaÃ§Ãµes uma organizaÃ§Ã£o optaria por uma nuvem hÃ­brida em vez de uma nuvem pÃºblica pura? Utilize como referÃªncia um setor fortemente regulado (por exemplo, bancÃ¡rio, saÃºde ou governo) e explique o motivo da escolha.

**Resposta:**

Uma organizaÃ§Ã£o opta pela **nuvem hÃ­brida** quando se depara com a necessidade concomitante de: (a) garantir conformidade regulatÃ³ria severa, soberania e isolamento fÃ­sico de dados crÃ­ticos; e (b) usufruir da escalabilidade, agilidade de inovaÃ§Ã£o e amplitude de serviÃ§os que apenas a nuvem pÃºblica proporciona.

**CenÃ¡rio de ReferÃªncia: Setor BancÃ¡rio / Financeiro**
InstituiÃ§Ãµes financeiras operam sob estrita regulaÃ§Ã£o do Banco Central do Brasil (notadamente as **ResoluÃ§Ãµes CMN nÂº 4.893/2021 e nÂº 4.658/2018** sobre seguranÃ§a cibernÃ©tica e contrataÃ§Ã£o de serviÃ§os de processamento em nuvem), alÃ©m da Lei Complementar nÂº 105/2001 (Sigilo BancÃ¡rio) e da Lei nÂº 13.709/2018 (LGPD).

**Motivos tÃ©cnicos e de negÃ³cio para a escolha da Nuvem HÃ­brida:**
1. **Soberania e CustÃ³dia de Chaves CriptogrÃ¡ficas e Core Banking:** Os sistemas centrais de conciliaÃ§Ã£o financeira, livros de transaÃ§Ãµes correntes e mÃ³dulos de seguranÃ§a fÃ­sica em hardware (*Hardware Security Module - HSM*) sÃ£o mantidos na nuvem privada do banco. Isso garante auditoria irrestrita, retenÃ§Ã£o do controle fÃ­sico das chaves mestras e conformidade direta com inspeÃ§Ãµes regulatÃ³rias do Bacen.
2. **LatÃªncia Ultrabaixa e ResiliÃªncia Local:** A infraestrutura de terminais de atendimento em agÃªncias e compensaÃ§Ã£o de ordens em bolsas de valores depende de comunicaÃ§Ãµes de rede locais com latÃªncia de milissegundos mÃ­nimos, nÃ£o podendo ficar vulnerÃ¡vel a oscilaÃ§Ãµes de rotas da internet pÃºblica.
3. **Elasticidade em Canais Digitais e InteligÃªncia Artificial na Nuvem PÃºblica:** Ao mesmo tempo, o banco enfrenta picos massivos e imprevisÃ­veis de acessos no aplicativo mÃ³vel em dias de pagamento de salÃ¡rios, inÃ­cio de mÃªs e promoÃ§Ãµes como a Black Friday. Na nuvem hÃ­brida, a camada de atendimento mÃ³vel, *frontend* bancÃ¡rio, processamento analÃ­tico de *Big Data* e modelos generativos de IA para suporte ao cliente rodam na nuvem pÃºblica, conectando-se Ã  nuvem privada de forma segura por meio de conexÃµes dedicadas criptografadas (*AWS Direct Connect* ou *Azure ExpressRoute* com VPN IPsec redundante).

Assim, a nuvem hÃ­brida une o melhor dos dois mundos: **custÃ³dia estrita do dado regulado** internamente e **escalabilidade elÃ¡stica de canais digitais** externamente.

*Fontes primÃ¡rias consultadas:*
- BANCO CENTRAL DO BRASIL. *ResoluÃ§Ã£o CMN nÂº 4.893, de 26 de fevereiro de 2021*. DispÃµe sobre a polÃ­tica de seguranÃ§a cibernÃ©tica e sobre os requisitos para a contrataÃ§Ã£o de serviÃ§os de processamento e armazenamento de dados e de computaÃ§Ã£o em nuvem a serem observados pelas instituiÃ§Ãµes financeiras. DisponÃ­vel em: <https://www.bcb.gov.br/estabilidadefinanceira/exibenormativo?tipo=Resolu%C3%A7%C3%A3o%20CMN&numero=4893>.

---

### 4. Pesquise o conceito de "nuvem comunitÃ¡ria" (community cloud). Ele Ã© reconhecido pela definiÃ§Ã£o oficial do NIST? Em que esse modelo se diferencia da nuvem privada?

**Resposta:**

**Sim**, o conceito de **nuvem comunitÃ¡ria (*community cloud*)** Ã© expressamente reconhecido e formalizado pela publicaÃ§Ã£o oficial do NIST (**NIST SP 800-145**, SeÃ§Ã£o 2.3).

O NIST define a nuvem comunitÃ¡ria como:
> *"A infraestrutura de nuvem Ã© provisionada para uso exclusivo de uma comunidade especÃ­fica de consumidores pertencentes a organizaÃ§Ãµes que compartilham preocupaÃ§Ãµes em comum (por exemplo, missÃ£o, requisitos de seguranÃ§a, conformidade de polÃ­ticas e regulamentaÃ§Ãµes). Pode pertencer, ser gerenciada e operada por uma ou mais organizaÃ§Ãµes da comunidade, por um terceiro ou por uma combinaÃ§Ã£o deles, e pode residir dentro ou fora de suas instalaÃ§Ãµes."*

**DiferenciaÃ§Ã£o em relaÃ§Ã£o Ã  Nuvem Privada:**

| CritÃ©rio de ComparaÃ§Ã£o | Nuvem Privada (*Private Cloud*) | Nuvem ComunitÃ¡ria (*Community Cloud*) |
| :--- | :--- | :--- |
| **Escopo de Atendimento** | Exclusiva para **uma Ãºnica organizaÃ§Ã£o** (embora atenda mÃºltiplos departamentos internos). | Compartilhada entre **duas ou mais organizaÃ§Ãµes distintas e independentes**, unidas por propÃ³sitos ou regulaÃ§Ãµes comuns. |
| **GovernanÃ§a e Tomada de DecisÃ£o** | Centralizada sob a diretoria e polÃ­ticas exclusivas da empresa proprietÃ¡ria. | Colegiada ou regulamentada por consÃ³rcios, termos de cooperaÃ§Ã£o ou acordos multilaterais entre as entidades participantes. |
| **Rateio de Custos** | Custos operacionais e de capital sÃ£o arcados integralmente pela Ãºnica organizaÃ§Ã£o proprietÃ¡ria. | Custos de infraestrutura, links de alta capacidade e seguranÃ§a sÃ£o divididos e rateados entre os entes da comunidade. |
| **Exemplo PrÃ¡tico** | Data center prÃ³prio de uma empresa de logÃ­stica para seus sistemas internos. | O **GovCloud** ou consÃ³rcios de hospitais universitÃ¡rios de pesquisa genÃ©tica que compartilham poder computacional e datasets genÃ´micos protegidos sob normas idÃªnticas de Ã©tica e sigilo. |

*Fontes primÃ¡rias consultadas:*
- MELL, P.; GRANCE, T. *The NIST Definition of Cloud Computing*. NIST SP 800-145, p. 3, 2011.

---

## BLOCO 2 â€” AS CINCO CARACTERÃSTICAS ESSENCIAIS (NIST)

### 5. Tabela Conceitual e ExemplificaÃ§Ã£o PrÃ¡tica das 5 CaracterÃ­sticas

| CaracterÃ­stica Essencial (NIST) | ExplicaÃ§Ã£o Conceitual (com palavras prÃ³prias) | Exemplo Real em Provedor e DocumentaÃ§Ã£o Oficial |
| :--- | :--- | :--- |
| **Autoatendimento sob demanda** (*On-demand self-service*) | Capacidade do usuÃ¡rio final solicitar, configurar e inicializar recursos computacionais (CPUs, memÃ³ria, discos e regras de rede) unilateralmente e de forma imediata, sem necessidade de enviar tickets manuais, falar com atendentes comerciais ou aguardar aprovaÃ§Ã£o de operadores humanos do provedor. | **AWS EC2 (Elastic Compute Cloud):** O usuÃ¡rio pode inicializar uma instÃ¢ncia virtual em menos de 60 segundos por meio da AWS Management Console, do comando de terminal `aws ec2 run-instances` (AWS CLI) ou de scripts de automaÃ§Ã£o via Terraform.<br>*Ref.:* AWS EC2 Docs â€” *Launch an instance* (https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/LaunchingAndUsingInstances.html). |
| **Amplo acesso Ã  rede** (*Broad network access*) | Os serviÃ§os da nuvem encontram-se disponÃ­veis pela rede de telecomunicaÃ§Ãµes atravÃ©s de protocolos de comunicaÃ§Ã£o universais e padronizados (ex.: HTTP/HTTPS, TLS, REST), viabilizando o consumo a partir de mÃºltiplos dispositivos heterogÃªneos (*smartphones*, *tablets*, *desktops*, clientes web ou terminais de linha de comando). | **Microsoft 365 / Google Workspace:** UsuÃ¡rios editam documentos, planilhas e colaboram em tempo real por meio de navegadores web em desktops Linux/Windows/Mac, bem como atravÃ©s de aplicativos nativos mÃ³veis em Android e iOS, mantendo a sincronia contÃ­nua de dados pela nuvem.<br>*Ref.:* Google Workspace Admin Help â€” *System Requirements* (https://support.google.com/a/answer/33864). |
| **Pool de recursos** (*Resource pooling*) | Os ativos de hardware do provedor (chips de processamento, memÃ³ria RAM, discos rÃ­gidos e interfaces de rede) sÃ£o consolidados em um grande conjunto compartilhado dinamicamente entre mÃºltiplos inquilinos (*multi-tenancy*). Os clientes usufruem de isolamento lÃ³gico estrito sem saber em qual mÃ¡quina fÃ­sica exata seus dados estÃ£o sendo executados. | **Isolamento no AWS Nitro System e Azure Hyper-V:** A AWS descreve que a segregaÃ§Ã£o fÃ­sica/lÃ³gica de clientes Ã© garantida por hardware customizado (*Nitro Cards*) que descarrega a virtualizaÃ§Ã£o da CPU hospedeira, impedindo acesso de memÃ³ria entre instÃ¢ncias de diferentes clientes. No Azure, redes virtuais (*VNets*) utilizam encapsulamento VxLAN para garantir que o trÃ¡fego de um cliente nunca vaze para outro no mesmo switch fÃ­sico.<br>*Ref.:* AWS Security Whitepaper â€” *Compute Isolation* (https://docs.aws.amazon.com/whitepapers/latest/aws-overview-security-processes/compute-isolation.html). |
| **Elasticidade rÃ¡pida** (*Rapid elasticity*) | A infraestrutura pode ser expandida (*scale-out*) ou reduzida (*scale-in*) de maneira Ã¡gil, automÃ¡tica e contÃ­nua, acompanhando diretamente as flutuaÃ§Ãµes de demanda do sistema. Para o cliente consumidor, a capacidade computacional disponÃ­vel aparenta ser inesgotÃ¡vel e pode ser contratada na quantidade exata no momento em que for demandada. | **Azure Virtual Machine Scale Sets (VMSS) / AWS Auto Scaling:** Mecanismos que monitoram mÃ©tricas em tempo real (como consumo de CPU > 70%) e disparam a inicializaÃ§Ã£o automÃ¡tica de dezenas de novas mÃ¡quinas virtuais e containers para suportar o pico, destruindo-os de volta quando o trÃ¡fego diminui.<br>*Ref.:* Azure Docs â€” *Overview of autoscale in Microsoft Azure* (https://learn.microsoft.com/en-us/azure/azure-monitor/autoscale/autoscale-overview). |
| **ServiÃ§o mensurÃ¡vel** (*Measured service*) | O provedor monitora, afere e registra com alta granularidade o uso real de cada unidade de recurso computacional consumido pelo cliente. Esse controle transparente viabiliza o modelo de cobranÃ§a por uso (*pay-as-you-go*), no qual o cliente recebe faturas detalhadas sobre o consumo estrito gerado. | **AWS Billing & CloudWatch / Azure Cost Management:** Exemplos claros de mÃ©tricas mÃ©tricas de cobranÃ§a: tempo de execuÃ§Ã£o de mÃ¡quina virtual faturado por segundo (ex.: vCPU/hora da instÃ¢ncia EC2 t3.medium), volume de dados mantidos no mÃªs em Gigabytes (ex.: GB-mÃªs no Amazon S3) e quantidade de requisiÃ§Ãµes de API executadas (ex.: faturamento por milhÃ£o de invocaÃ§Ãµes no AWS Lambda).<br>*Ref.:* AWS Pricing Principles (https://aws.amazon.com/pricing/). |

---

### 6. Passo a Passo de ConfiguraÃ§Ã£o de Auto Scaling a partir de DocumentaÃ§Ã£o Oficial

**Provedor Escolhido:** Amazon Web Services (AWS)  
**Recurso:** *Auto Scaling Group (ASG)* com InstÃ¢ncias EC2  
**Link da DocumentaÃ§Ã£o Consultada:** <https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-asg-launch-template.html>

#### Passo a Passo TÃ©cnico:

1. **CriaÃ§Ã£o do Launch Template (Modelo de InicializaÃ§Ã£o):**
   - Acesse o Console da AWS e navegue atÃ© **EC2 > Launch Templates > Create launch template**.
   - Defina o nome do modelo (ex.: `web-app-template-v1`).
   - Selecione a imagem de mÃ¡quina (*Amazon Machine Image - AMI*), por exemplo: *Amazon Linux 2023 AMI* ou *Ubuntu Server 22.04 LTS*.
   - Escolha o tipo de instÃ¢ncia (ex.: `t3.micro`).
   - Associe o par de chaves de acesso SSH e selecione um *Security Group* com permissÃ£o de entrada nas portas 80 (HTTP) e 443 (HTTPS).
   - No campo de metadados avanÃ§ados (*User Data*), insira o script de inicializaÃ§Ã£o do servidor web (ex.: script para instalar Nginx e servir a aplicaÃ§Ã£o).
2. **InicializaÃ§Ã£o da CriaÃ§Ã£o do Grupo de Auto Scaling:**
   - No painel esquerdo do EC2, acesse **Auto Scaling Groups** e clique em **Create Auto Scaling group**.
   - No Passo 1, dÃª um nome ao grupo (ex.: `asg-hospital-frontend`) e vincule o *Launch Template* configurado no item anterior.
3. **SeleÃ§Ã£o de Rede e Zonas de Disponibilidade (Alta Disponibilidade):**
   - No Passo 2, selecione a VPC (*Virtual Private Cloud*) de destino.
   - Selecione ao menos duas sub-redes distintas localizadas em **Zonas de Disponibilidade (AZs) diferentes** (ex.: `sa-east-1a` e `sa-east-1b` em SÃ£o Paulo), garantindo resiliÃªncia geogrÃ¡fica fÃ­sica contra panes em data centers individuais.
4. **IntegraÃ§Ã£o com Balanceador de Carga (Opcional, porÃ©m Recomendado):**
   - No Passo 3, selecione a opÃ§Ã£o **Attach to an existing load balancer** ou crie um *Application Load Balancer (ALB)* para distribuir as requisiÃ§Ãµes HTTP entre as instÃ¢ncias criadas pelo grupo.
   - Habilite os *Elastic Load Balancing Health Checks* para que instÃ¢ncias com falha de resposta de aplicaÃ§Ã£o sejam automaticamente substituÃ­das.
5. **DefiniÃ§Ã£o dos Limites de Capacidade (Group Size):**
   - No Passo 4, defina os parÃ¢metros fundamentais de dimensionamento do grupo:
     - **Capacidade Desejada (*Desired Capacity*):** `2` instÃ¢ncias (nÃºmero de servidores mantidos em condiÃ§Ãµes normais de trÃ¡fego).
     - **Capacidade MÃ­nima (*Minimum Capacity*):** `2` instÃ¢ncias (garantia de disponibilidade mÃ­nima tolerante a falhas).
     - **Capacidade MÃ¡xima (*Maximum Capacity*):** `10` instÃ¢ncias (teto mÃ¡ximo para impedir estouro orÃ§amentÃ¡rio).
6. **ConfiguraÃ§Ã£o da PolÃ­tica de Escalonamento AutomÃ¡tico (*Automatic Scaling Policy*):**
   - Escolha a modalidade **Target Tracking Scaling Policy** (polÃ­tica de rastreamento de metas).
   - Defina a mÃ©trica de monitoramento: **UtilizaÃ§Ã£o MÃ©dia de CPU (*Average CPU Utilization*)**.
   - Defina o valor-alvo (*Target Value*): `60%`.
   - *Comportamento resultante:* O serviÃ§o provisionarÃ¡ internamente alarmes no Amazon CloudWatch. Se o consumo mÃ©dio de CPU do grupo ultrapassar 60% por perÃ­odo contÃ­nuo configurado, o Auto Scaling dispararÃ¡ o provisionamento de novas instÃ¢ncias (*scale-out*). Quando o uso cair de volta, o serviÃ§o encerrarÃ¡ gradativamente as instÃ¢ncias excedentes (*scale-in*).
7. **RevisÃ£o e CriaÃ§Ã£o do Grupo:**
   - Revise o resumo de tags, notificaÃ§Ãµes (SNS) e configuraÃ§Ãµes.
   - Clique em **Create Auto Scaling group**. Imediatamente, o serviÃ§o iniciarÃ¡ a execuÃ§Ã£o das instÃ¢ncias desejadas no painel.

---

## BLOCO 3 â€” DESAFIOS DA COMPUTAÃ‡ÃƒO EM NUVEM

### 7. SeguranÃ§a: TrÃªs principais ameaÃ§as em nuvem e mitigaÃ§Ãµes

Segundo o levantamento de referÃªncia internacional da *Cloud Security Alliance (CSA)* (*Top Threats to Cloud Computing*):

1. **AmeaÃ§a 1: ConfiguraÃ§Ãµes Incorretas de SeguranÃ§a e GestÃ£o Inadequada de Recursos (*Misconfiguration*)**
   - *DescriÃ§Ã£o:* Ã‰ historicamente a principal causa de vazamento de dados em nuvem. Ocorre quando serviÃ§os e buckets de armazenamento (como AWS S3 ou Azure Blob Storage) sÃ£o criados com permissÃµes de leitura pÃºblica inadvertidamente, ou quando regras de firewall em nuvem (*Security Groups*) mantÃªm portas crÃ­ticas de gerenciamento (ex.: SSH na porta 22 ou RDP na porta 3389) abertas irrestritamente para a internet (`0.0.0.0/0`).
   - *Controle / PrÃ¡tica de MitigaÃ§Ã£o:* ImplementaÃ§Ã£o contÃ­nua de plataformas de **CSPM (*Cloud Security Posture Management*)** como AWS Security Hub ou Microsoft Defender for Cloud, auditorias automatizadas com ferramentas de Infraestrutura como CÃ³digo (*Checkov, tfsec* nos pipelines de CI/CD) e aplicaÃ§Ã£o de polÃ­ticas de guarda (*AWS Service Control Policies - SCPs*) que bloqueiem a criaÃ§Ã£o de recursos pÃºblicos por padrÃ£o.
2. **AmeaÃ§a 2: Fragilidade no Gerenciamento de Identidades, Credenciais e Acessos (*Identity and Access Management - IAM Failure*)**
   - *DescriÃ§Ã£o:* Comprometimento de credenciais em virtude da ausÃªncia de autenticaÃ§Ã£o multifator (MFA), senhas fracas, chaves de API permanentes codificadas (*hardcoded*) dentro de repositÃ³rios Git pÃºblicos ou concessÃ£o indiscriminada de privilÃ©gios de superusuÃ¡rio (*admin/root* com regras coringa `*.*`).
   - *Controle / PrÃ¡tica de MitigaÃ§Ã£o:* AplicaÃ§Ã£o estrita do **PrincÃ­pio do Menor PrivilÃ©gio (*Principle of Least Privilege*)** com papÃ©is temporÃ¡rios (*IAM Roles / AWS STS*) em vez de chaves estÃ¡ticas; imposiÃ§Ã£o obrigatÃ³ria e inegociÃ¡vel de **AutenticaÃ§Ã£o Multifator (MFA)** para todos os acessos humanos e uso de cofres centralizados de segredos com rotaÃ§Ã£o automÃ¡tica (*AWS Secrets Manager / Azure Key Vault*).
3. **AmeaÃ§a 3: Interfaces e APIs Inseguras (*Insecure Interfaces and APIs*)**
   - *DescriÃ§Ã£o:* Os sistemas de controle e os pontos de contato da nuvem operam inteiramente por meio de APIs HTTP/REST. APIs mal projetadas, desprovidas de autenticaÃ§Ã£o robusta, sem validaÃ§Ã£o de parÃ¢metros de entrada ou sem controle de taxa de requisiÃ§Ãµes, tornam-se vetores fÃ¡ceis para injeÃ§Ã£o de cÃ³digo, ataques de negaÃ§Ã£o de serviÃ§o (DDoS) e exfiltraÃ§Ã£o de dados confidenciais.
   - *Controle / PrÃ¡tica de MitigaÃ§Ã£o:* ImplantaÃ§Ã£o de **API Gateways** centrais para validaÃ§Ã£o de esquemas, exigÃªncia de autenticaÃ§Ã£o e autorizaÃ§Ã£o criptogrÃ¡fica moderna via tokens OAuth 2.0 / OpenID Connect (JWT), imposiÃ§Ã£o de trÃ¡fego exclusivo com **TLS 1.3** e proteÃ§Ã£o perimetral por **WAF (*Web Application Firewall*)** com limitaÃ§Ã£o de requisiÃ§Ãµes (*rate-limiting*).

*Fonte primÃ¡ria:* CLOUD SECURITY ALLIANCE (CSA). *Top Threats to Cloud Computing*. CSA Research, 2024. DisponÃ­vel em: <https://cloudsecurityalliance.org/research/top-threats/>.

---

### 8. Privacidade: Lei Geral de ProteÃ§Ã£o de Dados (LGPD â€” Lei nÂº 13.709/2018)

Ao armazenar e tratar dados pessoais de titulares brasileiros em infraestruturas de computaÃ§Ã£o em nuvem, as organizaÃ§Ãµes devem cumprir obrigaÃ§Ãµes mandatÃ³rias prescritas na LGPD:

- **ObrigaÃ§Ã£o 1: AdoÃ§Ã£o de medidas tÃ©cnicas e de seguranÃ§a adequadas para proteÃ§Ã£o de dados (Art. 46):**
  > *Art. 46. Os agentes de tratamento devem adotar medidas de seguranÃ§a, tÃ©cnicas e administrativas aptas a proteger os dados pessoais de acessos nÃ£o autorizados e de situaÃ§Ãµes acidentais ou ilÃ­citas de destruiÃ§Ã£o, perda, alteraÃ§Ã£o, comunicaÃ§Ã£o ou qualquer forma de tratamento inadequado ou ilÃ­cito.*
  - *AplicaÃ§Ã£o PrÃ¡tica na Nuvem:* As empresas contratantes sÃ£o legalmente obrigadas a assegurar que os serviÃ§os em nuvem possuam criptografia em repouso (usando algoritmos consolidados como AES-256) e em trÃ¢nsito (TLS 1.3), controles estritos de controle de acesso lÃ³gico baseados em funÃ§Ã£o (RBAC), logs auditÃ¡veis de acesso aos dados e planos de continuidade com backups imutÃ¡veis Ã  prova de *ransomware*.
- **ObrigaÃ§Ã£o 2: ComunicaÃ§Ã£o tempestiva de incidentes de seguranÃ§a Ã  autoridade e aos titulares (Art. 48):**
  > *Art. 48. O controlador deverÃ¡ comunicar Ã  autoridade nacional e aos titulares a ocorrÃªncia de incidente de seguranÃ§a que possa acarretar risco ou dano relevante aos titulares.*
  - *AplicaÃ§Ã£o PrÃ¡tica na Nuvem:* Em caso de violaÃ§Ã£o de dados ou ataque cibernÃ©tico que afete o ambiente em nuvem, a empresa controladora nÃ£o pode ocultar o evento; ela Ã© compelida a protocolar comunicaÃ§Ã£o formal junto Ã  ANPD (Autoridade Nacional de ProteÃ§Ã£o de Dados) e alertar os usuÃ¡rios impactados dentro de prazo razoÃ¡vel, discriminando a natureza dos dados vazados, as medidas de contingÃªncia adotadas e os riscos decorrentes.

*Fonte primÃ¡ria:* BRASIL. *Lei nÂº 13.709, de 14 de agosto de 2018*. Lei Geral de ProteÃ§Ã£o de Dados Pessoais (LGPD). DiÃ¡rio Oficial da UniÃ£o, BrasÃ­lia, DF, 2018. DisponÃ­vel em: <http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm>.

---

### 9. Sistemas Legados: Modelo dos "6 Rs" da migraÃ§Ã£o para nuvem

O framework dos "6 Rs" foi concebido para estruturar a jornada de modernizaÃ§Ã£o de portfÃ³lios corporativos legados para a nuvem. Selecionamos trÃªs deles:

1. **Rehost ("Lift and Shift" â€” Migrar e Hospedar):**
   - *Significado:* Consiste em migrar aplicaÃ§Ãµes e bancos de dados do ambiente local diretamente para instÃ¢ncias virtuais na nuvem (IaaS) praticamente sem nenhuma modificaÃ§Ã£o no cÃ³digo-fonte, na arquitetura ou no sistema operacional. Trata-se de "copiar e colar" a carga de trabalho no novo provedor.
   - *CenÃ¡rio mais indicado:* Projetos com prazos operacionais crÃ­ticos e inegociÃ¡veis (ex.: encerramento iminente de contrato de locaÃ§Ã£o de data center fÃ­sico ou fim de vida de hardware corporativo), bem como para sistemas legados consolidados cuja equipe nÃ£o possui conhecimento profundo do cÃ³digo-fonte para arriscar refatoraÃ§Ãµes imediatas.
2. **Replatform ("Lift, Tinker and Shift" â€” Migrar e Ajustar):**
   - *Significado:* Realiza adaptaÃ§Ãµes e substituiÃ§Ãµes pontuais em componentes da arquitetura para aproveitar os benefÃ­cios de serviÃ§os gerenciados em nuvem (PaaS), sem contudo alterar a lÃ³gica essencial e o cÃ³digo principal da aplicaÃ§Ã£o.
   - *CenÃ¡rio mais indicado:* MigraÃ§Ã£o de bancos de dados relacionais legados executados em servidores fÃ­sicos (ex.: Oracle, PostgreSQL, Microsoft SQL Server) para plataformas PaaS totalmente gerenciadas (como Amazon RDS, Azure SQL Database ou Google Cloud SQL). Elimina de imediato a carga de trabalho operacional com rotinas manuais de *patching*, replicaÃ§Ã£o e backups, mantendo a compatibilidade do software intacta.
3. **Refactor / Re-architect (Refatorar e Rearquitetar):**
   - *Significado:* ReimaginaÃ§Ã£o e reescrita profunda da soluÃ§Ã£o com princÃ­pios de desenvolvimento nativo em nuvem (*Cloud-Native*), decompondo sistemas monolÃ­ticos em microsserviÃ§os desacoplados, contÃªineres e arquiteturas serverless orientadas a eventos.
   - *CenÃ¡rio mais indicado:* AplicaÃ§Ãµes de missÃ£o crÃ­tica que representam o diferencial competitivo da empresa (ex.: sistema de pagamentos de um e-commerce ou telemedicina), cujos requisitos exigem extrema elasticidade sob demanda, tempos mÃ­nimos de resposta e deploys contÃ­nuos sem indisponibilidade de versÃ£o.

*Fonte primÃ¡ria:* AWS PRESCRIPTIVE GUIDANCE. *Migration strategy: 6 Rs of cloud migration*. Amazon Web Services, 2024. DisponÃ­vel em: <https://docs.aws.amazon.com/prescriptive-guidance/latest/migration-strategies/welcome.html>.

---

### 10. Cultura Organizacional: Caso real de resistÃªncia Ã  nuvem

**Caso Escolhido:** AdoÃ§Ã£o de Nuvem no Setor Financeiro Brasileiro (Grandes Bancos e Bancos Tradicionais) e o caso da plataforma de streaming **Netflix**.

- **Fatores Geradores de ResistÃªncia:**
  - *No Setor BancÃ¡rio Tradicional:* Historicamente, diretorias executivas, conselhos de administraÃ§Ã£o e equipes tÃ©cnicas de infraestrutura mantinham forte resistÃªncia Ã  nuvem pÃºblica devido ao receio arraigado de violaÃ§Ãµes de seguranÃ§a e vazamentos que acarretassem penalidades regulatÃ³rias extremas e dano Ã  reputaÃ§Ã£o. Adicionalmente, as equipes operacionais de data center temiam a obsolescÃªncia de suas funÃ§Ãµes e perda de controle sobre o ambiente tÃ©cnico.
  - *No caso da Netflix (2008):* Em agosto de 2008, uma corrupÃ§Ã£o catastrÃ³fica de banco de dados em seu data center fÃ­sico prÃ³prio paralisou o envio de DVDs por trÃªs dias seguidos. Quando a lideranÃ§a de engenharia decidiu fechar os data centers e migrar toda a operaÃ§Ã£o para a AWS, houve forte ceticismo interno e externo: a indÃºstria acreditava ser impraticÃ¡vel rodar um negÃ³cio de streaming de vÃ­deo massivo sobre a infraestrutura elÃ¡stica de terceiros, temendo que quedas do provedor aniquilassem o serviÃ§o.
- **Como a ResistÃªncia foi Superada:**
  - *Marco RegulatÃ³rio e GovernanÃ§a no Brasil:* A resistÃªncia do setor bancÃ¡rio foi dirimida quando o Banco Central formalizou parÃ¢metros rÃ­gidos de seguranÃ§a e governanÃ§a de dados na nuvem (ResoluÃ§Ãµes nÂº 4.658/2018 e nÂº 4.893/2021). Os bancos criaram centros de excelÃªncia em nuvem (*Cloud Centers of Excellence - CCoE*) e desenvolveram modelos hÃ­bridos onde a posse e a custÃ³dia das chaves criptogrÃ¡ficas de seguranÃ§a mÃ¡xima ficam sob o domÃ­nio exclusivo do banco (*Bring Your Own Key - BYOK* / HSM dedicado), impedindo que atÃ© o prÃ³prio provedor de nuvem leia os dados transacionais.
  - *Engenharia do Caos na Netflix:* A Netflix superou o ceticismo criando uma nova cultura de engenharia e confiabilidade, pioneira na tÃ©cnica batizada de *Chaos Engineering* (com ferramentas de cÃ³digo aberto como o *Chaos Monkey*). Em vez de esperar que a nuvem nunca falhasse, desenharam seus sistemas assumindo que instÃ¢ncias e zonas falhariam a qualquer momento, testando deliberadamente desligamentos em produÃ§Ã£o para provar a resiliÃªncia arquitetural. Ao mesmo tempo, capacitaram intensamente seu corpo de desenvolvedores, transformando a computaÃ§Ã£o em nuvem no motor propulsor da sua expansÃ£o global.

*Fontes primÃ¡rias:*
- COCKCROFT, Adrian. *Completing the Netflix Cloud Migration*. Netflix TechBlog, 2016. DisponÃ­vel em: <https://netflixtechblog.com/completing-the-netflix-cloud-migration-350c3f3252d4>.
- BANCO CENTRAL DO BRASIL. *ResoluÃ§Ã£o CMN nÂº 4.893/2021*.

---

## BLOCO 4 â€” MODELOS DE SERVIÃ‡O: IAAS, PAAS E SAAS

### 11. Tabela Comparativa de Modelos de ServiÃ§o

A separaÃ§Ã£o de papÃ©is na computaÃ§Ã£o em nuvem orienta-se pelo **Modelo de Responsabilidade Compartilhada (*Shared Responsibility Model*)**:

| CritÃ©rio Analisado | Infraestrutura como ServiÃ§o (**IaaS**) | Plataforma como ServiÃ§o (**PaaS**) | Software como ServiÃ§o (**SaaS**) |
| :--- | :--- | :--- | :--- |
| **O que o Cliente Gerencia** | Sistema Operacional, *runtime*, middleware, configuraÃ§Ãµes de rede interna/firewall, dados da aplicaÃ§Ã£o, rotinas de backup e o cÃ³digo da aplicaÃ§Ã£o. | O cÃ³digo-fonte da aplicaÃ§Ã£o, dados de negÃ³cio, parametrizaÃ§Ãµes e integraÃ§Ãµes da aplicaÃ§Ã£o. | Apenas configuraÃ§Ãµes de conta de usuÃ¡rio, preferÃªncias pessoais e permissÃµes internas de acesso aos dados. |
| **O que o Provedor Gerencia** | VirtualizaÃ§Ã£o, servidores fÃ­sicos, armazenamento de blocos/rede, infraestrutura de data center e climatizaÃ§Ã£o/energia fÃ­sica. | VirtualizaÃ§Ã£o, hardware fÃ­sico, data centers, alÃ©m de todo o Sistema Operacional, instalaÃ§Ã£o de *patches*, *runtimes* de linguagem e escalabilidade da mÃ¡quina. | Absolutamente toda a pilha tecnolÃ³gica: hardware, SO, banco de dados, rede, atualizaÃ§Ãµes do sistema, cÃ³digo do software e correÃ§Ãµes de seguranÃ§a da aplicaÃ§Ã£o. |
| **NÃ­vel de Flexibilidade** | **AltÃ­ssimo:** O cliente detÃ©m controle total para instalar qualquer versÃ£o de SO, kernels customizados, softwares de rede e utilitÃ¡rios especÃ­ficos de baixo nÃ­vel. | **MÃ©dio:** O cliente foca no desenvolvimento do cÃ³digo, devendo respeitar as linguagens, versÃµes de *runtime* e ecossistemas homologados pela plataforma. | **Baixo:** A flexibilidade restringe-se Ã s opÃ§Ãµes de customizaÃ§Ã£o e interfaces disponibilizadas nativamente pelo fabricante do software. |
| **Responsabilidade do Cliente pela SeguranÃ§a** | **Alta:** O cliente deve aplicar atualizaÃ§Ãµes (*patches*) de seguranÃ§a no SO, configurar firewalls de software, proteger portas e criptografar discos manualmente. | **MÃ©dia:** O cliente Ã© responsÃ¡vel por mitigar vulnerabilidades no seu cÃ³digo-fonte (ex.: SQL Injection, XSS) e gerenciar identidades e acessos (IAM). | **MÃ­nima:** O cliente zela apenas pela seguranÃ§a de suas credenciais de acesso (senhas fortes e uso de MFA) e permissÃµes de usuÃ¡rios. |

---

### 12. Dois Provedores Diferentes para Cada Modelo de ServiÃ§o

Abaixo, fornecedores consolidados no mercado tecnolÃ³gico global que divergem dos exemplos bÃ¡sicos de sala de aula:

1. **Infraestrutura como ServiÃ§o (IaaS):**
   - *Provedor 1:* **DigitalOcean** (ServiÃ§o: *DigitalOcean Droplets*) â€” Provedor focado em desenvolvedores e empresas de tecnologia que oferece instÃ¢ncias de mÃ¡quinas virtuais sob demanda com escolha do sistema operacional Linux, IPs dedicados e discos SSD NVMe com precificaÃ§Ã£o previsÃ­vel.
   - *Provedor 2:* **Oracle Cloud Infrastructure - OCI** (ServiÃ§o: *OCI Compute*) â€” Oferece instÃ¢ncias bare-metal dedicadas e mÃ¡quinas virtuais flexÃ­veis de alta performance, bastante utilizadas para cargas de bancos de dados empresariais e modelos de treinamento de IA.
2. **Plataforma como ServiÃ§o (PaaS):**
   - *Provedor 1:* **Render** (ServiÃ§o: *Render Web Services & PostgreSQL*) â€” Plataforma em nuvem totalmente gerenciada que automatiza o *build* e o *deploy* contÃ­nuo de cÃ³digo diretamente do GitHub/GitLab, provisionando containers e certificados TLS automaticamente sem intervenÃ§Ã£o em servidores.
   - *Provedor 2:* **Google App Engine** (Google Cloud) â€” Plataforma clÃ¡ssica de PaaS que permite aos desenvolvedores implantar aplicaÃ§Ãµes monolÃ­ticas ou microsserviÃ§os em linguagens como Python, Java e Go com provisionamento automÃ¡tico de balanceadores de carga e escala automÃ¡tica a zero.
3. **Software como ServiÃ§o (SaaS):**
   - *Provedor 1:* **Salesforce Sales Cloud** â€” Principal plataforma global de CRM (*Customer Relationship Management*), totalmente acessada pelo navegador ou aplicativo para gestÃ£o completa de clientes, pipeline de vendas e funis de marketing sem que a empresa gerencie servidores.
   - *Provedor 2:* **Slack Technologies (Salesforce)** â€” Plataforma corporativa de colaboraÃ§Ã£o e mensageria em tempo real, fornecida integralmente como serviÃ§o na nuvem com criptografia de ponta e integraÃ§Ãµes com ecossistemas externos.

---

### 13. Function as a Service (FaaS) / ComputaÃ§Ã£o Serverless

**Conceito:**  
*Function as a Service* (FaaS) â€” amplamente conhecido como computaÃ§Ã£o *serverless* (ex.: AWS Lambda, Azure Functions, Google Cloud Run/Functions) â€” Ã© um modelo de computaÃ§Ã£o em nuvem orientado a eventos (*event-driven*). Nele, o desenvolvedor escreve blocos isolados e modulares de cÃ³digo (funÃ§Ãµes atÃ´micas e *stateless*) que sÃ£o executadas exclusivamente quando acionadas por um evento externo especÃ­fico (por exemplo: uma requisiÃ§Ã£o HTTP, o upload de um arquivo para um bucket de armazenamento ou uma mensagem recebida em uma fila). NÃ£o hÃ¡ servidores virtuais persistentemente ativos sob a gestÃ£o do cliente; a plataforma orquestra e inicializa o container de execuÃ§Ã£o sob demanda e cobra apenas pela quantidade de milissegundos em que o cÃ³digo esteve em processamento ativo.

**AproximaÃ§Ã£o com os Modelos de ServiÃ§o:**  
O modelo FaaS aproxima-se primordialmente do **PaaS (Plataforma como ServiÃ§o)**, sendo classificado pela literatura e pelo mercado como uma evoluÃ§Ã£o direta e especializada do PaaS (frequentemente denominado *Event-driven PaaS* ou *Serverless PaaS*).

**Justificativa TÃ©cnica:**
- Assim como no PaaS clÃ¡ssico, o FaaS **elimina por completo a necessidade de gerenciar o sistema operacional, patches de seguranÃ§a de kernel, hardware ou capacidade de provisionamento de instÃ¢ncias**.
- Em ambos os modelos, a responsabilidade do cliente estÃ¡ restrita unicamente Ã  lÃ³gica do cÃ³digo da aplicaÃ§Ã£o.
- A principal distinÃ§Ã£o entre o PaaS convencional e o FaaS Ã© a granularidade e o ciclo de vida: enquanto o PaaS tradicional normalmente hospeda uma aplicaÃ§Ã£o web de execuÃ§Ã£o contÃ­nua aguardando requisiÃ§Ãµes em uma porta de rede, o FaaS opera em granularidade de microfunÃ§Ãµes temporÃ¡rias que **escalam a zero (*scale to zero*)** quando ociosas, nÃ£o gerando qualquer custo de mÃ¡quina virtual parada.

---

# PARTE 2 â€” ATIVIDADE PRÃTICA

---

## PRÃTICA 1 â€” MATRIZ COMPARATIVA DE PROVEDORES

Abaixo, a pesquisa comparativa detalhada estruturada a partir da documentaÃ§Ã£o tÃ©cnica primÃ¡ria de trÃªs grandes provedores de nuvem globais:

| CritÃ©rio de ComparaÃ§Ã£o | Provedor 1: Amazon Web Services (AWS) | Provedor 2: Microsoft Azure | Provedor 3: Google Cloud Platform (GCP) |
| :--- | :--- | :--- | :--- |
| **Modelos de implantaÃ§Ã£o oferecidos (pÃºblica / privada / hÃ­brida)** | **PÃºblica:** AWS Global Cloud.<br>**Privada/HÃ­brida:** AWS Outposts (hardware AWS no data center do cliente), AWS Local Zones e AWS Wavelength. | **PÃºblica:** Azure Global Cloud.<br>**Privada/HÃ­brida:** Azure Arc (gestÃ£o unificada on-premise/multicloud) e Azure Stack Hub (execuÃ§Ã£o de IaaS/PaaS local). | **PÃºblica:** Google Cloud Global.<br>**Privada/HÃ­brida:** Google Distributed Cloud (GDC) e GKE Enterprise (antigo Anthos) para gestÃ£o de clusters hÃ­bridos. |
| **Principal serviÃ§o IaaS** | **Amazon EC2 (Elastic Compute Cloud):** Fornecimento de instÃ¢ncias de mÃ¡quinas virtuais configurÃ¡veis e escalÃ¡veis. | **Azure Virtual Machines (Azure VMs):** MÃ¡quinas virtuais sob demanda para Linux e Windows Server. | **Google Compute Engine (GCE):** MÃ¡quinas virtuais flexÃ­veis de alta velocidade com discos persistentes. |
| **Principal serviÃ§o PaaS** | **AWS Elastic Beanstalk** / **AWS App Runner:** OrquestraÃ§Ã£o e deploy automÃ¡tico de aplicaÃ§Ãµes web conteinerizadas. | **Azure App Service:** Plataforma gerenciada para hospedar aplicaÃ§Ãµes web, APIs RESTful e backends mÃ³veis. | **Google App Engine** / **Cloud Run:** Plataforma totalmente gerenciada que executa containers sob demanda com escala a zero. |
| **Principal serviÃ§o SaaS (se houver)** | **Amazon WorkSpaces** (Virtual Desktop) e **Amazon Connect** (Contact Center em nuvem omnichannel). | **Microsoft 365** (Word, Excel, Teams, Exchange Online) e **Dynamics 365** (ERP/CRM). | **Google Workspace** (Gmail, Google Docs, Drive, Meet, Planilhas). |
| **Existe camada gratuita (Free Tier)? Quais limites?** | **Sim.** Possui 3 categorias:<br>â€¢ *12 meses grÃ¡tis:* 750 horas/mÃªs de EC2 `t2.micro` ou `t3.micro`, 5 GB de armazenamento Amazon S3 Standard e 750 horas de banco Amazon RDS.<br>â€¢ *Sempre grÃ¡tis:* 1 milhÃ£o de requisiÃ§Ãµes mensais no AWS Lambda e 10 mÃ©tricas de monitoramento no CloudWatch.<br>*Ref.:* aws.amazon.com/free | **Sim.** Possui 3 categorias:<br>â€¢ *12 meses grÃ¡tis:* 750 horas/mÃªs de VMs B1s (Linux e Windows), 5 GB de armazenamento Azure Blob LRS e 250 GB de Azure SQL Database.<br>â€¢ *Sempre grÃ¡tis:* 1 milhÃ£o de chamadas no Azure Functions e atÃ© 10 apps no Azure App Service F1 tier.<br>â€¢ *CrÃ©dito inicial:* US$ 200 para os primeiros 30 dias.<br>*Ref.:* azure.microsoft.com/free | **Sim.** Possui 2 categorias:<br>â€¢ *Sempre grÃ¡tis:* 1 instÃ¢ncia VM `e2-micro` (com 1 GB de RAM e 30 GB de disco na regiÃ£o dos EUA), 2 milhÃµes de invocaÃ§Ãµes Cloud Functions e 5 GB de Cloud Storage regional.<br>â€¢ *CrÃ©dito de teste:* US$ 300 para novos clientes gastarem em 90 dias.<br>*Ref.:* cloud.google.com/free |
| **RegiÃµes de data center disponÃ­veis no Brasil** | **RegiÃ£o AmÃ©rica do Sul (SÃ£o Paulo):** Identificador tÃ©cnico `sa-east-1`, composta por **3 Zonas de Disponibilidade (AZs)** fisicamente isoladas na Grande SÃ£o Paulo, operando desde 2011. | **RegiÃ£o Brazil South (SÃ£o Paulo):** Operando em SÃ£o Paulo com suporte a mÃºltiplas Zonas de Disponibilidade, complementada pela regiÃ£o secundÃ¡ria *Brazil Southeast* (Rio de Janeiro). | **RegiÃ£o southamerica-east1 (SÃ£o Paulo):** Inaugurada em 2017, composta por **3 Zonas de Disponibilidade (AZs)**, com data centers em SÃ£o Paulo e Vinhedo (SP). |

---

## PRÃTICA 2 â€” PUBLICANDO NA NUVEM (HANDS-ON)

Para atender a esta prÃ¡tica sem exigÃªncia de cadastro de cartÃ£o de crÃ©dito, utilizou-se uma plataforma moderna de **PaaS / Jamstack (GitHub Pages / Vercel / Netlify)** para publicar uma pÃ¡gina web estÃ¡tica com identificaÃ§Ã£o acadÃªmica e sÃ­ntese sobre computaÃ§Ã£o em nuvem.

### 1. CÃ³digo-fonte da PÃ¡gina Web Publicada (`index.html`)

O cÃ³digo abaixo foi desenvolvido com padrÃ£o HTML5/CSS3 responsivo e moderno, pronto para hospedagem:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ComputaÃ§Ã£o em Nuvem I - Atividade PrÃ¡tica</title>
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
            <h1>ComputaÃ§Ã£o em Nuvem I</h1>
            <p>Atividade de Pesquisa e PrÃ¡tica â€” PublicaÃ§Ã£o na Nuvem (Hands-On)</p>
            <div class="meta">
                <div class="meta-item">
                    <span>Estudante</span>
                    <strong>Tiago</strong>
                </div>
                <div class="meta-item">
                    <span>Turma / PerÃ­odo</span>
                    <strong>ComputaÃ§Ã£o em Nuvem I</strong>
                </div>
                <div class="meta-item">
                    <span>Ambiente de Hospedagem</span>
                    <strong>GitHub Pages (PaaS)</strong>
                </div>
            </div>
        </header>

        <section class="card">
            <h2>O que Ã© ComputaÃ§Ã£o em Nuvem?</h2>
            <p>
                Segundo o <strong>NIST SP 800-145</strong>, a computaÃ§Ã£o em nuvem Ã© um modelo para viabilizar o acesso sob demanda e via rede a um pool compartilhado de recursos computacionais configurÃ¡veis (servidores, armazenamento e redes) que podem ser rapidamente provisionados com o mÃ­nimo de esforÃ§o de gerenciamento.
            </p>
            <div class="features-grid">
                <div class="feature-box">
                    <h3>1. Autoatendimento sob Demanda</h3>
                    <p>Provisionamento autÃ´nomo e imediato sem interaÃ§Ã£o com operadores humanos.</p>
                </div>
                <div class="feature-box">
                    <h3>2. Amplo Acesso Ã  Rede</h3>
                    <p>Acessibilidade multiplataforma por protocolos universais de comunicaÃ§Ã£o.</p>
                </div>
                <div class="feature-box">
                    <h3>3. Pool de Recursos</h3>
                    <p>Infraestrutura multi-inquilino com alocaÃ§Ã£o dinÃ¢mica e isolamento seguro.</p>
                </div>
                <div class="feature-box">
                    <h3>4. Elasticidade RÃ¡pida</h3>
                    <p>Capacidade de escalabilidade contÃ­nua e automÃ¡tica acompanhando o trÃ¡fego.</p>
                </div>
                <div class="feature-box">
                    <h3>5. ServiÃ§o MensurÃ¡vel</h3>
                    <p>Telemetria e controle de uso para faturamento transparente por consumo.</p>
                </div>
            </div>
        </section>
        <footer>
            <p>&copy; 2026 â€” Atividade AcadÃªmica de ComputaÃ§Ã£o em Nuvem I</p>
        </footer>
    </div>
</body>
</html>
```

### 2. InstruÃ§Ãµes de Deploy RÃ¡pido (100% Gratuito e sem CartÃ£o):
- **Passo 1:** No [GitHub](https://github.com), crie um repositÃ³rio pÃºblico chamado `nuvem-pratica`.
- **Passo 2:** FaÃ§a o upload do arquivo `index.html` (ou adicione via git).
- **Passo 3:** No repositÃ³rio, acesse **Settings > Pages**. Em *Build and deployment*, na opÃ§Ã£o *Source*, selecione a branch `main` e a pasta `/(root)`, clicando em **Save**.
- **Passo 4:** Em cerca de 1 minuto, o link pÃºblico serÃ¡ gerado no topo da pÃ¡gina.

### 3. InformaÃ§Ãµes da AplicaÃ§Ã£o Publicada:
- **Link PÃºblico:** `https://tiagow2.github.io/Computa-o-em-Nuvem/` *(ou link Vercel/Netlify correspondente)*
- **EvidÃªncia de PublicaÃ§Ã£o:** *(Anexe aqui o print de tela do painel do GitHub Pages / Vercel com status "Deployed" com data e hora visÃ­veis).*

### 4. ParÃ¡grafo Explicativo TÃ©cnico ObrigatÃ³rio:
> A plataforma de publicaÃ§Ã£o utilizada (**GitHub Pages**) representa essencialmente o modelo de serviÃ§o **PaaS (Plataforma como ServiÃ§o)** focado em hospedagem de aplicaÃ§Ãµes web estÃ¡ticas. Nesse modelo, a minha responsabilidade enquanto usuÃ¡rio/desenvolvedor restringiu-se exclusivamente Ã  concepÃ§Ã£o e estruturaÃ§Ã£o do cÃ³digo-fonte (`index.html`) e ao apontamento da branch de publicaÃ§Ã£o no repositÃ³rio. Por outro lado, todo o restante da pilha operacional ficou sob encargo integral do provedor: o provisionamento do servidor web (Nginx), a configuraÃ§Ã£o e emissÃ£o automatizada do certificado criptogrÃ¡fico SSL/TLS para HTTPS, a orquestraÃ§Ã£o do pipeline de integraÃ§Ã£o contÃ­nua (CI/CD via GitHub Actions), a distribuiÃ§Ã£o global do conteÃºdo em nÃ³s de CDN (*Content Delivery Network*) com proteÃ§Ã£o contra ataques de negaÃ§Ã£o de serviÃ§o (DDoS), bem como toda a manutenÃ§Ã£o do sistema operacional subjacente e da infraestrutura fÃ­sica do data center.

---

## PRÃTICA 3 â€” ESTUDO DE CASO: DESENHO DE ARQUITETURA HÃBRIDA

### O CenÃ¡rio do Hospital:
> *Um hospital de mÃ©dio porte deseja modernizar sua infraestrutura de TI. Ele precisa manter os prontuÃ¡rios eletrÃ´nicos de pacientes (dados sensÃ­veis, sujeitos Ã  LGPD) sob total controle interno, mas tambÃ©m quer usar aplicaÃ§Ãµes de agendamento online e um sistema de telemedicina que apresentam picos de acesso variÃ¡veis ao longo do dia.*

---

### a. Quais partes do sistema vocÃª colocaria em nuvem privada, e quais em nuvem pÃºblica? Justifique com base nas caracterÃ­sticas de privacidade e elasticidade estudadas.

**Proposta de DivisÃ£o Arquitetural:**

1. **Componentes Alocados na Nuvem Privada (Data Center Interno do Hospital):**
   - **Banco de Dados Central de ProntuÃ¡rios EletrÃ´nicos dos Pacientes (PEP):** HistÃ³rico clÃ­nico, laudos mÃ©dicos, prescriÃ§Ãµes farmacolÃ³gicas e exames diagnÃ³sticos de alta resoluÃ§Ã£o (PACS/DICOM).
   - **Servidor de Chaves CriptogrÃ¡ficas (HSM):** Armazenamento de chaves mestras e controle estrito de autenticaÃ§Ã£o de mÃ©dicos e equipe assistencial.
   - **Justificativa de Privacidade (LGPD):** Dados relativos Ã  saÃºde sÃ£o classificados legalmente pelo Art. 5Âº, inciso II da LGPD como **dados pessoais sensÃ­veis**, exigindo rigor mÃ¡ximo de proteÃ§Ã£o. Manter o repositÃ³rio central na nuvem privada garante ao hospital a custÃ³dia e o controle fÃ­sico irrestrito das mÃ­dias de armazenamento, auditoria local direta e garantia de que nenhum dado sensÃ­vel sairÃ¡ da jurisdiÃ§Ã£o fÃ­sica institucional sem autorizaÃ§Ã£o prÃ©via. AlÃ©m disso, a rede local hospitalar assegura latÃªncia ultrabaixa (< 5ms) para acesso a imagens mÃ©dicas pesadas nos computadores de centros cirÃºrgicos e UTIs, sem vulnerabilidade a eventuais interrupÃ§Ãµes de links externos de internet.

2. **Componentes Alocados na Nuvem PÃºblica (ex.: AWS, Azure ou Google Cloud):**
   - **Portal Web e Aplicativo Mobile de Agendamento de Consultas:** Interface pÃºblica de autoatendimento para pacientes.
   - **Plataforma de VideoconferÃªncia e Salas Virtuais de Telemedicina:** ServiÃ§os de *streaming* de Ã¡udio/vÃ­deo WebRTC, salas de espera virtual e fila de triagem remota.
   - **MicrosserviÃ§o de NotificaÃ§Ãµes:** Disparo de lembretes e confirmaÃ§Ãµes por WhatsApp/SMS e e-mail.
   - **Justificativa de Elasticidade:** AplicaÃ§Ãµes voltadas ao pÃºblico externo apresentam padrÃµes de acessos com **picos sazonais extremos e imprevisÃ­veis** (por exemplo: abertura de agendas de especialistas no primeiro dia do mÃªs ou campanhas de vacinaÃ§Ã£o). A nuvem pÃºblica oferece o pilar da **elasticidade rÃ¡pida** (*Auto Scaling* e balanceamento de carga), provisionando novos contÃªineres e largura de banda instantaneamente durante os picos e encolhendo os recursos na madrugada, evitando desperdÃ­cio de investimentos em servidores locais que ficariam ociosos a maior parte do tempo.

---

### b. Essa arquitetura seria classificada como nuvem hÃ­brida? Explique por quÃª.

**Sim.** A soluÃ§Ã£o desenhada enquadra-se rigorosamente na definiÃ§Ã£o clÃ¡ssica de **Nuvem HÃ­brida** estabelecida pelo NIST SP 800-145.

**Justificativa TÃ©cnica:**
A arquitetura Ã© composta pela coexistÃªncia de duas infraestruturas de nuvem conceitualmente distintas:
- Uma **nuvem privada** (executada no data center do hospital para governanÃ§a dos dados sensÃ­veis do PEP); e
- Uma **nuvem pÃºblica** (hospedada em provedor externo para executar as aplicaÃ§Ãµes elÃ¡sticas de agendamento e telemedicina).

Elas permanecem como entidades operacionais Ãºnicas e autÃ´nomas, mas sÃ£o **intrinsecamente interligadas e orquestradas por meio de canais de comunicaÃ§Ã£o seguros e padronizados** â€” especificamente um tÃºnel de VPN IPsec corporativo com criptografia AES-GCM-256 redundante ou link dedicado direto (*AWS Direct Connect* / *Azure ExpressRoute*). 

O sistema de agendamento na nuvem pÃºblica comunica-se com a nuvem privada exclusivamente por meio de chamadas de API autenticadas e controladas por um *API Gateway* com regras de validaÃ§Ã£o rigorosas. Dessa forma, hÃ¡ troca fluida e portabilidade de fluxos de trabalho entre os dois ambientes sem que a base de dados interna fique diretamente exposta Ã  internet pÃºblica.

---

### c. Que desafios (dos quatro estudados: seguranÃ§a, privacidade, legado, cultura) vocÃª espera que essa migraÃ§Ã£o enfrente no hospital, e como mitigÃ¡-los?

| Eixo de Desafio | DescriÃ§Ã£o do Desafio EspecÃ­fico no Hospital | Plano de MitigaÃ§Ã£o TÃ©cnico e Organizacional |
| :--- | :--- | :--- |
| **1. SeguranÃ§a** | O elo de comunicaÃ§Ã£o que integra a nuvem pÃºblica Ã  nuvem privada interna (APIs de telemedicina e agendamento) torna-se um alvo atrativo para ataques cibernÃ©ticos, injeÃ§Ã£o de comandos maliciosos e sequestro de dados (*ransomware*). | â€¢ Estabelecer arquitetura **Zero Trust** (nenhum componente confia cegamente no outro).<br>â€¢ TrÃ¡fego de interconexÃ£o canalizado estritamente por tÃºnel VPN criptografado com TLS 1.3 / IPsec dedicado.<br>â€¢ Posicionamento de um *Web Application Firewall (WAF)* e *API Gateway* com autenticaÃ§Ã£o mÃºtua (mTLS) e limitaÃ§Ã£o de taxa (*rate limiting*).<br>â€¢ Criptografia total de ponta a ponta dos dados em trÃ¢nsito e em repouso. |
| **2. Privacidade (LGPD)** | Risco de vazamento de dados de prontuÃ¡rios mÃ©dicos durante as transmissÃµes de telemedicina ou armazenamento inadvertido de dados de pacientes em caches/logs da nuvem pÃºblica em desconformidade com a LGPD. | â€¢ Implementar tÃ©cnicas de **anonimizaÃ§Ã£o ou pseudonimizaÃ§Ã£o** de identificadores de pacientes na camada pÃºblica (o portal web trafega apenas IDs aleatÃ³rios e *tokens*, nunca o CPF ou histÃ³rico clÃ­nico descriptografado).<br>â€¢ ConfiguraÃ§Ã£o estrita de regras de retenÃ§Ã£o nos serviÃ§os da nuvem pÃºblica para apagar logs transitÃ³rios imediatamente apÃ³s a conclusÃ£o da consulta remota.<br>â€¢ ElaboraÃ§Ã£o formal do RelatÃ³rio de Impacto Ã  ProteÃ§Ã£o de Dados Pessoais (RIPD). |
| **3. Sistemas Legados** | O sistema de prontuÃ¡rio eletrÃ´nico antigo do hospital comumente opera em arquitetura monolÃ­tica, cliente-servidor tradicional ou em bancos relacionais antigos sem suporte nativo a chamadas de API modernas (REST/JSON), gerando atrito de integraÃ§Ã£o. | â€¢ AdoÃ§Ã£o da estratÃ©gia de migraÃ§Ã£o **Replatform** ou **Refactor parcial**, criando uma camada intermediÃ¡ria de microsserviÃ§os desacoplados (*BFF â€” Backend for Frontend* ou padrÃ£o *Strangler Fig*).<br>â€¢ Essa camada atua como adaptador / ponte de traduÃ§Ã£o, convertendo as consultas das APIs modernas em instruÃ§Ãµes que o banco legado compreende sem necessidade de substituir o software hospitalar imediatamente. |
| **4. Cultura Organizacional** | ResistÃªncia do corpo clÃ­nico (mÃ©dicos e enfermeiros) ao uso de novas interfaces de telemedicina e agendamento, aliada ao receio da equipe interna de TI do hospital de perder relevÃ¢ncia e controle com a terceirizaÃ§Ã£o de parte dos sistemas para a nuvem. | â€¢ Instituir um comitÃª de GestÃ£o de MudanÃ§a (*Change Management*), envolvendo mÃ©dicos-chave desde a fase de testes e prototipagem da telemedicina para garantir ergonomia de uso.<br>â€¢ Promover programas de capacitaÃ§Ã£o e reciclagem tÃ©cnica para os analistas de TI locais em computaÃ§Ã£o em nuvem e DevOps, demonstrando que eles se tornarÃ£o gestores estratÃ©gicos de nuvem hÃ­brida e seguranÃ§a, e nÃ£o apenas operadores de hardware. |

---

# REFERÃŠNCIAS BIBLIOGRÃFICAS (NORMAS ABNT)

1. AMAZON WEB SERVICES (AWS). **Overview of Amazon Web Services: AWS Whitepapers**. Seattle: Amazon, 2024. DisponÃ­vel em: <https://docs.aws.amazon.com/whitepapers/latest/aws-overview/aws-overview.pdf>. Acesso em: 14 set. 2026.
2. BANCO CENTRAL DO BRASIL (BACEN). **ResoluÃ§Ã£o CMN nÂº 4.893, de 26 de fevereiro de 2021**. DispÃµe sobre a polÃ­tica de seguranÃ§a cibernÃ©tica e sobre os requisitos para a contrataÃ§Ã£o de serviÃ§os de processamento e armazenamento de dados e de computaÃ§Ã£o em nuvem a serem observados pelas instituiÃ§Ãµes financeiras. BrasÃ­lia: DiÃ¡rio Oficial da UniÃ£o, 2021.
3. BRASIL. **Lei nÂº 13.709, de 14 de agosto de 2018**. DispÃµe sobre o tratamento de dados pessoais, inclusive nos meios digitais (Lei Geral de ProteÃ§Ã£o de Dados Pessoais - LGPD). BrasÃ­lia: DiÃ¡rio Oficial da UniÃ£o, 2018. DisponÃ­vel em: <http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm>. Acesso em: 14 set. 2026.
4. CLOUD SECURITY ALLIANCE (CSA). **Top Threats to Cloud Computing**. CSA Research, 2024. DisponÃ­vel em: <https://cloudsecurityalliance.org/research/top-threats/>. Acesso em: 14 set. 2026.
5. COCKCROFT, Adrian. **Completing the Netflix Cloud Migration**. Netflix Technology Blog, 2016. DisponÃ­vel em: <https://netflixtechblog.com/completing-the-netflix-cloud-migration-350c3f3252d4>. Acesso em: 14 set. 2026.
6. ERL, Thomas; PUTTINI, Ricardo; MAHMOOD, Zaigham. **Cloud Computing: Concepts, Technology & Architecture**. Upper Saddle River: Prentice Hall / Pearson, 2013.
7. GOOGLE CLOUD. **Google Cloud documentation and architecture center**. Google, 2024. DisponÃ­vel em: <https://cloud.google.com/docs>. Acesso em: 14 set. 2026.
8. MELL, Peter; GRANCE, Timothy. **The NIST Definition of Cloud Computing**. NIST Special Publication 800-145. Gaithersburg: National Institute of Standards and Technology (NIST), U.S. Department of Commerce, 2011. DisponÃ­vel em: <https://doi.org/10.6028/NIST.SP.800-145>. Acesso em: 14 set. 2026.
9. MICROSOFT AZURE. **Microsoft Azure Documentation and Architecture Guidelines**. Redmond: Microsoft, 2024. DisponÃ­vel em: <https://learn.microsoft.com/en-us/azure/>. Acesso em: 14 set. 2026.

