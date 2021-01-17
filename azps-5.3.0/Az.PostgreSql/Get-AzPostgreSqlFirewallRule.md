---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378474"
---
# <span data-ttu-id="b3628-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3628-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="b3628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3628-102">SYNOPSIS</span></span>
<span data-ttu-id="b3628-103">Információkat kap a kiszolgáló tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="b3628-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="b3628-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3628-104">SYNTAX</span></span>

### <span data-ttu-id="b3628-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3628-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3628-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="b3628-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3628-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3628-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3628-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3628-108">DESCRIPTION</span></span>
<span data-ttu-id="b3628-109">Információkat kap a kiszolgáló tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="b3628-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="b3628-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3628-110">EXAMPLES</span></span>

### <span data-ttu-id="b3628-111">1. példa: A megadott PostgreSql-kiszolgáló tűzfalszabályának felsorolása</span><span class="sxs-lookup"><span data-stu-id="b3628-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="b3628-112">Ez a parancsmag felsorolja a megadott PostgreSql-kiszolgáló tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="b3628-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="b3628-113">2. példa: Tűzfalszabály be szerezni név szerint</span><span class="sxs-lookup"><span data-stu-id="b3628-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="b3628-114">Ez a parancsmag név szerint kapja meg a tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="b3628-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="b3628-115">3. példa: Tűzfalszabály beállítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="b3628-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="b3628-116">Ez a parancsmag identitás szerint kapja meg a tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="b3628-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="b3628-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3628-117">PARAMETERS</span></span>

### <span data-ttu-id="b3628-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3628-118">-DefaultProfile</span></span>
<span data-ttu-id="b3628-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3628-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3628-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3628-120">-InputObject</span></span>
<span data-ttu-id="b3628-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b3628-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b3628-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b3628-122">-Name</span></span>
<span data-ttu-id="b3628-123">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b3628-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3628-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3628-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-125">The name of the resource group.</span></span>
<span data-ttu-id="b3628-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b3628-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b3628-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3628-127">-ServerName</span></span>
<span data-ttu-id="b3628-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-128">The name of the server.</span></span>

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

### <span data-ttu-id="b3628-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3628-129">-SubscriptionId</span></span>
<span data-ttu-id="b3628-130">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b3628-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b3628-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3628-131">CommonParameters</span></span>
<span data-ttu-id="b3628-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3628-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3628-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3628-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3628-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3628-134">INPUTS</span></span>

### <span data-ttu-id="b3628-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b3628-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b3628-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3628-136">OUTPUTS</span></span>

### <span data-ttu-id="b3628-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3628-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b3628-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3628-138">NOTES</span></span>

<span data-ttu-id="b3628-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b3628-139">ALIASES</span></span>

<span data-ttu-id="b3628-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b3628-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3628-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b3628-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3628-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3628-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3628-143">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b3628-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3628-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b3628-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b3628-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b3628-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b3628-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3628-148">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b3628-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b3628-150">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b3628-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="b3628-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b3628-152">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b3628-153">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b3628-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b3628-154">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="b3628-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b3628-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3628-155">RELATED LINKS</span></span>

