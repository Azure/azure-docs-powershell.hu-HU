---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469393"
---
# <span data-ttu-id="fa81c-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fa81c-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="fa81c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa81c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa81c-103">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="fa81c-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="fa81c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa81c-104">SYNTAX</span></span>

### <span data-ttu-id="fa81c-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa81c-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fa81c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fa81c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fa81c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa81c-107">DESCRIPTION</span></span>
<span data-ttu-id="fa81c-108">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="fa81c-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="fa81c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa81c-109">EXAMPLES</span></span>

### <span data-ttu-id="fa81c-110">1. példa: A MariaDB virtuális hálózati szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="fa81c-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="fa81c-111">Ez a parancs frissíti a virtuális hálózati szabályokat.</span><span class="sxs-lookup"><span data-stu-id="fa81c-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="fa81c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa81c-112">PARAMETERS</span></span>

### <span data-ttu-id="fa81c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa81c-113">-AsJob</span></span>
<span data-ttu-id="fa81c-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="fa81c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="fa81c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa81c-115">-DefaultProfile</span></span>
<span data-ttu-id="fa81c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa81c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa81c-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa81c-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="fa81c-118">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="fa81c-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="fa81c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa81c-119">-InputObject</span></span>
<span data-ttu-id="fa81c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fa81c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa81c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fa81c-121">-Name</span></span>
<span data-ttu-id="fa81c-122">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="fa81c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fa81c-123">-NoWait</span></span>
<span data-ttu-id="fa81c-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="fa81c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fa81c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa81c-125">-PassThru</span></span>
<span data-ttu-id="fa81c-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="fa81c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fa81c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa81c-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa81c-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fa81c-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="fa81c-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fa81c-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fa81c-130">-ServerName</span></span>
<span data-ttu-id="fa81c-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-131">The name of the server.</span></span>

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

### <span data-ttu-id="fa81c-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fa81c-132">-SubnetId</span></span>
<span data-ttu-id="fa81c-133">A ARM alhálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fa81c-133">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa81c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa81c-134">-SubscriptionId</span></span>
<span data-ttu-id="fa81c-135">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="fa81c-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="fa81c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa81c-136">-Confirm</span></span>
<span data-ttu-id="fa81c-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fa81c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa81c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa81c-138">-WhatIf</span></span>
<span data-ttu-id="fa81c-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fa81c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa81c-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa81c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa81c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa81c-141">CommonParameters</span></span>
<span data-ttu-id="fa81c-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa81c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa81c-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa81c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa81c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa81c-144">INPUTS</span></span>

### <span data-ttu-id="fa81c-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="fa81c-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="fa81c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa81c-146">OUTPUTS</span></span>

### <span data-ttu-id="fa81c-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fa81c-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="fa81c-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa81c-148">NOTES</span></span>

<span data-ttu-id="fa81c-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fa81c-149">ALIASES</span></span>

<span data-ttu-id="fa81c-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="fa81c-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fa81c-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="fa81c-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fa81c-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fa81c-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fa81c-153">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="fa81c-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fa81c-154">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fa81c-155">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fa81c-156">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fa81c-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="fa81c-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fa81c-158">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fa81c-159">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fa81c-160">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="fa81c-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fa81c-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fa81c-162">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fa81c-163">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="fa81c-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="fa81c-164">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="fa81c-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fa81c-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa81c-165">RELATED LINKS</span></span>

