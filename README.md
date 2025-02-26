# Resumo do Lab Microsoft Azure - Localizando Serviços por Categoria

Existem inúmeros serviços para suprir as diversas necessidades e todos estão organizados em categorias.

---

Em cada categoria também há uma divisão por assuntos como é o exemplo da Categoria `Análise`, há o assunto `Processamento de Big Data` com os itens:

- Analysis Services
- Clusters HDInsight
- Data Factories
- Data Lake Analytics
- Data Lake Storage Gen1
- Azure Databricks
- Microsoft Graph Data Connect
- Azure HDInsight em clusters AKS

Essa divisão permite com facilidade a localização do serviço dentro da console da Azure.

---

## 🛡️ SLA E ALTA DISPONIBILIDADE

O nível de acordo de serviço ou SLA (Service Level Agreement) é o tempo que o Cloud Provider oferece de disponibilidade do serviço. Quando o valor é 99%, o tempo é de 1,68 horas por semana e 7,2 horas por mês. Se o SLA é de 99,9%, o tempo já diminui significativamente para 10,1 minutos por semana e 43,6 minutos por mês.

Ao criar uma máquina virtual, é possível configurá-la com redundância em outros servidores ou localidades para aumentar a disponibilidade. Isso pode ser útil em estratégias como ambientes resistentes a desastres, onde o ambiente pode estar disponível em outro lugar, ou para aumentar a velocidade de acesso, pois a informação será oriunda de vários lugares.

É importante alinhar bem a arquitetura do sistema e validar a infraestrutura que será usada, pois as cobranças podem aumentar significativamente.

## 🖥️ Criação de Máquina Virtual / Imagem e Arquitetura

No painel de criação da máquina virtual, é possível ver o valor estimado que será cobrado pela máquina e sobre a responsabilidade. É possível configurar itens como:

- Reinício automático
- Monitoramento
- Discos
- Peças
- Modelo de redundância

## 🌍 Data Centers - Globo

O site datacenters.microsoft.com/globe/explore oferece um mapa interativo, em 2D ou 3D, que permite visualizar a localização dos datacenters da Microsoft ao redor do mundo. Ele exibe as regiões do Azure, suas geografias e outras informações relacionadas à infraestrutura global da Microsoft. O mapa pode ser filtrado por diferentes categorias e também oferece uma visão geral da presença global da plataforma Azure.

## 🖥️ Criação de Máquinas Virtuais e Área de Trabalho Remoto

A criação de máquinas virtuais no Azure é simples e oferece diversas configurações que facilitam a gestão da infraestrutura. Todas as máquinas e recursos configurados no Azure precisam de um grupo de recursos, e esta é a segunda configuração ao criar uma máquina virtual. Além disso, é possível configurar:

- Nome da máquina
- Região
- Zona de disponibilidade
- Tipo de segurança
- Sistema operacional
- Tamanhos
- Tipo de autenticação
- Criar um usuário administrador

Entre outras configurações, é possível também configurar:

- Disco
- Rede
- Gerenciamento
- Monitoração

Também é possível configurar outras opções úteis para a governança e configuração de máquinas virtuais, como desktop remoto, para facilitar a disponibilidade de máquinas para funcionários sem precisar fornecer um computador ao usuário.

## 💾 Armazenamento

Para fazer uma configuração de armazenamento, a assinatura já vem configurada e deve ser escolhido o grupo de recursos. O nome da conta de armazenamento deve ser único.

OBS.: Conta de armazenamento é o nome do armazenamento que está sendo criado.

- Região: Deve ser escolhida de acordo com os requisitos de latência ou custo.
- Desempenho: Pode ser escolhido o `Standard` ou `Premium`, que determinará a latência.
- Redundância: Pode ser usada LRS (local), GRS (geográfica), ZRS (zona) e GZRS (zona geográfica), que determinará o tipo de redundância que este armazenamento deverá ter.

Outras configurações permitem a escolha do tipo de armazenamento (frio ou quente), configuração de rede, criptografia e outras opções.

### 📂 Menu: Armazenamento de Dados

Configuração de armazenamento, recebimento, compartilhamento e organização de dados e arquivos do Azure.

