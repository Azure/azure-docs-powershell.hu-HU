---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: fae355df0b33fa648be1d9043f140123cf9d79a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359014"
---
# <span data-ttu-id="217f6-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="217f6-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="217f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="217f6-102">SYNOPSIS</span></span>
<span data-ttu-id="217f6-103">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="217f6-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="217f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="217f6-104">SYNTAX</span></span>

### <span data-ttu-id="217f6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="217f6-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="217f6-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="217f6-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="217f6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="217f6-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="217f6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="217f6-108">DESCRIPTION</span></span>
<span data-ttu-id="217f6-109">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="217f6-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="217f6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="217f6-110">EXAMPLES</span></span>

### <span data-ttu-id="217f6-111">1. példa: A megadott MySql-kiszolgáló összes konfigurációjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="217f6-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="217f6-112">Ez a parancsmag felsorolja a megadott MySql-kiszolgáló összes konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="217f6-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="217f6-113">2. példa: A MySql-konfiguráció név szerint való beállítása</span><span class="sxs-lookup"><span data-stu-id="217f6-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="217f6-114">Ez a parancsmag név szerint kapja meg a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="217f6-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="217f6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="217f6-115">PARAMETERS</span></span>

### <span data-ttu-id="217f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217f6-116">-DefaultProfile</span></span>
<span data-ttu-id="217f6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="217f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="217f6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="217f6-118">-InputObject</span></span>
<span data-ttu-id="217f6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="217f6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="217f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="217f6-120">-Name</span></span>
<span data-ttu-id="217f6-121">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="217f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="217f6-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-123">The name of the resource group.</span></span>
<span data-ttu-id="217f6-124">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="217f6-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="217f6-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="217f6-125">-ServerName</span></span>
<span data-ttu-id="217f6-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-126">The name of the server.</span></span>

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

### <span data-ttu-id="217f6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="217f6-127">-SubscriptionId</span></span>
<span data-ttu-id="217f6-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="217f6-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="217f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217f6-129">CommonParameters</span></span>
<span data-ttu-id="217f6-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="217f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217f6-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="217f6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217f6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="217f6-132">INPUTS</span></span>

### <span data-ttu-id="217f6-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="217f6-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="217f6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="217f6-134">OUTPUTS</span></span>

### <span data-ttu-id="217f6-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="217f6-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="217f6-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="217f6-136">NOTES</span></span>

<span data-ttu-id="217f6-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="217f6-137">ALIASES</span></span>

<span data-ttu-id="217f6-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="217f6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="217f6-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="217f6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="217f6-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="217f6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="217f6-141">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="217f6-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="217f6-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="217f6-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="217f6-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="217f6-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="217f6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="217f6-146">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="217f6-147">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="217f6-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="217f6-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="217f6-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="217f6-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="217f6-151">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="217f6-152">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="217f6-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="217f6-153">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="217f6-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="217f6-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="217f6-154">RELATED LINKS</span></span>

