---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 1c7b3c1f64637554745e960fadfe93cb3d87fa84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940402"
---
# <span data-ttu-id="18c42-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="18c42-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="18c42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18c42-102">SYNOPSIS</span></span>
<span data-ttu-id="18c42-103">Információkat kap a kiszolgáló tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="18c42-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="18c42-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18c42-104">SYNTAX</span></span>

### <span data-ttu-id="18c42-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18c42-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18c42-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="18c42-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18c42-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="18c42-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="18c42-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18c42-108">DESCRIPTION</span></span>
<span data-ttu-id="18c42-109">Információkat kap a kiszolgáló tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="18c42-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="18c42-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18c42-110">EXAMPLES</span></span>

### <span data-ttu-id="18c42-111">1. példa: Az összes tűzfalszabály felsorolása a MariaDB-ben</span><span class="sxs-lookup"><span data-stu-id="18c42-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="18c42-112">Ez a parancs felsorolja a MariaDB alatti összes girewall szabályt.</span><span class="sxs-lookup"><span data-stu-id="18c42-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="18c42-113">2. példa: Tűzfalszabály létrehozása a MariaDB-ben</span><span class="sxs-lookup"><span data-stu-id="18c42-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="18c42-114">Ez a parancs egy tűzfalszabályt kap Egy MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="18c42-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="18c42-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18c42-115">PARAMETERS</span></span>

### <span data-ttu-id="18c42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c42-116">-DefaultProfile</span></span>
<span data-ttu-id="18c42-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18c42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18c42-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18c42-118">-InputObject</span></span>
<span data-ttu-id="18c42-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="18c42-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18c42-120">-Name</span><span class="sxs-lookup"><span data-stu-id="18c42-120">-Name</span></span>
<span data-ttu-id="18c42-121">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="18c42-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c42-122">-ResourceGroupName</span></span>
<span data-ttu-id="18c42-123">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="18c42-124">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="18c42-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="18c42-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="18c42-125">-ServerName</span></span>
<span data-ttu-id="18c42-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-126">The name of the server.</span></span>

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

### <span data-ttu-id="18c42-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18c42-127">-SubscriptionId</span></span>
<span data-ttu-id="18c42-128">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="18c42-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="18c42-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c42-129">CommonParameters</span></span>
<span data-ttu-id="18c42-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c42-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c42-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18c42-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c42-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18c42-132">INPUTS</span></span>

### <span data-ttu-id="18c42-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="18c42-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="18c42-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18c42-134">OUTPUTS</span></span>

### <span data-ttu-id="18c42-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="18c42-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="18c42-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18c42-136">NOTES</span></span>

<span data-ttu-id="18c42-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="18c42-137">ALIASES</span></span>

<span data-ttu-id="18c42-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="18c42-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18c42-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="18c42-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18c42-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18c42-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18c42-141">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="18c42-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18c42-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="18c42-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="18c42-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="18c42-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="18c42-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18c42-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="18c42-147">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="18c42-148">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="18c42-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="18c42-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="18c42-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="18c42-151">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="18c42-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="18c42-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="18c42-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="18c42-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18c42-153">RELATED LINKS</span></span>

