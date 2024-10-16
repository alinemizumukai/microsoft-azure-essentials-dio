# Ferramentas de Implantação no Microsoft Azure

Este guia contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

## Índice
- [Introdução](#introdução)
- [Ferramentas para gerenciar o ambiente](#ferramentas-para-gerenciar-o-ambiente)
    - [Portal do Azure](#portal-do-azure)
    - [Azure Cloud Shell](#azure-cloud-shell)
    - [Azure PowerShell](#azure-powershell)
    - [CLI do Azure](#cli-do-azure)
- [Azure Arc](#azure-arc)
- [Azure Resource Manager](#azure-resource-manager)
    - [Infraestrutura como código](#infraestrutura-como-código)
    - [Modelos de ARM](#modelos-de-arm)
    - [Bicep](#bicep)
- [Documentação Adicional](#documentação-adicional)

## Introdução

Este desafio consiste em explorar o portal do Microsoft Azure, analisando ferramentas para interagir com o Microsoft Azure.

## Ferramentas para gerenciar o ambiente

O  Azure fornece várias ferramentas para gerenciar seu ambiente, incluindo:
- Portal do Azure
- Azure PowerShell
- CLI (Interface de Linha de Comando) do Azure.

### Portal do Azure

O portal do Azure é um console unificado baseado na Web que fornece uma alternativa para as ferramentas de linha de comando. Com o portal do Azure, você pode gerenciar a assinatura do Azure usando uma interface gráfica do usuário.

O portal do Azure foi projetado para ter resiliência e disponibilidade contínua. Ele mantém uma presença em todos os datacenters do Azure. Essa configuração torna-o resiliente a falhas de datacenters individuais e evita a lentidão da rede ao se manter perto dos usuários. O portal é atualizado continuamente e não requer nenhum tempo de inatividade para atividades de manutenção.

### Azure Cloud Shell

O Azure Cloud Shell é uma ferramenta de shell baseada em navegador que permite criar, configurar e gerenciar recursos do Azure usando um shell. O Azure Cloud Shell dá suporte ao Azure PowerShell e à CLI (Interface de Linha de Comando) do Azure, que é um shell bash.

![Acesso ao Cloud Shell](azure-power-shell.png)

O Azure Cloud Shell tem vários recursos que o tornam uma oferta exclusiva para dar suporte ao gerenciamento do Azure.
- É uma experiência de shell baseada em navegador sem a necessidade de instalação ou configuração local.
- Ele é autenticado em suas credenciais do Azure, portanto, quando você faz logon, ele sabe inerentemente quem você é e quais permissões você tem.
- Você escolhe o shell com o qual está mais familiarizado; o Azure Cloud Shell dá suporte ao Azure PowerShell e à CLI do Azure (que usa o Bash).

### Azure PowerShell

O Azure PowerShell é um shell com o qual desenvolvedores, DevOps e profissionais de TI podem executar comandos chamados de command-lets (cmdlets). Esses comandos chamam a API REST do Azure para realizar tarefas de gerenciamento no Azure.

Os cmdlets podem ser executados de modo independente para lidar com alterações pontuais ou ser combinados para ajudar a orquestrar ações complexas como:
- A configuração, desinstalação e manutenção de rotina de um único recurso ou de vários recursos conectados.
- A implantação de uma infraestrutura inteira, que pode conter dezenas ou centenas de recursos, de um código imperativo.

### CLI do Azure

A CLI do Azure é funcionalmente equivalente ao Azure PowerShell, sendo a principal diferença a sintaxe dos comandos. Enquanto o Azure PowerShell usa comandos do PowerShell, a CLI do Azure usa comandos Bash.

A CLI do Azure fornece os mesmos benefícios de lidar com tarefas separadas ou orquestrar operações complexas por meio do código. Ele também pode ser instalado nas plataformas Windows, Linux e Mac, bem como por meio do Azure Cloud Shell.

## Azure Arc

Ao utilizar o ARM (Azure Resource Manager), o Arc permite estender a conformidade e o monitoramento do Azure para suas configurações híbridas e multinuvem. O Azure Arc simplifica a governança e o gerenciamento ao fornecer uma plataforma de gerenciamento local e de várias nuvens consistente.

O Azure Arc fornece uma forma centralizada e unificada para:
- Gerenciar todo o ambiente projetando os recursos que não são do Azure no ARM.
- Gerenciar máquinas virtuais híbridas e de várias nuvens, clusters do Kubernetes e bancos de dados como se eles estivessem em execução no Azure.
- Usar as funcionalidades familiares de gerenciamento e serviços do Azure, independentemente de onde eles estejam hospedados.
- Continuar usando a ITOps tradicional, introduzindo práticas de DevOps para dar suporte a novos padrões nativos de nuvem no seu ambiente.
- Configurar localizações personalizadas como uma camada de abstração no cluster de Kubernetes habilitado para Azure Arc e nas extensões de cluster.

## Azure Resource Manager

O ARM (Azure Resource Manager) é o serviço de implantação e gerenciamento do Azure. Ele fornece uma camada de gerenciamento que lhe permite criar, atualizar e excluir recursos em sua conta do Azure. Sempre que você faz qualquer coisa com seus recursos do Azure, o ARM está envolvido.

Quando um usuário envia uma solicitação de ferramentas, APIs ou SDKs do Azure, o ARM recebe a solicitação. O ARM se autentica e autoriza a solicitação. Então, o ARM envia a solicitação para o serviço do Azure, que executa a ação solicitada. Você vê resultados e recursos consistentes em todas as diferentes ferramentas porque todas as solicitações são tratadas por meio da mesma API.

### Infraestrutura como código

A infraestrutura como código é um conceito em que você gerencia sua infraestrutura como linhas de código. Em um nível introdutório, é como usar o Azure Cloud Shell, Azure PowerShell ou a CLI do Azure para gerenciar e configurar seus recursos. À medida que você fica mais confortável na nuvem, você pode usar a infraestrutura como conceito de código para gerenciar implantações inteiras usando modelos e configurações repetíveis. Os modelos do ARM e o Bicep são dois exemplos de como usar a infraestrutura como código com o Azure Resource Manager para manter seu ambiente.

### Modelos de ARM

Ao usar os modelos do ARM, você pode descrever os recursos que deseja usar em um formato JSON declarativo. Com um modelo do ARM, o código de implantação é verificado antes da execução de qualquer código. Isso garante que os recursos serão criados e conectados corretamente. Em seguida, o modelo orquestra a criação desses recursos em paralelo. Ou seja, se você precisar de 50 instâncias do mesmo recurso, todas as 50 instâncias serão criadas ao mesmo tempo.

### Bicep

O Bicep é uma linguagem que usa sintaxe declarativa para implantar recursos do Azure. Um arquivo Bicep define a infraestrutura e a configuração. Em seguida, o ARM implanta esse ambiente com base no arquivo Bicep. Embora semelhante a um modelo do ARM, que é escrito em JSON, os arquivos Bicep tendem a usar um estilo mais simples e conciso.

## Documentação adicional

[Documentação Oficial do Microsoft Azure](https://docs.microsoft.com/azure).

[Azure Arc](https://learn.microsoft.com/pt-br/azure/azure-arc/).

[Azure Resource Manager](https://azure.microsoft.com/pt-br/get-started/azure-portal/resource-manager).