# Segurança e Identidade no Microsoft Azure

Este guia contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

## Índice
- [Introdução](#introdução)
- [Microsoft Entra ID](#microsoft-entra-id)
- [Microsoft Defender for Cloud](#microsoft-defender-for-cloud)
- [Documentação Adicional](#documentação-adicional)

## Introdução

Este desafio consiste em explorar o portal do Microsoft Azure, analisando alguns produtos de Segurança e Identidade do Microsoft Azure, como por exemplo o Microsoft Entra ID e o Microsoft Defender for Cloud.

O Microsoft Entra ID (antigo Active Directory) é um serviço de gerenciamento de identidade e acesso baseado em nuvem que permite que seus funcionários acessem recursos externos. Exemplos de recursos incluem o Microsoft 365, o portal do Azure e milhares de outros aplicativos SaaS.

O Microsoft Defender for Cloud é uma plataforma de CNAPP (proteção de aplicativo nativo de nuvem) composta de medidas e práticas de segurança projetadas para proteger os aplicativos baseados em nuvem contra várias ameaças e vulnerabilidades cibernéticas. 

## Microsoft Entra ID

O Microsoft Entra ID é um serviço de diretório que permite que você faça login e acesse tanto os aplicativos de nuvem da Microsoft quanto os aplicativos de nuvem que você desenvolver. O Microsoft Entra ID também pode ajudar você a manter sua implantação do Active Directory local.

O Microsoft Entra ID fornece serviços como:
- Autenticação: inclui verificar a identidade para acessar aplicativos e recursos. Também inclui fornecer funcionalidades como redefinição de senha por autoatendimento, autenticação multifator, uma lista personalizada de senhas banidas e serviços de bloqueio inteligente.
- Logon único: o SSO (logon único) permite que você se lembre apenas de um nome de usuário e uma senha para acessar vários aplicativos. Uma única identidade é vinculada a um usuário, o que simplifica o modelo de segurança. À medida que os usuários trocam de funções ou saem de uma organização, as modificações de acesso são vinculadas àquela identidade, o que reduz consideravelmente o esforço necessário para alterar ou desabilitar contas.
- Gerenciamento de aplicativos: Você pode gerenciar seus aplicativos de nuvem e locais usando o Microsoft Entra ID. Recursos como Proxy de Aplicativo, aplicativos SaaS, o portal Meus Aplicativos e o logon único proporcionam uma experiência do usuário aprimorada.
- Gerenciamento de dispositivos: Além de seu uso com as contas individuais de uma pessoa, o Microsoft Entra ID dá suporte ao registro de dispositivos. O registro permite que os dispositivos sejam gerenciados por meio de ferramentas como o Microsoft Intune. Também permite que políticas de Acesso Condicional baseadas no dispositivo restrinjam tentativas de acesso somente às provenientes de dispositivos conhecidos, independentemente da conta de usuário solicitante.

## Microsoft Defender for Cloud

O Microsoft Defender for Cloud é uma plataforma de proteção de aplicativos nativa da nuvem (CNAPP) com um conjunto de medidas e práticas de segurança projetadas para proteger seus aplicativos baseados em nuvem de ponta a ponta combinando os seguintes recursos:
- Uma solução de operações de segurança de desenvolvimento (DevSecOps) que unifica o gerenciamento de segurança no nível do código em ambientes multinuvem e de vários pipelines
- Uma solução de CSPM (gerenciamento da postura de segurança na nuvem) que apresenta ações que você pode executar para evitar violações
- Uma CWPP (plataforma de proteção de carga de trabalho de nuvem) com proteções específicas para servidores, contêineres, armazenamento, bancos de dados e outras cargas de trabalho

O Defender ajuda a encontrar e corrigir vulnerabilidades de segurança e também aplica controles de acesso e de aplicativos para bloquear atividades mal-intencionadas, detectar ameaças usando a análise e a inteligência e responder rapidamente quando estiver sob ataque.

A página de Overview fornece uma visão unificada da postura de segurança das suas cargas de trabalho de nuvem híbrida, ajudando você a descobrir e avaliar a segurança das suas cargas de trabalho e a identificar e mitigar riscos.

Você pode exibir e filtrar sua lista de assinaturas no menu de assinaturas para que o Defender para Nuvem ajuste a exibição da página de visão geral para refletir a postura de segurança das assinaturas selecionadas.

Poucos minutos após a inicialização do Defender para Nuvem você poderá ver:
- Recomendações de maneiras para melhorar a segurança dos recursos conectados.
- Um inventário dos seus recursos que o Defender para Nuvem avalia juntamente com a postura de segurança de cada um.

## Documentação adicional

[Documentação Oficial do Microsoft Azure](https://docs.microsoft.com/azure).

[Documentação do Microsoft Entra ID](https://learn.microsoft.com/pt-br/entra/identity/?WT.mc_id=APC-AzureActiveDirectory).

[Documentação do Microsoft Defender para nuvem](https://learn.microsoft.com/pt-br/azure/defender-for-cloud/?wt.mc_id=defenderforcloud_inproduct_portal_external).