---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: 11278c1d317f6f4e0171513a4503c5681506f1ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194305"
---
# <span data-ttu-id="c6867-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c6867-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="c6867-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6867-102">SYNOPSIS</span></span>
<span data-ttu-id="c6867-103">Információt kap a kiszolgálói tűzfalszabályok szabályairól.</span><span class="sxs-lookup"><span data-stu-id="c6867-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="c6867-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6867-104">SYNTAX</span></span>

### <span data-ttu-id="c6867-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6867-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6867-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c6867-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6867-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6867-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c6867-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6867-108">DESCRIPTION</span></span>
<span data-ttu-id="c6867-109">Információt kap a kiszolgálói tűzfalszabályok szabályairól.</span><span class="sxs-lookup"><span data-stu-id="c6867-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="c6867-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c6867-110">EXAMPLES</span></span>

### <span data-ttu-id="c6867-111">Példa 1: a megadott MySql-kiszolgálón lévő összes tűzfal-szabály listázása</span><span class="sxs-lookup"><span data-stu-id="c6867-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="c6867-112">Ez a parancsmag felsorolja az összes tűzfal-szabályt a megadott MySql-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="c6867-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="c6867-113">2. példa: tűzfalszabály beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="c6867-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="c6867-114">Ez a parancsmag a tűzfal szabályait név szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="c6867-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="c6867-115">3. példa: tűzfalszabályok beszerzése identitással</span><span class="sxs-lookup"><span data-stu-id="c6867-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="c6867-116">Ez a parancsmag identitással kapja meg a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="c6867-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="c6867-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6867-117">PARAMETERS</span></span>

### <span data-ttu-id="c6867-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6867-118">-DefaultProfile</span></span>
<span data-ttu-id="c6867-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6867-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6867-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6867-120">-InputObject</span></span>
<span data-ttu-id="c6867-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6867-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c6867-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6867-122">-Name</span></span>
<span data-ttu-id="c6867-123">A kiszolgáló tűzfal-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="c6867-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6867-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6867-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-125">The name of the resource group.</span></span>
<span data-ttu-id="c6867-126">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="c6867-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c6867-127">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c6867-127">-ServerName</span></span>
<span data-ttu-id="c6867-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-128">The name of the server.</span></span>

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

### <span data-ttu-id="c6867-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6867-129">-SubscriptionId</span></span>
<span data-ttu-id="c6867-130">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c6867-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c6867-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6867-131">CommonParameters</span></span>
<span data-ttu-id="c6867-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6867-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6867-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6867-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6867-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6867-134">INPUTS</span></span>

### <span data-ttu-id="c6867-135">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c6867-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c6867-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6867-136">OUTPUTS</span></span>

### <span data-ttu-id="c6867-137">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c6867-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="c6867-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6867-138">NOTES</span></span>

<span data-ttu-id="c6867-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c6867-139">ALIASES</span></span>

<span data-ttu-id="c6867-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c6867-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6867-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c6867-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6867-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c6867-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6867-143">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c6867-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6867-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c6867-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c6867-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c6867-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c6867-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6867-148">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c6867-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c6867-150">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="c6867-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="c6867-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c6867-152">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c6867-153">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c6867-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c6867-154">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="c6867-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c6867-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6867-155">RELATED LINKS</span></span>

