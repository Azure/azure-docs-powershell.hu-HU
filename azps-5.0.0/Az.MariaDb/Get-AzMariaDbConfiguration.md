---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConfiguration.md
ms.openlocfilehash: d3e530cd9526f6f8797e770c45ecb223acbad62d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194621"
---
# <span data-ttu-id="3ec1d-101">Get-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ec1d-101">Get-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="3ec1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ec1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec1d-103">Információt kap a kiszolgáló konfigurációjáról.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="3ec1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ec1d-104">SYNTAX</span></span>

### <span data-ttu-id="3ec1d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ec1d-105">List (Default)</span></span>
```
Get-AzMariaDbConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3ec1d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ec1d-106">Get</span></span>
```
Get-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3ec1d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3ec1d-107">GetViaIdentity</span></span>
```
Get-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3ec1d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ec1d-108">DESCRIPTION</span></span>
<span data-ttu-id="3ec1d-109">Információt kap a kiszolgáló konfigurációjáról.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="3ec1d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ec1d-110">EXAMPLES</span></span>

### <span data-ttu-id="3ec1d-111">Példa 1: a MariaDB alatti összes konfiguráció listázása</span><span class="sxs-lookup"><span data-stu-id="3ec1d-111">Example 1: List all configuration under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConfiguration -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMariaDB/servers/configurations
audit_log_events                         Microsoft.DBforMariaDB/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMariaDB/servers/configurations
audit_log_include_users                  Microsoft.DBforMariaDB/servers/configurations
binlog_row_image                         Microsoft.DBforMariaDB/servers/configurations
character_set_server                     Microsoft.DBforMariaDB/servers/configurations
collation_server                         Microsoft.DBforMariaDB/servers/configurations
default_regex_flags                      Microsoft.DBforMariaDB/servers/configurations
default_week_format                      Microsoft.DBforMariaDB/servers/configurations
delayed_insert_limit                     Microsoft.DBforMariaDB/servers/configurations
delayed_insert_timeout                   Microsoft.DBforMariaDB/servers/configurations
delayed_queue_size                       Microsoft.DBforMariaDB/servers/configurations
div_precision_increment                  Microsoft.DBforMariaDB/servers/configurations
event_scheduler                          Microsoft.DBforMariaDB/servers/configurations
expensive_subquery_limit                 Microsoft.DBforMariaDB/servers/configurations
explicit_defaults_for_timestamp          Microsoft.DBforMariaDB/servers/configurations
group_concat_max_len                     Microsoft.DBforMariaDB/servers/configurations
histogram_size                           Microsoft.DBforMariaDB/servers/configurations
histogram_type                           Microsoft.DBforMariaDB/servers/configurations
host_cache_size                          Microsoft.DBforMariaDB/servers/configurations
init_connect                             Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_flushing                 Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_flushing_lwm             Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_hash_index               Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_hash_index_partitions    Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_hash_index_parts         Microsoft.DBforMariaDB/servers/configurations
innodb_adaptive_max_sleep_delay          Microsoft.DBforMariaDB/servers/configurations
innodb_autoextend_increment              Microsoft.DBforMariaDB/servers/configurations
innodb_autoinc_lock_mode                 Microsoft.DBforMariaDB/servers/configurations
innodb_buffer_pool_dump_pct              Microsoft.DBforMariaDB/servers/configurations
innodb_buffer_pool_size                  Microsoft.DBforMariaDB/servers/configurations
innodb_change_buffer_max_size            Microsoft.DBforMariaDB/servers/configurations
innodb_change_buffering                  Microsoft.DBforMariaDB/servers/configurations
innodb_cmp_per_index_enabled             Microsoft.DBforMariaDB/servers/configurations
innodb_compression_failure_threshold_pct Microsoft.DBforMariaDB/servers/configurations
innodb_compression_level                 Microsoft.DBforMariaDB/servers/configurations
innodb_compression_pad_pct_max           Microsoft.DBforMariaDB/servers/configurations
innodb_concurrency_tickets               Microsoft.DBforMariaDB/servers/configurations
innodb_deadlock_detect                   Microsoft.DBforMariaDB/servers/configurations
innodb_default_row_format                Microsoft.DBforMariaDB/servers/configurations
innodb_fill_factor                       Microsoft.DBforMariaDB/servers/configurations
innodb_flush_log_at_timeout              Microsoft.DBforMariaDB/servers/configurations
innodb_ft_enable_stopword                Microsoft.DBforMariaDB/servers/configurations
innodb_ft_num_word_optimize              Microsoft.DBforMariaDB/servers/configurations
innodb_ft_result_cache_limit             Microsoft.DBforMariaDB/servers/configurations
innodb_io_capacity                       Microsoft.DBforMariaDB/servers/configurations
innodb_lock_wait_timeout                 Microsoft.DBforMariaDB/servers/configurations
innodb_log_compressed_pages              Microsoft.DBforMariaDB/servers/configurations
innodb_lru_scan_depth                    Microsoft.DBforMariaDB/servers/configurations
innodb_max_dirty_pages_pct               Microsoft.DBforMariaDB/servers/configurations
innodb_max_dirty_pages_pct_lwm           Microsoft.DBforMariaDB/servers/configurations
innodb_max_purge_lag                     Microsoft.DBforMariaDB/servers/configurations
innodb_max_purge_lag_delay               Microsoft.DBforMariaDB/servers/configurations
innodb_max_undo_log_size                 Microsoft.DBforMariaDB/servers/configurations
innodb_old_blocks_pct                    Microsoft.DBforMariaDB/servers/configurations
innodb_old_blocks_time                   Microsoft.DBforMariaDB/servers/configurations
innodb_online_alter_log_max_size         Microsoft.DBforMariaDB/servers/configurations
innodb_open_files                        Microsoft.DBforMariaDB/servers/configurations
innodb_optimize_fulltext_only            Microsoft.DBforMariaDB/servers/configurations
innodb_page_cleaners                     Microsoft.DBforMariaDB/servers/configurations
innodb_purge_batch_size                  Microsoft.DBforMariaDB/servers/configurations
innodb_purge_rseg_truncate_frequency     Microsoft.DBforMariaDB/servers/configurations
innodb_random_read_ahead                 Microsoft.DBforMariaDB/servers/configurations
innodb_read_ahead_threshold              Microsoft.DBforMariaDB/servers/configurations
innodb_read_io_threads                   Microsoft.DBforMariaDB/servers/configurations
innodb_stats_auto_recalc                 Microsoft.DBforMariaDB/servers/configurations
innodb_stats_include_delete_marked       Microsoft.DBforMariaDB/servers/configurations
innodb_stats_method                      Microsoft.DBforMariaDB/servers/configurations
innodb_stats_modified_counter            Microsoft.DBforMariaDB/servers/configurations
innodb_stats_on_metadata                 Microsoft.DBforMariaDB/servers/configurations
innodb_stats_persistent                  Microsoft.DBforMariaDB/servers/configurations
innodb_stats_persistent_sample_pages     Microsoft.DBforMariaDB/servers/configurations
innodb_stats_traditional                 Microsoft.DBforMariaDB/servers/configurations
innodb_stats_transient_sample_pages      Microsoft.DBforMariaDB/servers/configurations
innodb_status_output                     Microsoft.DBforMariaDB/servers/configurations
innodb_status_output_locks               Microsoft.DBforMariaDB/servers/configurations
innodb_strict_mode                       Microsoft.DBforMariaDB/servers/configurations
innodb_sync_array_size                   Microsoft.DBforMariaDB/servers/configurations
innodb_table_locks                       Microsoft.DBforMariaDB/servers/configurations
innodb_thread_concurrency                Microsoft.DBforMariaDB/servers/configurations
innodb_thread_sleep_delay                Microsoft.DBforMariaDB/servers/configurations
innodb_undo_log_truncate                 Microsoft.DBforMariaDB/servers/configurations
innodb_write_io_threads                  Microsoft.DBforMariaDB/servers/configurations
interactive_timeout                      Microsoft.DBforMariaDB/servers/configurations
join_buffer_size                         Microsoft.DBforMariaDB/servers/configurations
join_cache_level                         Microsoft.DBforMariaDB/servers/configurations
lock_wait_timeout                        Microsoft.DBforMariaDB/servers/configurations
log_bin_trust_function_creators          Microsoft.DBforMariaDB/servers/configurations
log_output                               Microsoft.DBforMariaDB/servers/configurations
log_queries_not_using_indexes            Microsoft.DBforMariaDB/servers/configurations
log_slow_admin_statements                Microsoft.DBforMariaDB/servers/configurations
log_slow_filter                          Microsoft.DBforMariaDB/servers/configurations
log_slow_rate_limit                      Microsoft.DBforMariaDB/servers/configurations
log_slow_verbosity                       Microsoft.DBforMariaDB/servers/configurations
long_query_time                          Microsoft.DBforMariaDB/servers/configurations
low_priority_updates                     Microsoft.DBforMariaDB/servers/configurations
lower_case_table_names                   Microsoft.DBforMariaDB/servers/configurations
max_allowed_packet                       Microsoft.DBforMariaDB/servers/configurations
max_connect_errors                       Microsoft.DBforMariaDB/servers/configurations
max_connections                          Microsoft.DBforMariaDB/servers/configurations
max_delayed_threads                      Microsoft.DBforMariaDB/servers/configurations
max_digest_length                        Microsoft.DBforMariaDB/servers/configurations
max_error_count                          Microsoft.DBforMariaDB/servers/configurations
max_heap_table_size                      Microsoft.DBforMariaDB/servers/configurations
max_join_size                            Microsoft.DBforMariaDB/servers/configurations
max_length_for_sort_data                 Microsoft.DBforMariaDB/servers/configurations
max_prepared_stmt_count                  Microsoft.DBforMariaDB/servers/configurations
max_recursive_iterations                 Microsoft.DBforMariaDB/servers/configurations
max_seeks_for_key                        Microsoft.DBforMariaDB/servers/configurations
max_session_mem_used                     Microsoft.DBforMariaDB/servers/configurations
max_sort_length                          Microsoft.DBforMariaDB/servers/configurations
max_sp_recursion_depth                   Microsoft.DBforMariaDB/servers/configurations
max_user_connections                     Microsoft.DBforMariaDB/servers/configurations
max_write_lock_count                     Microsoft.DBforMariaDB/servers/configurations
min_examined_row_limit                   Microsoft.DBforMariaDB/servers/configurations
net_read_timeout                         Microsoft.DBforMariaDB/servers/configurations
net_retry_count                          Microsoft.DBforMariaDB/servers/configurations
net_write_timeout                        Microsoft.DBforMariaDB/servers/configurations
optimizer_search_depth                   Microsoft.DBforMariaDB/servers/configurations
optimizer_selectivity_sampling_limit     Microsoft.DBforMariaDB/servers/configurations
optimizer_use_condition_selectivity      Microsoft.DBforMariaDB/servers/configurations
preload_buffer_size                      Microsoft.DBforMariaDB/servers/configurations
query_store_capture_interval             Microsoft.DBforMariaDB/servers/configurations
query_store_capture_mode                 Microsoft.DBforMariaDB/servers/configurations
query_store_capture_utility_queries      Microsoft.DBforMariaDB/servers/configurations
query_store_retention_period_in_days     Microsoft.DBforMariaDB/servers/configurations
query_store_wait_sampling_capture_mode   Microsoft.DBforMariaDB/servers/configurations
query_store_wait_sampling_frequency      Microsoft.DBforMariaDB/servers/configurations
read_only                                Microsoft.DBforMariaDB/servers/configurations
server_id                                Microsoft.DBforMariaDB/servers/configurations
session_track_schema                     Microsoft.DBforMariaDB/servers/configurations
session_track_state_change               Microsoft.DBforMariaDB/servers/configurations
session_track_transaction_info           Microsoft.DBforMariaDB/servers/configurations
skip_show_database                       Microsoft.DBforMariaDB/servers/configurations
slave_parallel_threads                   Microsoft.DBforMariaDB/servers/configurations
slow_query_log                           Microsoft.DBforMariaDB/servers/configurations
sort_buffer_size                         Microsoft.DBforMariaDB/servers/configurations
sql_mode                                 Microsoft.DBforMariaDB/servers/configurations
standard_compliant_cte                   Microsoft.DBforMariaDB/servers/configurations
stored_program_cache                     Microsoft.DBforMariaDB/servers/configurations
sync_master_info                         Microsoft.DBforMariaDB/servers/configurations
sync_relay_log_info                      Microsoft.DBforMariaDB/servers/configurations
table_definition_cache                   Microsoft.DBforMariaDB/servers/configurations
table_open_cache                         Microsoft.DBforMariaDB/servers/configurations
thread_pool_max_threads                  Microsoft.DBforMariaDB/servers/configurations
thread_pool_min_threads                  Microsoft.DBforMariaDB/servers/configurations
thread_pool_prio_kickup_timer            Microsoft.DBforMariaDB/servers/configurations
thread_pool_priority                     Microsoft.DBforMariaDB/servers/configurations
thread_pool_stall_limit                  Microsoft.DBforMariaDB/servers/configurations
time_zone                                Microsoft.DBforMariaDB/servers/configurations
tx_isolation                             Microsoft.DBforMariaDB/servers/configurations
updatable_views_with_limit               Microsoft.DBforMariaDB/servers/configurations
use_stat_tables                          Microsoft.DBforMariaDB/servers/configurations
userstat                                 Microsoft.DBforMariaDB/servers/configurations
wait_timeout                             Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="3ec1d-112">Ez a parancs felsorolja az összes konfigurációt a MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-112">This command lists all configuration under a MariaDB.</span></span>

### <span data-ttu-id="3ec1d-113">2. példa: a MariaDB konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ec1d-113">Example 2: Get a configuration of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConfiguration -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Name max_connections

Name            Type
----            ----
max_connections Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="3ec1d-114">Ez a parancs a MariaDB konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-114">This command gets a configuration of MariaDB.</span></span>

## <span data-ttu-id="3ec1d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-115">PARAMETERS</span></span>

### <span data-ttu-id="3ec1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec1d-116">-DefaultProfile</span></span>
<span data-ttu-id="3ec1d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec1d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ec1d-118">-InputObject</span></span>
<span data-ttu-id="3ec1d-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec1d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ec1d-120">-Name</span></span>
<span data-ttu-id="3ec1d-121">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ec1d-123">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3ec1d-124">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec1d-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3ec1d-125">-ServerName</span></span>
<span data-ttu-id="3ec1d-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec1d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ec1d-127">-SubscriptionId</span></span>
<span data-ttu-id="3ec1d-128">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-128">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec1d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec1d-129">CommonParameters</span></span>
<span data-ttu-id="3ec1d-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ec1d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec1d-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec1d-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-132">INPUTS</span></span>

### <span data-ttu-id="3ec1d-133">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="3ec1d-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="3ec1d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-134">OUTPUTS</span></span>

### <span data-ttu-id="3ec1d-135">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ec1d-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="3ec1d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ec1d-136">NOTES</span></span>

<span data-ttu-id="3ec1d-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-137">ALIASES</span></span>

<span data-ttu-id="3ec1d-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3ec1d-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ec1d-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ec1d-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ec1d-141">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3ec1d-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ec1d-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3ec1d-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3ec1d-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3ec1d-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3ec1d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ec1d-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3ec1d-147">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3ec1d-148">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3ec1d-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3ec1d-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3ec1d-151">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="3ec1d-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3ec1d-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3ec1d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ec1d-153">RELATED LINKS</span></span>
