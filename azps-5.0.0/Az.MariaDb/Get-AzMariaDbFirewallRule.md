---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194619"
---
# <span data-ttu-id="aa4b4-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="aa4b4-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="aa4b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4b4-103">Információt kap a kiszolgálói tűzfalszabályok szabályairól.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="aa4b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa4b4-104">SYNTAX</span></span>

### <span data-ttu-id="aa4b4-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa4b4-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aa4b4-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="aa4b4-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aa4b4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa4b4-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="aa4b4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa4b4-108">DESCRIPTION</span></span>
<span data-ttu-id="aa4b4-109">Információt kap a kiszolgálói tűzfalszabályok szabályairól.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="aa4b4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aa4b4-110">EXAMPLES</span></span>

### <span data-ttu-id="aa4b4-111">Példa 1: az összes tűzfalszabály listázása egy MariaDB alatt</span><span class="sxs-lookup"><span data-stu-id="aa4b4-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="aa4b4-112">Ez a parancs felsorolja az összes girewall szabályt egy MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="aa4b4-113">2. példa: tűzfalszabály beszerzése egy MariaDB alatt</span><span class="sxs-lookup"><span data-stu-id="aa4b4-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="aa4b4-114">Ez a parancs egy MariaDB alatti tűzfal-szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="aa4b4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa4b4-115">PARAMETERS</span></span>

### <span data-ttu-id="aa4b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4b4-116">-DefaultProfile</span></span>
<span data-ttu-id="aa4b4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa4b4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa4b4-118">-InputObject</span></span>
<span data-ttu-id="aa4b4-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa4b4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa4b4-120">-Name</span></span>
<span data-ttu-id="aa4b4-121">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="aa4b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa4b4-123">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aa4b4-124">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aa4b4-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="aa4b4-125">-ServerName</span></span>
<span data-ttu-id="aa4b4-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-126">The name of the server.</span></span>

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

### <span data-ttu-id="aa4b4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa4b4-127">-SubscriptionId</span></span>
<span data-ttu-id="aa4b4-128">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="aa4b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4b4-129">CommonParameters</span></span>
<span data-ttu-id="aa4b4-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa4b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4b4-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4b4-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa4b4-132">INPUTS</span></span>

### <span data-ttu-id="aa4b4-133">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="aa4b4-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="aa4b4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa4b4-134">OUTPUTS</span></span>

### <span data-ttu-id="aa4b4-135">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="aa4b4-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="aa4b4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa4b4-136">NOTES</span></span>

<span data-ttu-id="aa4b4-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aa4b4-137">ALIASES</span></span>

<span data-ttu-id="aa4b4-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="aa4b4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa4b4-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa4b4-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa4b4-141">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="aa4b4-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa4b4-142">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="aa4b4-143">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="aa4b4-144">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="aa4b4-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="aa4b4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa4b4-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="aa4b4-147">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="aa4b4-148">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="aa4b4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="aa4b4-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="aa4b4-151">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="aa4b4-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="aa4b4-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa4b4-153">RELATED LINKS</span></span>

