RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 13/08/2025
Empresa: Abstergo Industries
Responsável: Caique Almeida
Introdução

Este relatório apresenta o plano estratégico para a implementação de serviços de nuvem na empresa Abstergo Industries, combinando as necessidades da operação farmacêutica e da redistribuidora. O objetivo é elencar e detalhar um plano cronológico para a implementação de 3 serviços essenciais da AWS (Amazon Web Services), com o objetivo principal de gerar redução de custos e aumento de performance de forma rápida e estratégica.
Descrição do Projeto

O projeto foi dividido em 3 etapas cronológicas, projetadas para construir uma base sólida na nuvem, garantindo ganhos progressivos e minimizando riscos.

Etapa 1: Backup e Arquivamento de Longo Prazo

    Ferramenta: Amazon S3 (Simple Storage Service)  / S3 Glacier

    Foco: Redução Imediata de Custos com Backup e Arquivamento de Dados.

    Descrição de Caso de Uso:

        Atualmente, os backups de servidores e o arquivamento de documentos fiscais e registros de lotes (exigidos pela ANVISA) são mantidos em mídias físicas (fitas ou discos) ou em storages locais de alto custo.

        Implementação: Substituiremos essa estrutura pela automação dos backups diretamente para o Amazon S3. Dados que precisam ser guardados por muitos anos, com acesso raro, serão movidos automaticamente para o S3 Glacier Deep Archive, uma camada de armazenamento de custo extremamente baixo.

    Resultado Esperado (Métricas):

        Redução de >70% nos custos de armazenamento de longo prazo.

        Redução de 100% no tempo gasto com operações manuais de troca de fitas.

        Aumento da durabilidade dos dados para 99.999999999%, garantindo conformidade e segurança.

Etapa 2: Migração de Servidores Críticos

    Ferramenta: Amazon EC2 (Elastic Compute Cloud)

    Foco: Aumento de Performance e Redução de Custos de Infraestrutura.

    Descrição de Caso de Uso:

        O servidor que hospeda o sistema de gestão ERP (TOTVS/SAP outros serviços) ou o banco de dados principal da operação está em um hardware físico local, que sofre com picos de lentidão no fechamento do mês e possui um alto custo de manutenção e energia.

        Implementação: O servidor será migrado para uma instância Amazon EC2. A capacidade do servidor poderá ser aumentada sob demanda durante os picos de processamento e reduzida nos períodos normais, pagando apenas pelo que for utilizado (modelo "pay-as-you-go").

    Resultado Esperado (Métricas):

        Redução de 50% no tempo de processamento de relatórios de fechamento mensal.

        Aumento da disponibilidade do sistema (uptime) para 99,9%.

        Eliminação dos gastos com compra e depreciação de servidores (CAPEX).

Etapa 3: Inteligência de Negócio e Otimização da Operação

    Ferramenta: Amazon QuickSight

    Foco: Otimização de Operações e Tomada de Decisão com Business Intelligence (BI).

    Descrição de Caso de Uso:

        As decisões sobre gestão de estoque e otimização de rotas de entrega são baseadas em planilhas e relatórios manuais, o que leva a ineficiências e custos ocultos (excesso de estoque, perdas por vencimento, rotas não otimizadas).

        Implementação: O Amazon QuickSight será conectado às fontes de dados (como o banco de dados do ERP, agora no EC2). Serão criados painéis (dashboards) interativos para visualizar em tempo real a performance de vendas por região, os níveis de estoque de cada produto e a eficiência das entregas.

    Resultado Esperado (Métricas):

        Redução de 15% no excesso de estoque através de previsões de demanda mais precisas.

        Diminuição de 20% nas rupturas de estoque (falta de produto).

        Tomada de decisão ágil e baseada em dados, com relatórios gerados em minutos, não em horas.

Conclusão

A implementação sequencial destes três serviços na Abstergo Industries tem como resultado esperado uma redução significativa nos custos operacionais de TI, um ganho de agilidade e performance nos sistemas críticos e, por fim, a habilidade de transformar dados brutos em inteligência para otimizar a operação logística e comercial. Recomenda-se a aprovação deste plano e a continuidade da jornada na nuvem, buscando sempre novas tecnologias que possam melhorar ainda mais os processos da empresa.
Anexos

    PlanilhadeComparativodeCustos:On−Premisevs.AWS
    CronogramaDetalhadodoProjeto
    ManualdePolıˊticadeBackupnoS3

Links de Referência e Tutoriais (AWS)
Geral e Estratégia de Nuvem

    Calculadora de Preços AWS: Para estimar custos e comparar cenários.

        https://calculator.aws/

    AWS Well-Architected Framework (Pilar de Otimização de Custos): Melhores práticas para construir de forma segura, eficiente e econômica na nuvem.

        https://aws.amazon.com/pt/architecture/well-architected/?wa-lens-cost-optimization.sort-by=item.additionalFields.sortDate&wa-lens-cost-optimization.sort-order=desc

    Soluções AWS para Saúde e Ciências da Vida (Farmacêutica):

        https://aws.amazon.com/pt/health/

Etapa 1: Amazon S3 e Glacier

    Primeiros Passos com o Amazon S3: Tutorial oficial da AWS.

        https://aws.amazon.com/pt/s3/getting-started/

    Gerenciando o ciclo de vida do armazenamento (Mover para Glacier):

        https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/object-lifecycle-mgmt.html

    Workshop de Backup e Restauração:

        https://catalog.workshops.aws/backup-and-restore

Etapa 2: Amazon EC2

    Tutorial: Conceitos básicos das instâncias do Amazon EC2 para Linux:

        https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/EC2_GetStarted.html

    Migração de Servidores para a AWS (AWS Migration Hub):

        https://aws.amazon.com/pt/migration-hub/

    Executando SAP na AWS (Relevante para ERPs):

        https://aws.amazon.com/pt/sap/

Etapa 3: Amazon QuickSight

    Comece a usar o Amazon QuickSight: Página oficial com visão geral.

        https://aws.amazon.com/pt/quicksight/getting-started/

    Workshop: Crie seu primeiro Dashboard com QuickSight (em inglês):

        https://catalog.workshops.aws/quicksight/en-US

    Galeria de Demonstração do QuickSight: Exemplos de dashboards para inspiração.

        https://democentral.learnquicksight.online/

Assinatura do Responsável pelo Projeto:
caiqueBTC

