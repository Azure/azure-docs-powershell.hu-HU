---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 30e361d77f3c3b738703e1dde075ccbabc38b0b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932538"
---
# <span data-ttu-id="9e99d-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9e99d-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="9e99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e99d-102">SYNOPSIS</span></span>
<span data-ttu-id="9e99d-103">Virtuális hálózati szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="9e99d-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="9e99d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e99d-104">SYNTAX</span></span>

### <span data-ttu-id="9e99d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e99d-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9e99d-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="9e99d-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9e99d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e99d-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="9e99d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e99d-108">DESCRIPTION</span></span>
<span data-ttu-id="9e99d-109">Virtuális hálózati szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="9e99d-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="9e99d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e99d-110">EXAMPLES</span></span>

### <span data-ttu-id="9e99d-111">1. példa: A megadott MySql-kiszolgáló összes virtuális hálózati szabályának felsorolása</span><span class="sxs-lookup"><span data-stu-id="9e99d-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9e99d-112">Ez a parancsmag felsorolja a megadott MySql-kiszolgáló összes virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="9e99d-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="9e99d-113">2. példa: Virtuális hálózat szabályának lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="9e99d-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9e99d-114">Ez a parancsmag név szerint virtuális hálózatszabályt kap.</span><span class="sxs-lookup"><span data-stu-id="9e99d-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="9e99d-115">3. példa: Virtuális hálózat szabályának lekérte identitás alapján</span><span class="sxs-lookup"><span data-stu-id="9e99d-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9e99d-116">Ez a parancsmag identitás szerint virtuális hálózatszabályt kap.</span><span class="sxs-lookup"><span data-stu-id="9e99d-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="9e99d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e99d-117">PARAMETERS</span></span>

### <span data-ttu-id="9e99d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e99d-118">-DefaultProfile</span></span>
<span data-ttu-id="9e99d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e99d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e99d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e99d-120">-InputObject</span></span>
<span data-ttu-id="9e99d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9e99d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e99d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9e99d-122">-Name</span></span>
<span data-ttu-id="9e99d-123">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e99d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e99d-124">-PassThru</span></span>
<span data-ttu-id="9e99d-125">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="9e99d-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e99d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e99d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9e99d-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-127">The name of the resource group.</span></span>
<span data-ttu-id="9e99d-128">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9e99d-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9e99d-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e99d-129">-ServerName</span></span>
<span data-ttu-id="9e99d-130">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-130">The name of the server.</span></span>

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

### <span data-ttu-id="9e99d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e99d-131">-SubscriptionId</span></span>
<span data-ttu-id="9e99d-132">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9e99d-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9e99d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e99d-133">CommonParameters</span></span>
<span data-ttu-id="9e99d-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e99d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e99d-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e99d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e99d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e99d-136">INPUTS</span></span>

### <span data-ttu-id="9e99d-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9e99d-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9e99d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e99d-138">OUTPUTS</span></span>

### <span data-ttu-id="9e99d-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9e99d-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="9e99d-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e99d-140">NOTES</span></span>

<span data-ttu-id="9e99d-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9e99d-141">ALIASES</span></span>

<span data-ttu-id="9e99d-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9e99d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e99d-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9e99d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e99d-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e99d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e99d-145">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9e99d-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e99d-146">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9e99d-147">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9e99d-148">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9e99d-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9e99d-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e99d-150">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="9e99d-151">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9e99d-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9e99d-153">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9e99d-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="9e99d-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9e99d-155">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9e99d-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9e99d-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9e99d-157">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9e99d-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9e99d-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e99d-158">RELATED LINKS</span></span>

