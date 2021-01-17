---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 224d60bdeca8b8884be02a716159374f5d0e31c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360385"
---
# <span data-ttu-id="775ae-101">Remove-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="775ae-101">Remove-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="775ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="775ae-102">SYNOPSIS</span></span>
<span data-ttu-id="775ae-103">A megadott nevű virtuális hálózati szabály törlése.</span><span class="sxs-lookup"><span data-stu-id="775ae-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="775ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="775ae-104">SYNTAX</span></span>

### <span data-ttu-id="775ae-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="775ae-105">Delete (Default)</span></span>
```
Remove-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="775ae-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="775ae-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="775ae-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="775ae-107">DESCRIPTION</span></span>
<span data-ttu-id="775ae-108">A megadott nevű virtuális hálózati szabály törlése.</span><span class="sxs-lookup"><span data-stu-id="775ae-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="775ae-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="775ae-109">EXAMPLES</span></span>

### <span data-ttu-id="775ae-110">1. példa: A MySql-kiszolgáló virtuális hálózatszabályának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="775ae-110">Example 1: Remove MySql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest-ServerName mysql-test

```

<span data-ttu-id="775ae-111">Ez a parancsmag név szerint eltávolítja a MySql-kiszolgáló virtuális hálózatszabályát.</span><span class="sxs-lookup"><span data-stu-id="775ae-111">This cmdlet removes MySql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="775ae-112">2. példa: A MySql-kiszolgáló virtuális hálózatszabályának eltávolítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="775ae-112">Example 2: Remove MySql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Remove-AzMySqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="775ae-113">Ezek a parancsmagok identitás szerint eltávolítják a MySql-kiszolgáló virtuális hálózatszabályát.</span><span class="sxs-lookup"><span data-stu-id="775ae-113">These cmdlets remove MySql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="775ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="775ae-114">PARAMETERS</span></span>

### <span data-ttu-id="775ae-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="775ae-115">-AsJob</span></span>
<span data-ttu-id="775ae-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="775ae-116">Run the command as a job</span></span>

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

### <span data-ttu-id="775ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775ae-117">-DefaultProfile</span></span>
<span data-ttu-id="775ae-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="775ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="775ae-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="775ae-119">-InputObject</span></span>
<span data-ttu-id="775ae-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="775ae-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="775ae-121">-Name</span><span class="sxs-lookup"><span data-stu-id="775ae-121">-Name</span></span>
<span data-ttu-id="775ae-122">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775ae-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="775ae-123">-NoWait</span></span>
<span data-ttu-id="775ae-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="775ae-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="775ae-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="775ae-125">-PassThru</span></span>
<span data-ttu-id="775ae-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="775ae-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="775ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="775ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="775ae-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-128">The name of the resource group.</span></span>
<span data-ttu-id="775ae-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="775ae-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775ae-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="775ae-130">-ServerName</span></span>
<span data-ttu-id="775ae-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775ae-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="775ae-132">-SubscriptionId</span></span>
<span data-ttu-id="775ae-133">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="775ae-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775ae-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="775ae-134">-Confirm</span></span>
<span data-ttu-id="775ae-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="775ae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="775ae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="775ae-136">-WhatIf</span></span>
<span data-ttu-id="775ae-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="775ae-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="775ae-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="775ae-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="775ae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775ae-139">CommonParameters</span></span>
<span data-ttu-id="775ae-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="775ae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775ae-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="775ae-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775ae-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="775ae-142">INPUTS</span></span>

### <span data-ttu-id="775ae-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="775ae-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="775ae-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="775ae-144">OUTPUTS</span></span>

### <span data-ttu-id="775ae-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="775ae-145">System.Boolean</span></span>

## <span data-ttu-id="775ae-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="775ae-146">NOTES</span></span>

<span data-ttu-id="775ae-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="775ae-147">ALIASES</span></span>

<span data-ttu-id="775ae-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="775ae-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="775ae-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="775ae-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="775ae-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="775ae-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="775ae-151">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="775ae-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="775ae-152">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="775ae-153">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="775ae-154">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="775ae-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="775ae-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="775ae-156">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="775ae-157">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="775ae-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="775ae-159">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="775ae-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="775ae-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="775ae-161">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="775ae-162">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="775ae-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="775ae-163">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="775ae-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="775ae-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="775ae-164">RELATED LINKS</span></span>

