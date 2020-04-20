# Monitoring Azure SQL Managed Instance with Azure SQL Analytics

![hackathon design](/images/training.jpg)

- [Monitoring Azure SQL Managed Instance with Azure SQL Analytics](#monitoring-azure-sql-managed-instance-with-azure-sql-analytics)
  - [1. Setting-up for Azure SQL Analytics](#1-setting-up-for-azure-sql-analytics)
    - [1.1 Create Azure Log Analytics Workspace](#11-create-azure-log-analytics-workspace)
  - [1.2 Configure the streaming export of diagnostic telemetry](#12-configure-the-streaming-export-of-diagnostic-telemetry)
  - [1.3 Install Azure SQL Analytics Solution](#13-install-azure-sql-analytics-solution)
    - [2. Review SQL MI metrics and insights using ‘out-of-the-box- Azure SQL Analytics](#2-review-sql-mi-metrics-and-insights-using-out-of-the-box--azure-sql-analytics)
  - [3. Review Kusto query language for Azure Log Analytics](#3-review-kusto-query-language-for-azure-log-analytics)
  - [4. Create  Azure Monitor Alerts based on CPU and/or Storage utilization from Log Analytics Queries](#4-create-azure-monitor-alerts-based-on-cpu-andor-storage-utilization-from-log-analytics-queries)

## 1. Setting-up for Azure SQL Analytics

### 1.1 Create Azure Log Analytics Workspace

In the Azure portal, click **All services**. In the list of resources, type Log Analytics. As you begin typing, the list filters based on your input. Select Log Analytics workspaces.

![create log analytics](/images/azure-portal-01.png)

- Click Add, and then select choices for the following items:
Provide a name for the new Log Analytics workspace, such as DefaultLAWorkspace. This name must be globally unique across all Azure Monitor subscriptions.
- Select a Subscription to link to by selecting from the drop-down list if the default selected is not appropriate.
- For Resource Group, choose to use an existing resource group already setup or create a new one.
- Select an available **Location**. For more information, see which regions [Log Analytics is available in](https://azure.microsoft.com/regions/services/) and search for Azure Monitor from the Search for a product field.
- If you are creating a workspace in a new subscription created after April 2, 2018, it will automatically use the Per GB pricing plan and the option to select a pricing tier will not be available. If you are creating a workspace for an existing subscription created before April 2, or to subscription that was tied to an existing Enterprise Agreement (EA) enrollment, select your preferred pricing tier. For more information about the particular tiers, see [Log Analytics Pricing Details](https://azure.microsoft.com/pricing/details/log-analytics/).

![create log analytics workspace](/images/create-loganalytics-workspace-02.png)

After providing the required information on the Log Analytics Workspace pane, click OK.

*Please see [quick create document](https://docs.microsoft.com/en-us/azure/azure-monitor/learn/quick-create-workspace) for additional details*

## 1.2 Configure the streaming export of diagnostic telemetry

You can use the Diagnostics settings menu in the Azure portal to enable and configure streaming of diagnostic telemetry.

Set-up for Managed Instance resource and each instance database - [Managed Instance diagnostic telemetry](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-metrics-diag-logging?tabs=azure-portal#managed-instance)

## 1.3 Install Azure SQL Analytics Solution

Go to the Azure portal. Search for and select Solutions.

![create log analytics](/images/search_solutions.PNG)

Click **Add**

![create log analytics](/images/solutions_add.PNG)

Search for the Azure SQL Analytics solution.

![create log analytics](/images/sql_analytics_solution.PNG)

During creation select the Log Analytics workspace your created in 1.1. Once creation is complete, click on your 
Azure SQL Analytics Solution.

![create log analytics](/images/sql_analytics_solution_02.PNG
)

CLick **View Summary** then drill into your Managed Instance

![summary](/images/azure_sql_analytics_summary.PNG)

![panel](/images/summary_panel.PNG)

![mi view](/images/managed_instance_view.PNG)


### 2. Review SQL MI metrics and insights using ‘out-of-the-box- Azure SQL Analytics

## 3. Review Kusto query language for Azure Log Analytics

## 4. Create  Azure Monitor Alerts based on CPU and/or Storage utilization from Log Analytics Queries
