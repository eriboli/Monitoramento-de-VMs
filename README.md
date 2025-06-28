# Monitoramento-de-VMs

1. Escolha e Configuração do Agente Correto
	Utilize o Azure Monitor Agent (AMA), que é a solução recomendada atualmente.
	Evite o uso do Log Analytics Agent (MMA), pois está sendo descontinuado.
	Instale o agente diretamente na VM ou via extensão do Azure.
	Melhor prática: centralize a coleta de dados em um Log Analytics Workspace compartilhado.

3. Habilitação de Diagnóstico e Coleta de Logs
	Habilite a coleta de:
	Métricas de desempenho (CPU, memória, disco, rede).
	Logs de atividade (Azure Activity Log).
	Logs de sistema (eventos do Windows/Linux, syslog, etc.).
	Envie os dados para:
	Log Analytics Workspace.
	Armazenamento (para arquivamento).
	Event Hub (para integrações externas).
	Não se esqueça de configurar a coleta de logs a nível de recurso.

4. Utilização do Azure Monitor e VM Insights
	Habilite o VM Insights para visão centralizada e gráfica do desempenho.
	Acompanhe em tempo real:
	Consumo de CPU.
	Uso de memória.
	IOPS de disco.
	Tráfego de rede.
	Boa prática: configure painéis personalizados no Azure Monitor para equipes de operação.

5. Configuração de Alertas Inteligentes
	Crie alertas baseados em:
	Métricas (exemplo: CPU acima de 80%).
	Logs (consultas KQL, como falhas de login).
	Use grupos de ação para envio por e-mail, SMS, webhook ou automação.
	Recomenda-se criar alertas para eventos críticos e configurar runbooks automáticos como resposta.

6. Criação de Workbooks Personalizados
	Use os Workbooks para criar relatórios dinâmicos e visuais.
	Combine dados de diferentes fontes: métricas, logs, segurança.
	Ideal para dashboards executivos e operacionais.

7. Segurança e Governança no Monitoramento
	Use controle de acesso baseado em função (RBAC) para limitar quem pode ver ou configurar alertas e logs.
	Ative o Microsoft Defender for Servers para identificar vulnerabilidades e comportamentos suspeitos.
	Integrar com o Azure Security Center (Defender for Cloud) é prática recomendada.

8. Retenção e Custo
	Ajuste a retenção dos logs conforme as exigências de compliance e custo.
	Métricas são armazenadas gratuitamente por 93 dias.
	Logs têm retenção configurável (30 a 730 dias), podendo impactar no custo.
	Dica: utilize filtros na coleta de logs para evitar ingestão desnecessária de dados.

Checklist para Configuração Eficiente
	Azure Monitor Agent instalado
	Diagnóstico ativado e enviando a workspace	
	Métricas e logs coletados corretamente	
	Alertas e grupos de ação configurados	
	VM Insights habilitado	
	RBAC aplicado corretamente	
	Monitoramento integrado ao Defender	
	Workbooks e dashboards criados
