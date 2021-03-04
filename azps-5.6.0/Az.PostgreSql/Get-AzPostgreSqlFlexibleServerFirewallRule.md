---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: c6197ff97191c50f7f85acbee0a8ce51b54d8211
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920458"
---
# <span data-ttu-id="354ec-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="354ec-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="354ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="354ec-102">SYNOPSIS</span></span>
<span data-ttu-id="354ec-103">List all the firewall rules in a given server.</span><span class="sxs-lookup"><span data-stu-id="354ec-103">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="354ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="354ec-104">SYNTAX</span></span>

### <span data-ttu-id="354ec-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="354ec-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="354ec-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="354ec-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="354ec-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="354ec-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="354ec-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="354ec-108">DESCRIPTION</span></span>
<span data-ttu-id="354ec-109">List all the firewall rules in a given server.</span><span class="sxs-lookup"><span data-stu-id="354ec-109">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="354ec-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="354ec-110">EXAMPLES</span></span>

### <span data-ttu-id="354ec-111">1. példa: Tűzfalszabályok lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="354ec-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="354ec-112">Ez a parancsmag név szerint kapja meg a tűzfalszabályokat.</span><span class="sxs-lookup"><span data-stu-id="354ec-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="354ec-113">2. példa: Tűzfalszabályok beállítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="354ec-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/servers/postgresql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="354ec-114">Ez a parancsmag identitás szerint kapja meg a tűzfalszabályokat.</span><span class="sxs-lookup"><span data-stu-id="354ec-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="354ec-115">3. példa: A megadott PostgreSql-kiszolgáló tűzfalszabályának felsorolása</span><span class="sxs-lookup"><span data-stu-id="354ec-115">Example 3: Lists all the firewall rules in the specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="354ec-116">Ez a parancsmag felsorolja a megadott PostgreSql-kiszolgáló összes tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="354ec-116">This cmdlet lists all the firewall rule in specified PostgreSql server.</span></span>

## <span data-ttu-id="354ec-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="354ec-117">PARAMETERS</span></span>

### <span data-ttu-id="354ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354ec-118">-DefaultProfile</span></span>
<span data-ttu-id="354ec-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="354ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="354ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="354ec-120">-InputObject</span></span>
<span data-ttu-id="354ec-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="354ec-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="354ec-122">-Name</span><span class="sxs-lookup"><span data-stu-id="354ec-122">-Name</span></span>
<span data-ttu-id="354ec-123">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="354ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="354ec-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-125">The name of the resource group.</span></span>
<span data-ttu-id="354ec-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="354ec-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="354ec-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="354ec-127">-ServerName</span></span>
<span data-ttu-id="354ec-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-128">The name of the server.</span></span>

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

### <span data-ttu-id="354ec-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="354ec-129">-SubscriptionId</span></span>
<span data-ttu-id="354ec-130">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="354ec-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="354ec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354ec-131">CommonParameters</span></span>
<span data-ttu-id="354ec-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354ec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354ec-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="354ec-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354ec-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="354ec-134">INPUTS</span></span>

### <span data-ttu-id="354ec-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="354ec-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="354ec-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="354ec-136">OUTPUTS</span></span>

### <span data-ttu-id="354ec-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="354ec-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="354ec-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="354ec-138">NOTES</span></span>

<span data-ttu-id="354ec-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="354ec-139">ALIASES</span></span>

<span data-ttu-id="354ec-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="354ec-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="354ec-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="354ec-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="354ec-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="354ec-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="354ec-143">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="354ec-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="354ec-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="354ec-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="354ec-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="354ec-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="354ec-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="354ec-148">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="354ec-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="354ec-150">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="354ec-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="354ec-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="354ec-152">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="354ec-153">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="354ec-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="354ec-154">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="354ec-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="354ec-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="354ec-155">RELATED LINKS</span></span>

