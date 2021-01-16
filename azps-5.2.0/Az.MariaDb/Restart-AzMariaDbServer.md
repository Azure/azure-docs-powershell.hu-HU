---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326728"
---
# <span data-ttu-id="93c61-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="93c61-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="93c61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c61-102">SYNOPSIS</span></span>
<span data-ttu-id="93c61-103">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="93c61-103">Restarts a server.</span></span>

## <span data-ttu-id="93c61-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93c61-104">SYNTAX</span></span>

### <span data-ttu-id="93c61-105">ServerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93c61-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93c61-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="93c61-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93c61-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93c61-107">DESCRIPTION</span></span>
<span data-ttu-id="93c61-108">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="93c61-108">Restarts a server.</span></span>

## <span data-ttu-id="93c61-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93c61-109">EXAMPLES</span></span>

### <span data-ttu-id="93c61-110">1. példa: A MariaDB újraindítása</span><span class="sxs-lookup"><span data-stu-id="93c61-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="93c61-111">Ez a parancs újraindítja a MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="93c61-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="93c61-112">2. példa: A MariaDB újraindítása</span><span class="sxs-lookup"><span data-stu-id="93c61-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="93c61-113">Ez a parancs újraindítja a MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="93c61-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="93c61-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93c61-114">PARAMETERS</span></span>

### <span data-ttu-id="93c61-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93c61-115">-AsJob</span></span>
<span data-ttu-id="93c61-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="93c61-116">Run the command as a job</span></span>

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

### <span data-ttu-id="93c61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c61-117">-DefaultProfile</span></span>
<span data-ttu-id="93c61-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93c61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c61-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93c61-119">-InputObject</span></span>
<span data-ttu-id="93c61-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="93c61-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93c61-121">-Name</span><span class="sxs-lookup"><span data-stu-id="93c61-121">-Name</span></span>
<span data-ttu-id="93c61-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c61-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="93c61-123">-NoWait</span></span>
<span data-ttu-id="93c61-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="93c61-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="93c61-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93c61-125">-PassThru</span></span>
<span data-ttu-id="93c61-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="93c61-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="93c61-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93c61-127">-ResourceGroupName</span></span>
<span data-ttu-id="93c61-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="93c61-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="93c61-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c61-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93c61-130">-SubscriptionId</span></span>
<span data-ttu-id="93c61-131">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="93c61-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c61-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93c61-132">-Confirm</span></span>
<span data-ttu-id="93c61-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93c61-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c61-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c61-134">-WhatIf</span></span>
<span data-ttu-id="93c61-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93c61-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c61-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93c61-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93c61-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c61-137">CommonParameters</span></span>
<span data-ttu-id="93c61-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c61-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c61-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93c61-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c61-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93c61-140">INPUTS</span></span>

### <span data-ttu-id="93c61-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="93c61-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="93c61-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93c61-142">OUTPUTS</span></span>

### <span data-ttu-id="93c61-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93c61-143">System.Boolean</span></span>

## <span data-ttu-id="93c61-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93c61-144">NOTES</span></span>

<span data-ttu-id="93c61-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="93c61-145">ALIASES</span></span>

<span data-ttu-id="93c61-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="93c61-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93c61-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="93c61-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93c61-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93c61-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93c61-149">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="93c61-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93c61-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="93c61-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="93c61-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="93c61-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="93c61-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93c61-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="93c61-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="93c61-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="93c61-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="93c61-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="93c61-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="93c61-159">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="93c61-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="93c61-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="93c61-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="93c61-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93c61-161">RELATED LINKS</span></span>

