---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 89c11be18fbb603f2b05fa9768a3ce05d51ddd86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929930"
---
# <span data-ttu-id="b9567-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9567-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="b9567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9567-102">SYNOPSIS</span></span>
<span data-ttu-id="b9567-103">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="b9567-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b9567-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9567-104">SYNTAX</span></span>

### <span data-ttu-id="b9567-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9567-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9567-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b9567-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9567-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9567-107">DESCRIPTION</span></span>
<span data-ttu-id="b9567-108">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="b9567-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b9567-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9567-109">EXAMPLES</span></span>

### <span data-ttu-id="b9567-110">1. példa: A PostgreSql virtuális hálózat szabályának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="b9567-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="b9567-111">Ez a parancsmag név szerint frissíti a PostgreSql Virtuális hálózat szabályát.</span><span class="sxs-lookup"><span data-stu-id="b9567-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="b9567-112">2. példa: A PostgreSql virtuális hálózat szabályának frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="b9567-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="b9567-113">Ezek a parancsmagok identitás szerint frissítik a PostgreSql virtuális hálózat szabályát.</span><span class="sxs-lookup"><span data-stu-id="b9567-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="b9567-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9567-114">PARAMETERS</span></span>

### <span data-ttu-id="b9567-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9567-115">-AsJob</span></span>
<span data-ttu-id="b9567-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="b9567-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b9567-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9567-117">-DefaultProfile</span></span>
<span data-ttu-id="b9567-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9567-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9567-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9567-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b9567-120">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="b9567-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b9567-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9567-121">-InputObject</span></span>
<span data-ttu-id="b9567-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b9567-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9567-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b9567-123">-Name</span></span>
<span data-ttu-id="b9567-124">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-124">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9567-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b9567-125">-NoWait</span></span>
<span data-ttu-id="b9567-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="b9567-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9567-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9567-127">-PassThru</span></span>
<span data-ttu-id="b9567-128">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="b9567-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b9567-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9567-129">-ResourceGroupName</span></span>
<span data-ttu-id="b9567-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-130">The name of the resource group.</span></span>
<span data-ttu-id="b9567-131">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b9567-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9567-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9567-132">-ServerName</span></span>
<span data-ttu-id="b9567-133">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9567-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b9567-134">-SubnetId</span></span>
<span data-ttu-id="b9567-135">A ARM alhálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b9567-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9567-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9567-136">-SubscriptionId</span></span>
<span data-ttu-id="b9567-137">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b9567-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9567-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9567-138">-Confirm</span></span>
<span data-ttu-id="b9567-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b9567-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9567-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9567-140">-WhatIf</span></span>
<span data-ttu-id="b9567-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b9567-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9567-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9567-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9567-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9567-143">CommonParameters</span></span>
<span data-ttu-id="b9567-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9567-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9567-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9567-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9567-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9567-146">INPUTS</span></span>

### <span data-ttu-id="b9567-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b9567-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b9567-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9567-148">OUTPUTS</span></span>

### <span data-ttu-id="b9567-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9567-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="b9567-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9567-150">NOTES</span></span>

<span data-ttu-id="b9567-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b9567-151">ALIASES</span></span>

<span data-ttu-id="b9567-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b9567-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9567-153">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b9567-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9567-154">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9567-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9567-155">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b9567-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9567-156">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b9567-157">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b9567-158">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b9567-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b9567-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9567-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b9567-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b9567-162">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b9567-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="b9567-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b9567-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b9567-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b9567-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b9567-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="b9567-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b9567-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9567-167">RELATED LINKS</span></span>

