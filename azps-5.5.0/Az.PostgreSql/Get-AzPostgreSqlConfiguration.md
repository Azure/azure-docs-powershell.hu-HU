---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153867"
---
# <span data-ttu-id="0d686-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d686-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="0d686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d686-102">SYNOPSIS</span></span>
<span data-ttu-id="0d686-103">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="0d686-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="0d686-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0d686-104">SYNTAX</span></span>

### <span data-ttu-id="0d686-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d686-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d686-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="0d686-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d686-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d686-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d686-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0d686-108">DESCRIPTION</span></span>
<span data-ttu-id="0d686-109">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="0d686-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="0d686-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0d686-110">EXAMPLES</span></span>

### <span data-ttu-id="0d686-111">1. példa: A PostgreSql-kiszolgáló összes konfigurációjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="0d686-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="0d686-112">Ez a parancsmag felsorolja a megadott PostgreSql-kiszolgáló összes konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0d686-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="0d686-113">2. példa: A PostgreSql-konfiguráció név szerint való beállítása</span><span class="sxs-lookup"><span data-stu-id="0d686-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="0d686-114">Ez a parancsmag név szerint kapja meg a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0d686-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="0d686-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d686-115">PARAMETERS</span></span>

### <span data-ttu-id="0d686-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d686-116">-DefaultProfile</span></span>
<span data-ttu-id="0d686-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d686-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d686-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d686-118">-InputObject</span></span>
<span data-ttu-id="0d686-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0d686-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d686-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0d686-120">-Name</span></span>
<span data-ttu-id="0d686-121">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="0d686-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d686-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d686-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-123">The name of the resource group.</span></span>
<span data-ttu-id="0d686-124">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0d686-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0d686-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0d686-125">-ServerName</span></span>
<span data-ttu-id="0d686-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-126">The name of the server.</span></span>

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

### <span data-ttu-id="0d686-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d686-127">-SubscriptionId</span></span>
<span data-ttu-id="0d686-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0d686-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0d686-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d686-129">CommonParameters</span></span>
<span data-ttu-id="0d686-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d686-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d686-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d686-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d686-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d686-132">INPUTS</span></span>

### <span data-ttu-id="0d686-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0d686-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0d686-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d686-134">OUTPUTS</span></span>

### <span data-ttu-id="0d686-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d686-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="0d686-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0d686-136">NOTES</span></span>

<span data-ttu-id="0d686-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0d686-137">ALIASES</span></span>

<span data-ttu-id="0d686-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0d686-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d686-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0d686-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d686-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d686-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d686-141">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0d686-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d686-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0d686-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0d686-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0d686-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0d686-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d686-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0d686-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0d686-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0d686-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="0d686-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0d686-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0d686-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0d686-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0d686-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0d686-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0d686-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d686-153">RELATED LINKS</span></span>

