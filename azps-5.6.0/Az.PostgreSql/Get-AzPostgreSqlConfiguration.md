---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 97b16f3930eda94e69c3528432ee54927c3eef7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918161"
---
# <span data-ttu-id="6adb4-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6adb4-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="6adb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6adb4-102">SYNOPSIS</span></span>
<span data-ttu-id="6adb4-103">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="6adb4-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="6adb4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6adb4-104">SYNTAX</span></span>

### <span data-ttu-id="6adb4-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6adb4-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6adb4-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="6adb4-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6adb4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6adb4-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6adb4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6adb4-108">DESCRIPTION</span></span>
<span data-ttu-id="6adb4-109">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="6adb4-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="6adb4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6adb4-110">EXAMPLES</span></span>

### <span data-ttu-id="6adb4-111">1. példa: A PostgreSql-kiszolgáló összes konfigurációjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="6adb4-111">Example 1: List all configurations in PostgreSql server</span></span>
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

<span data-ttu-id="6adb4-112">Ez a parancsmag felsorolja a megadott PostgreSql-kiszolgáló összes konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6adb4-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="6adb4-113">2. példa: A PostgreSql-konfiguráció név szerint való beállítása</span><span class="sxs-lookup"><span data-stu-id="6adb4-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="6adb4-114">Ez a parancsmag név szerint kapja meg a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="6adb4-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="6adb4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6adb4-115">PARAMETERS</span></span>

### <span data-ttu-id="6adb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6adb4-116">-DefaultProfile</span></span>
<span data-ttu-id="6adb4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6adb4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6adb4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6adb4-118">-InputObject</span></span>
<span data-ttu-id="6adb4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6adb4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6adb4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6adb4-120">-Name</span></span>
<span data-ttu-id="6adb4-121">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="6adb4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6adb4-122">-ResourceGroupName</span></span>
<span data-ttu-id="6adb4-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-123">The name of the resource group.</span></span>
<span data-ttu-id="6adb4-124">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6adb4-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6adb4-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6adb4-125">-ServerName</span></span>
<span data-ttu-id="6adb4-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-126">The name of the server.</span></span>

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

### <span data-ttu-id="6adb4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6adb4-127">-SubscriptionId</span></span>
<span data-ttu-id="6adb4-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6adb4-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6adb4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6adb4-129">CommonParameters</span></span>
<span data-ttu-id="6adb4-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6adb4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6adb4-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6adb4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6adb4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6adb4-132">INPUTS</span></span>

### <span data-ttu-id="6adb4-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6adb4-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6adb4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6adb4-134">OUTPUTS</span></span>

### <span data-ttu-id="6adb4-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="6adb4-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="6adb4-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6adb4-136">NOTES</span></span>

<span data-ttu-id="6adb4-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6adb4-137">ALIASES</span></span>

<span data-ttu-id="6adb4-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6adb4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6adb4-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6adb4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6adb4-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6adb4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6adb4-141">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6adb4-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6adb4-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6adb4-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6adb4-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6adb4-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6adb4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6adb4-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6adb4-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6adb4-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6adb4-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="6adb4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6adb4-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6adb4-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6adb4-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6adb4-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6adb4-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6adb4-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6adb4-153">RELATED LINKS</span></span>

