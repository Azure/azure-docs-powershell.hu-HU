---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: b29f1162f784535ab635c437d9d481bb9f9492cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003973"
---
# <span data-ttu-id="5dff1-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5dff1-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="5dff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dff1-102">SYNOPSIS</span></span>
<span data-ttu-id="5dff1-103">Törli a kiszolgáló tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="5dff1-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="5dff1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5dff1-104">SYNTAX</span></span>

### <span data-ttu-id="5dff1-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5dff1-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5dff1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5dff1-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5dff1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5dff1-107">DESCRIPTION</span></span>
<span data-ttu-id="5dff1-108">Törli a kiszolgáló tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="5dff1-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="5dff1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5dff1-109">EXAMPLES</span></span>

### <span data-ttu-id="5dff1-110">1. példa: Tűzfalszabály eltávolítása a MariaDB-ben</span><span class="sxs-lookup"><span data-stu-id="5dff1-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="5dff1-111">Ez a parancs eltávolítja a tűzfalszabályt a MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="5dff1-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="5dff1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dff1-112">PARAMETERS</span></span>

### <span data-ttu-id="5dff1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5dff1-113">-AsJob</span></span>
<span data-ttu-id="5dff1-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="5dff1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5dff1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dff1-115">-DefaultProfile</span></span>
<span data-ttu-id="5dff1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5dff1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dff1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dff1-117">-InputObject</span></span>
<span data-ttu-id="5dff1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5dff1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dff1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5dff1-119">-Name</span></span>
<span data-ttu-id="5dff1-120">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-120">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dff1-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5dff1-121">-NoWait</span></span>
<span data-ttu-id="5dff1-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="5dff1-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5dff1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dff1-123">-PassThru</span></span>
<span data-ttu-id="5dff1-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="5dff1-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5dff1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dff1-125">-ResourceGroupName</span></span>
<span data-ttu-id="5dff1-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5dff1-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="5dff1-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5dff1-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5dff1-128">-ServerName</span></span>
<span data-ttu-id="5dff1-129">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-129">The name of the server.</span></span>

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

### <span data-ttu-id="5dff1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5dff1-130">-SubscriptionId</span></span>
<span data-ttu-id="5dff1-131">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="5dff1-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5dff1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dff1-132">-Confirm</span></span>
<span data-ttu-id="5dff1-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5dff1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dff1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dff1-134">-WhatIf</span></span>
<span data-ttu-id="5dff1-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5dff1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dff1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5dff1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dff1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dff1-137">CommonParameters</span></span>
<span data-ttu-id="5dff1-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dff1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dff1-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5dff1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dff1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5dff1-140">INPUTS</span></span>

### <span data-ttu-id="5dff1-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="5dff1-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="5dff1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dff1-142">OUTPUTS</span></span>

### <span data-ttu-id="5dff1-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5dff1-143">System.Boolean</span></span>

## <span data-ttu-id="5dff1-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5dff1-144">NOTES</span></span>

<span data-ttu-id="5dff1-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5dff1-145">ALIASES</span></span>

<span data-ttu-id="5dff1-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5dff1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5dff1-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5dff1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5dff1-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5dff1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5dff1-149">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5dff1-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5dff1-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5dff1-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5dff1-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5dff1-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5dff1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5dff1-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5dff1-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5dff1-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="5dff1-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5dff1-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5dff1-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5dff1-159">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="5dff1-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="5dff1-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="5dff1-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5dff1-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5dff1-161">RELATED LINKS</span></span>

