---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: e4ea7cf3b8f85b018ec087122bda8dcfeec066d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003942"
---
# <span data-ttu-id="52b86-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="52b86-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="52b86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b86-102">SYNOPSIS</span></span>
<span data-ttu-id="52b86-103">Töröl egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="52b86-103">Deletes a server.</span></span>

## <span data-ttu-id="52b86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="52b86-104">SYNTAX</span></span>

### <span data-ttu-id="52b86-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52b86-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="52b86-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52b86-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52b86-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="52b86-107">DESCRIPTION</span></span>
<span data-ttu-id="52b86-108">Töröl egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="52b86-108">Deletes a server.</span></span>

## <span data-ttu-id="52b86-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="52b86-109">EXAMPLES</span></span>

### <span data-ttu-id="52b86-110">1. példa: A MariaDB eltávolítása</span><span class="sxs-lookup"><span data-stu-id="52b86-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="52b86-111">Ez a parancs eltávolítja a MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="52b86-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="52b86-112">2. példa: A MariaDB eltávolítása</span><span class="sxs-lookup"><span data-stu-id="52b86-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="52b86-113">Ez a parancs eltávolítja a MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="52b86-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="52b86-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52b86-114">PARAMETERS</span></span>

### <span data-ttu-id="52b86-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52b86-115">-AsJob</span></span>
<span data-ttu-id="52b86-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="52b86-116">Run the command as a job</span></span>

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

### <span data-ttu-id="52b86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b86-117">-DefaultProfile</span></span>
<span data-ttu-id="52b86-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52b86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b86-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52b86-119">-InputObject</span></span>
<span data-ttu-id="52b86-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="52b86-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="52b86-121">-Name</span><span class="sxs-lookup"><span data-stu-id="52b86-121">-Name</span></span>
<span data-ttu-id="52b86-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b86-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="52b86-123">-NoWait</span></span>
<span data-ttu-id="52b86-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="52b86-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="52b86-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52b86-125">-PassThru</span></span>
<span data-ttu-id="52b86-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="52b86-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="52b86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b86-127">-ResourceGroupName</span></span>
<span data-ttu-id="52b86-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="52b86-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="52b86-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="52b86-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52b86-130">-SubscriptionId</span></span>
<span data-ttu-id="52b86-131">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="52b86-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="52b86-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52b86-132">-Confirm</span></span>
<span data-ttu-id="52b86-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="52b86-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b86-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b86-134">-WhatIf</span></span>
<span data-ttu-id="52b86-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="52b86-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b86-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52b86-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b86-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b86-137">CommonParameters</span></span>
<span data-ttu-id="52b86-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b86-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b86-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52b86-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b86-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52b86-140">INPUTS</span></span>

### <span data-ttu-id="52b86-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="52b86-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="52b86-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52b86-142">OUTPUTS</span></span>

### <span data-ttu-id="52b86-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52b86-143">System.Boolean</span></span>

## <span data-ttu-id="52b86-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="52b86-144">NOTES</span></span>

<span data-ttu-id="52b86-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="52b86-145">ALIASES</span></span>

<span data-ttu-id="52b86-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="52b86-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52b86-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="52b86-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52b86-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52b86-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52b86-149">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="52b86-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52b86-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="52b86-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="52b86-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="52b86-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="52b86-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52b86-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="52b86-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="52b86-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="52b86-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="52b86-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="52b86-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="52b86-159">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="52b86-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="52b86-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="52b86-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="52b86-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52b86-161">RELATED LINKS</span></span>

