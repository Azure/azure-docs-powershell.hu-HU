---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: fae355df0b33fa648be1d9043f140123cf9d79a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161283"
---
# <span data-ttu-id="bf305-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf305-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="bf305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf305-102">SYNOPSIS</span></span>
<span data-ttu-id="bf305-103">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="bf305-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="bf305-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bf305-104">SYNTAX</span></span>

### <span data-ttu-id="bf305-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf305-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf305-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="bf305-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf305-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bf305-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bf305-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bf305-108">DESCRIPTION</span></span>
<span data-ttu-id="bf305-109">Információkat kap a kiszolgáló konfigurációról.</span><span class="sxs-lookup"><span data-stu-id="bf305-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="bf305-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bf305-110">EXAMPLES</span></span>

### <span data-ttu-id="bf305-111">1. példa: A megadott MySql-kiszolgáló összes konfigurációjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="bf305-111">Example 1: List all configurations in specified MySql server</span></span>
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

<span data-ttu-id="bf305-112">Ez a parancsmag felsorolja a megadott MySql-kiszolgáló összes konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="bf305-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="bf305-113">2. példa: A MySql-konfiguráció név szerint való beállítása</span><span class="sxs-lookup"><span data-stu-id="bf305-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="bf305-114">Ez a parancsmag név szerint kapja meg a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="bf305-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="bf305-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf305-115">PARAMETERS</span></span>

### <span data-ttu-id="bf305-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf305-116">-DefaultProfile</span></span>
<span data-ttu-id="bf305-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf305-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf305-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf305-118">-InputObject</span></span>
<span data-ttu-id="bf305-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bf305-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bf305-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bf305-120">-Name</span></span>
<span data-ttu-id="bf305-121">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="bf305-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf305-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf305-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-123">The name of the resource group.</span></span>
<span data-ttu-id="bf305-124">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="bf305-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bf305-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bf305-125">-ServerName</span></span>
<span data-ttu-id="bf305-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-126">The name of the server.</span></span>

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

### <span data-ttu-id="bf305-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf305-127">-SubscriptionId</span></span>
<span data-ttu-id="bf305-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bf305-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bf305-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf305-129">CommonParameters</span></span>
<span data-ttu-id="bf305-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf305-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf305-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf305-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf305-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf305-132">INPUTS</span></span>

### <span data-ttu-id="bf305-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bf305-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bf305-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf305-134">OUTPUTS</span></span>

### <span data-ttu-id="bf305-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf305-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="bf305-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bf305-136">NOTES</span></span>

<span data-ttu-id="bf305-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bf305-137">ALIASES</span></span>

<span data-ttu-id="bf305-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="bf305-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf305-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="bf305-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf305-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf305-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf305-141">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="bf305-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf305-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bf305-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bf305-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bf305-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="bf305-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf305-146">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bf305-147">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bf305-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bf305-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="bf305-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="bf305-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bf305-151">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bf305-152">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bf305-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bf305-153">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="bf305-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bf305-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf305-154">RELATED LINKS</span></span>

