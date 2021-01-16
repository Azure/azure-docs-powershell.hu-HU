---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: f750718c4bd380b579dff0897b53a68ae4f45b95
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359000"
---
# <span data-ttu-id="fd4c9-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fd4c9-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="fd4c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4c9-103">Információkat kap a kiszolgáló tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="fd4c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd4c9-104">SYNTAX</span></span>

### <span data-ttu-id="fd4c9-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd4c9-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd4c9-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="fd4c9-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd4c9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fd4c9-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fd4c9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd4c9-108">DESCRIPTION</span></span>
<span data-ttu-id="fd4c9-109">Információkat kap a kiszolgáló tűzfalszabályról.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="fd4c9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd4c9-110">EXAMPLES</span></span>

### <span data-ttu-id="fd4c9-111">1. példa: A megadott MySql-kiszolgáló tűzfalszabályának felsorolása</span><span class="sxs-lookup"><span data-stu-id="fd4c9-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="fd4c9-112">Ez a parancsmag felsorolja a megadott MySql-kiszolgáló tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="fd4c9-113">2. példa: Tűzfalszabály be szerezni név szerint</span><span class="sxs-lookup"><span data-stu-id="fd4c9-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="fd4c9-114">Ez a parancsmag név szerint kapja meg a tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="fd4c9-115">3. példa: Tűzfalszabály beállítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="fd4c9-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="fd4c9-116">Ez a parancsmag identitás szerint kapja meg a tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="fd4c9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd4c9-117">PARAMETERS</span></span>

### <span data-ttu-id="fd4c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4c9-118">-DefaultProfile</span></span>
<span data-ttu-id="fd4c9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd4c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd4c9-120">-InputObject</span></span>
<span data-ttu-id="fd4c9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd4c9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fd4c9-122">-Name</span></span>
<span data-ttu-id="fd4c9-123">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="fd4c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd4c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd4c9-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-125">The name of the resource group.</span></span>
<span data-ttu-id="fd4c9-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fd4c9-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fd4c9-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fd4c9-127">-ServerName</span></span>
<span data-ttu-id="fd4c9-128">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-128">The name of the server.</span></span>

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

### <span data-ttu-id="fd4c9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd4c9-129">-SubscriptionId</span></span>
<span data-ttu-id="fd4c9-130">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fd4c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4c9-131">CommonParameters</span></span>
<span data-ttu-id="fd4c9-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4c9-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd4c9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4c9-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd4c9-134">INPUTS</span></span>

### <span data-ttu-id="fd4c9-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fd4c9-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="fd4c9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd4c9-136">OUTPUTS</span></span>

### <span data-ttu-id="fd4c9-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fd4c9-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="fd4c9-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd4c9-138">NOTES</span></span>

<span data-ttu-id="fd4c9-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fd4c9-139">ALIASES</span></span>

<span data-ttu-id="fd4c9-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="fd4c9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd4c9-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd4c9-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd4c9-143">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="fd4c9-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd4c9-144">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fd4c9-145">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fd4c9-146">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fd4c9-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="fd4c9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd4c9-148">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="fd4c9-149">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fd4c9-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fd4c9-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fd4c9-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="fd4c9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fd4c9-153">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fd4c9-154">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fd4c9-155">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fd4c9-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fd4c9-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd4c9-156">RELATED LINKS</span></span>

