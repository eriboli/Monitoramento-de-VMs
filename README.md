# Escolher e configurar o agente correto
1. Utilizar o Azure Monitor Agent (AMA), que é a solução recomendada atualmente.
2. Evitar o uso do Log Analytics Agent (MMA), pois está sendo descontinuado.
3. Instalar o agente diretamente na VM ou via extensão do Azure.

Melhor prática: centralizar a coleta de dados em um Log Analytics Workspace compartilhado.

# Habilitar e diagnóstico e coleta de Logs

Habilitar a coleta de:
- Métricas de desempenho (CPU, memória, disco, rede).
- Logs de atividade (Azure Activity Log).
- Logs de sistema (eventos do Windows/Linux, syslog, etc.).

Enviar os dados para:
- Log Analytics Workspace.
- Armazenamento (para arquivamento).
- Event Hub (para integrações externas).

Não esquecer de configurar a coleta de logs a nível de recurso.

# Utilizar o Azure Monitor e VM Insights

Habilitar o VM Insights para visão centralizada e gráfica do desempenho.

Acompanhar em tempo real:
- Consumo de CPU.
- Uso de memória.
- IOPS de disco.
- Tráfego de rede.

Dica de boa prática:
Configurar painéis personalizados no Azure Monitor para equipes de operação.

# Configurar Alertas Inteligentes

Crie alertas baseados em:
 - Métricas (exemplo: CPU acima de 80%).
 - Logs (consultas KQL, como falhas de login).
 - Usar grupos de ação para envio por e-mail, SMS, webhook ou automação.

Recomenda-se criar alertas para eventos críticos e configurar runbooks automáticos como resposta.

# Criar Workbooks personalizados

- Usar Workbooks para criar relatórios dinâmicos e visuais.
- Combinar dados de diferentes fontes: métricas, logs, segurança.

Ideal para dashboards executivos e operacionais.

# Segurança e governança no monitoramento

- Usar controle de acesso baseado em função (RBAC) para limitar quem pode ver ou configurar alertas e logs.
- Ativar o Microsoft Defender for Servers para identificar vulnerabilidades e comportamentos suspeitos.
- Integrar com o Azure Security Center (Defender for Cloud) é prática recomendada.

# Retenção e custo

- Ajustar a retenção dos logs conforme as exigências de compliance e custo.
- Métricas são armazenadas gratuitamente por 93 dias.
- Logs têm retenção configurável (30 a 730 dias), podendo impactar no custo.
- Dica: utilizar filtros na coleta de logs para evitar ingestão desnecessária de dados.

# Checklist para Configuração Eficiente
- Azure Monitor Agent instalado
- Diagnóstico ativado e enviando a workspace	
- Métricas e logs coletados corretamente	
- Alertas e grupos de ação configurados	
- VM Insights habilitado	
- RBAC aplicado corretamente	
- Monitoramento integrado ao Defender	
- Workbooks e dashboards criados
