---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 572943ea0f694b5a3a68ff4c1c030a1a3a1fc0f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926985"
---
# <span data-ttu-id="ac054-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ac054-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="ac054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac054-102">SYNOPSIS</span></span>
<span data-ttu-id="ac054-103">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="ac054-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ac054-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac054-104">SYNTAX</span></span>

### <span data-ttu-id="ac054-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac054-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac054-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ac054-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac054-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac054-107">DESCRIPTION</span></span>
<span data-ttu-id="ac054-108">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="ac054-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ac054-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac054-109">EXAMPLES</span></span>

### <span data-ttu-id="ac054-110">1. példa: A MySql virtuális hálózat szabályának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="ac054-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="ac054-111">Ez a parancsmag név szerint frissíti a MySql virtuális hálózat szabályát.</span><span class="sxs-lookup"><span data-stu-id="ac054-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="ac054-112">2. példa: A MySql virtuális hálózat szabályának frissítése identitás alapján.</span><span class="sxs-lookup"><span data-stu-id="ac054-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="ac054-113">Ezek a parancsmagok identitás szerint frissítik a MySql virtuális hálózat szabályát.</span><span class="sxs-lookup"><span data-stu-id="ac054-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="ac054-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac054-114">PARAMETERS</span></span>

### <span data-ttu-id="ac054-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac054-115">-AsJob</span></span>
<span data-ttu-id="ac054-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="ac054-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ac054-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac054-117">-DefaultProfile</span></span>
<span data-ttu-id="ac054-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac054-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac054-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac054-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="ac054-120">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="ac054-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="ac054-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac054-121">-InputObject</span></span>
<span data-ttu-id="ac054-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ac054-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac054-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ac054-123">-Name</span></span>
<span data-ttu-id="ac054-124">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ac054-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac054-125">-NoWait</span></span>
<span data-ttu-id="ac054-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="ac054-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac054-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac054-127">-PassThru</span></span>
<span data-ttu-id="ac054-128">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="ac054-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ac054-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac054-129">-ResourceGroupName</span></span>
<span data-ttu-id="ac054-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-130">The name of the resource group.</span></span>
<span data-ttu-id="ac054-131">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ac054-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ac054-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ac054-132">-ServerName</span></span>
<span data-ttu-id="ac054-133">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-133">The name of the server.</span></span>

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

### <span data-ttu-id="ac054-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ac054-134">-SubnetId</span></span>
<span data-ttu-id="ac054-135">A ARM alhálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac054-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="ac054-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac054-136">-SubscriptionId</span></span>
<span data-ttu-id="ac054-137">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac054-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ac054-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac054-138">-Confirm</span></span>
<span data-ttu-id="ac054-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ac054-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac054-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac054-140">-WhatIf</span></span>
<span data-ttu-id="ac054-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ac054-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac054-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac054-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac054-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac054-143">CommonParameters</span></span>
<span data-ttu-id="ac054-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac054-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac054-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac054-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac054-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac054-146">INPUTS</span></span>

### <span data-ttu-id="ac054-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ac054-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ac054-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac054-148">OUTPUTS</span></span>

### <span data-ttu-id="ac054-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ac054-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="ac054-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac054-150">NOTES</span></span>

<span data-ttu-id="ac054-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ac054-151">ALIASES</span></span>

<span data-ttu-id="ac054-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ac054-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac054-153">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ac054-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac054-154">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac054-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac054-155">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ac054-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac054-156">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ac054-157">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ac054-158">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ac054-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ac054-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac054-160">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ac054-161">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ac054-162">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ac054-163">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ac054-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="ac054-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ac054-165">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ac054-166">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac054-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ac054-167">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="ac054-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ac054-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac054-168">RELATED LINKS</span></span>

