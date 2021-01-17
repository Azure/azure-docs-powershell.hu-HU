---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378432"
---
# <span data-ttu-id="86ee2-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="86ee2-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="86ee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="86ee2-103">Virtuális hálózati szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="86ee2-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="86ee2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86ee2-104">SYNTAX</span></span>

### <span data-ttu-id="86ee2-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86ee2-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="86ee2-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="86ee2-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="86ee2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="86ee2-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="86ee2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86ee2-108">DESCRIPTION</span></span>
<span data-ttu-id="86ee2-109">Virtuális hálózati szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="86ee2-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="86ee2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86ee2-110">EXAMPLES</span></span>

### <span data-ttu-id="86ee2-111">1. példa: A virtuális hálózatra vonatkozó szabályok felsorolása a megadott PostgreSql-kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="86ee2-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="86ee2-112">Ez a parancsmag felsorolja a virtuális hálózatra vonatkozó szabályokat a megadott PostgreSql-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="86ee2-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="86ee2-113">2. példa: Virtuális hálózat szabályának lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="86ee2-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="86ee2-114">Ez a parancsmag név szerint virtuális hálózatszabályt kap.</span><span class="sxs-lookup"><span data-stu-id="86ee2-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="86ee2-115">3. példa: Virtuális hálózat szabályának lekérte identitás alapján</span><span class="sxs-lookup"><span data-stu-id="86ee2-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="86ee2-116">Ez a parancsmag identitás szerint virtuális hálózatszabályt kap.</span><span class="sxs-lookup"><span data-stu-id="86ee2-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="86ee2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86ee2-117">PARAMETERS</span></span>

### <span data-ttu-id="86ee2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ee2-118">-DefaultProfile</span></span>
<span data-ttu-id="86ee2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86ee2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86ee2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86ee2-120">-InputObject</span></span>
<span data-ttu-id="86ee2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="86ee2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="86ee2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="86ee2-122">-Name</span></span>
<span data-ttu-id="86ee2-123">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="86ee2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86ee2-124">-PassThru</span></span>
<span data-ttu-id="86ee2-125">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="86ee2-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="86ee2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ee2-126">-ResourceGroupName</span></span>
<span data-ttu-id="86ee2-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-127">The name of the resource group.</span></span>
<span data-ttu-id="86ee2-128">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="86ee2-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="86ee2-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86ee2-129">-ServerName</span></span>
<span data-ttu-id="86ee2-130">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-130">The name of the server.</span></span>

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

### <span data-ttu-id="86ee2-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86ee2-131">-SubscriptionId</span></span>
<span data-ttu-id="86ee2-132">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="86ee2-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="86ee2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ee2-133">CommonParameters</span></span>
<span data-ttu-id="86ee2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ee2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ee2-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86ee2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ee2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86ee2-136">INPUTS</span></span>

### <span data-ttu-id="86ee2-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="86ee2-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="86ee2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86ee2-138">OUTPUTS</span></span>

### <span data-ttu-id="86ee2-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="86ee2-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="86ee2-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86ee2-140">NOTES</span></span>

<span data-ttu-id="86ee2-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="86ee2-141">ALIASES</span></span>

<span data-ttu-id="86ee2-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="86ee2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86ee2-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="86ee2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86ee2-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86ee2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86ee2-145">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="86ee2-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="86ee2-146">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="86ee2-147">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="86ee2-148">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="86ee2-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="86ee2-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86ee2-150">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="86ee2-151">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="86ee2-152">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="86ee2-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="86ee2-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="86ee2-154">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="86ee2-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="86ee2-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="86ee2-156">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="86ee2-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="86ee2-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86ee2-157">RELATED LINKS</span></span>