- Containers: Gerenciamento de pastas (é possível também já configurar um backup)
- Compartilhamento de arquivos: Ferramenta para criar uma conexão usando o menu `Conectar`, disponível para conexão SMB para Windows, Linux e Mac.
- Filas: Configuração de mensageria
- Tabelas: Criação de tabelas

### 🚚 Migração de Dados

É possível criar um projeto de migração que viabiliza migrar arquivos e dados da estrutura on-premises para a cloud usando ferramentas como o AZ Copy ou o Azure Data Box.

- AZ Copy: Aplicação simples e leve para usar no terminal para transportar arquivos, disponível para Linux, Windows e Mac.
- Azure Data Box: Modalidade de transporte de dados com um disco rígido que é enviado para o cliente, o cliente escreve os dados no disco e encaminha de volta ao Azure para subir na nuvem. O limite dessa modalidade é de 80TB.
- Data Box Disk: Limite de 35TB
- Data Box Heavy: Limite de 800TB
- Data Box Job: Limite de 1TB

Cada serviço do Azure Data Box possui valores diferentes.

### 🗄️ Gerenciador de Armazenamento do Microsoft Azure

Aplicação para gestão de armazenamento. Basta baixar, instalar e fazer a sincronização, e a console irá mostrar as assinaturas, contas de armazenamento e mais.

## 🔐 Identidade e Segurança (ENTRA ID)

Todo usuário deve ser gerenciado no Azure através do Entra ID, que determinará funções e permissões dos usuários. É diferente do RBAC, pois os usuários gerenciados nessa seção terão permissão apenas para gerenciamento dentro do Entra ID, com permissões para mudanças na gestão de usuários.

É possível criar usuários e convidar usuários externos, inclusive em grupo.

- Entra Connect: Sincroniza os usuários do ambiente on-premises para o ambiente de cloud.

Uma conta deletada tem até 30 dias para ser recuperada.

### 🛡️ Defender for Cloud

Aplicação cloud native e híbrida que traz informações sobre a segurança do ambiente.

- Recomendação de segurança: Validador de segurança e sugestão de melhorias.

## 💰 CALCULADORAS DE CUSTOS

Existem duas calculadoras dentro do Azure. Uma é ideal para as estimativas de preços dos recursos do Azure e a outra serve para cálculo de economia na migração de on-premises para o Azure.

Essa segunda calculadora é chamada de TCO (Total Cost of Ownership), ou seja, é a calculadora de custo total de propriedade.

A importância do uso dessas calculadoras dá-se à necessidade de que a empresa precisa avaliar os valores e elencar o que faz sentido ou reduzir o risco de custos inesperados.

## 🛠️ Portal de Confiança do Serviço

É um portal de governança com diversas ferramentas.

- Normas de auditoria que a Microsoft obedece para estar em compliance. É um local onde podemos validar quais são as regras de cada país e como são aplicadas.
- Bloqueio de recursos
- Purview

## 🚀 Ferramentas de Implantação do Azure

- Cloud Shell: É um botão que abre a ferramenta de execução de comandos PowerShell ou Bash. Para usar, é necessário um storage account.

O Bicep auxilia na automação de criação de máquinas virtuais.

O Azure Arc é uma ferramenta de gestão de máquinas fora do Azure. Com o ARC, é possível fazer atualização e acesso remoto direto na console.

## 📊 Ferramentas de Monitoramento do Azure

No Azure, há diversas ferramentas para monitorar o ambiente, verificar a saúde dos recursos e receber recomendações.

- Azure Monitor: Uma ferramenta completa com insights para análises com uma visão ampla de toda a estrutura. Validação de serviço.
- Service Health: Um painel de visualização da saúde e manutenções agendadas que mostram se há algum ponto em degradação.
- Advisor: Traz recomendações sobre a infraestrutura que garantem benefícios.

### 🧑‍🏫 Expert [Dio](https://www.dio.me)

- [Valéria Baptista | LinkedIn](https://www.linkedin.com/in/valeriabaptista/)
  
Head of Cloud and Cybersecurity, CloudData Tech & DevOps

### 📲 Follow me

- [MARCIO ADRIANO DA SILVA | LinkedIn](https://www.linkedin.com/in/mads1974/)
