# Governança e Conformidade no Microsoft Azure

Este guia contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

## Índice
- [Introdução](#introdução)
- [Microsoft Purview](#microsoft-purview)
- [Azure Policy](#azure-policy)
- [Bloqueios de Recursos](#bloqueios-de-recursos)
- [Portal de Confiança do Serviço](#portal-de-confiança-do-serviço)
- [Documentação Adicional](#documentação-adicional)

## Introdução

Este desafio consiste em explorar o portal do Microsoft Azure, analisando algumas opções de gerenciamento de políticas de Governança e Conformidade no Microsoft Azure.

## Microsoft Purview

O Microsoft Purview é uma família de soluções de governança, risco e conformidade de dados que ajuda você a obter uma única exibição unificada em seus dados. O Microsoft Purview coleta informações sobre seus dados locais, multinuvem e software como serviço.

Com o Microsoft Purview, você pode se manter atualizado sobre seu cenário de dados graças a:
- Descoberta de dados automatizada
- Classificação de dados confidenciais
- Linhagem de dados de ponta a ponta

Duas áreas de solução principais compreendem o Microsoft Purview: risco e conformidade e governança unificada de dados.

O Microsoft Purview tem soluções robustas e unificadas de governança de dados que ajudam a gerenciar seus dados locais, multinuvem e de software como serviço. Os recursos robustos de governança de dados do Microsoft Purview permitem gerenciar seus dados armazenados em bancos de dados do Azure, SQL e Hive, localmente e até mesmo em outras nuvens, como o Amazon S3.

## Azure Policy

O Azure Policy é um serviço do Azure que permite criar, atribuir e gerenciar políticas que controlam ou auditam os recursos. Essas políticas impõem regras diferentes sobre as configurações dos recursos, de modo que essas configurações permaneçam em conformidade com os padrões corporativos.

As Políticas do Azure podem ser definidas em cada nível, permitindo que você defina políticas em um recurso específico, um grupo de recursos, uma assinatura e assim por diante. Além disso, as Políticas do Azure são herdadas, portanto, se você definir uma política em um nível superior, ela será aplicada automaticamente a todos os agrupamentos que se enquadram no pai. Por exemplo, se você definir um Azure Policy em um grupo de recursos, todos os recursos criados nesse grupo de recursos receberão automaticamente a mesma política.

## Bloqueios de Recursos

Um bloqueio de recurso impede que os recursos sejam excluídos ou alterados acidentalmente.

Mesmo com as políticas do controle de acesso baseado em função do Azure (RBAC do Azure) em vigor, ainda há um risco de que as pessoas com o nível correto de acesso possam excluir recursos de nuvem críticos. Os bloqueios de recursos impedem que recursos sejam excluídos ou atualizados, dependendo do tipo de bloqueio.

Podem ser aplicados a recursos individuais, grupos de recursos ou até mesmo a toda uma assinatura. Os bloqueios de recursos são herdados, o que significa que, se você colocar um bloqueio de recurso em um grupo de recursos, todos os recursos do grupo de recursos também terão o bloqueio de recurso aplicado.

Há dois tipos de bloqueios de recursos, um que impede que os usuários excluam e outro que impede que os usuários alterem ou excluam um recurso.
- A exclusão significa que os usuários autorizados ainda poderão ler e modificar um recurso, mas não poderão excluir o recurso.
- ReadOnly significa que os usuários autorizados poderão ler um recurso, mas não poderão excluir ou atualizar o recurso. Aplicar esse bloqueio é semelhante ao restringir todos os usuários autorizados para as permissões concedidas pela função Leitor.

## Portal de Confiança do Serviço

O Portal de Confiança do Serviço da Microsoft é um local que oferece acesso a vários conteúdos, ferramentas e outros recursos sobre práticas de segurança, privacidade e conformidade da Microsoft.

Ele contém detalhes sobre a implementação de controles e processos da Microsoft que protegem nossos serviços na nuvem e os dados do cliente encontrados neles. Para acessar alguns dos recursos do Portal de Confiança do Serviço, é preciso entrar como usuário autenticado com sua conta de serviços em nuvem da Microsoft (conta da organização do Microsoft Entra ID). Você precisará examinar e aceitar o contrato de confidencialidade da Microsoft dos materiais de conformidade.

## Documentação adicional

[Documentação Oficial do Microsoft Azure](https://docs.microsoft.com/azure).

[Microsoft Purview](https://learn.microsoft.com/pt-br/purview/).

[Azure Policy](https://learn.microsoft.com/pt-br/azure/governance/policy/).

[Portal de Confiança do Serviço](https://servicetrust.microsoft.com/).