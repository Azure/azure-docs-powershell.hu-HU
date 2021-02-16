---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 9c1a0d2746b40402982f1e904548d92f2776819f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146330"
---
# <span data-ttu-id="d59ab-101">Restart-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="d59ab-101">Restart-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="d59ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d59ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d59ab-103">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="d59ab-103">Restarts a server.</span></span>

## <span data-ttu-id="d59ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d59ab-104">SYNTAX</span></span>

### <span data-ttu-id="d59ab-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d59ab-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d59ab-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d59ab-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d59ab-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d59ab-107">DESCRIPTION</span></span>
<span data-ttu-id="d59ab-108">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="d59ab-108">Restarts a server.</span></span>

## <span data-ttu-id="d59ab-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d59ab-109">EXAMPLES</span></span>

### <span data-ttu-id="d59ab-110">1. példa: A kiszolgáló újraindítása erőforrásnév alapján</span><span class="sxs-lookup"><span data-stu-id="d59ab-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="d59ab-111">A kiszolgáló újraindítása név szerint</span><span class="sxs-lookup"><span data-stu-id="d59ab-111">Restart the server by name</span></span>

### <span data-ttu-id="d59ab-112">2. példa: A kiszolgáló újraindítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="d59ab-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/restart"
PS C:\> Restart-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="d59ab-113">A kiszolgáló újraindítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="d59ab-113">Restart the server by identity</span></span>

## <span data-ttu-id="d59ab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d59ab-114">PARAMETERS</span></span>

### <span data-ttu-id="d59ab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d59ab-115">-AsJob</span></span>
<span data-ttu-id="d59ab-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d59ab-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d59ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59ab-117">-DefaultProfile</span></span>
<span data-ttu-id="d59ab-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d59ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d59ab-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d59ab-119">-InputObject</span></span>
<span data-ttu-id="d59ab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d59ab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d59ab-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d59ab-121">-Name</span></span>
<span data-ttu-id="d59ab-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59ab-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d59ab-123">-NoWait</span></span>
<span data-ttu-id="d59ab-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d59ab-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d59ab-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d59ab-125">-PassThru</span></span>
<span data-ttu-id="d59ab-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="d59ab-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d59ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d59ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="d59ab-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-128">The name of the resource group.</span></span>
<span data-ttu-id="d59ab-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d59ab-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59ab-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d59ab-130">-SubscriptionId</span></span>
<span data-ttu-id="d59ab-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d59ab-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59ab-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d59ab-132">-Confirm</span></span>
<span data-ttu-id="d59ab-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d59ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d59ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d59ab-134">-WhatIf</span></span>
<span data-ttu-id="d59ab-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d59ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d59ab-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d59ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d59ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59ab-137">CommonParameters</span></span>
<span data-ttu-id="d59ab-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59ab-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d59ab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59ab-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d59ab-140">INPUTS</span></span>

### <span data-ttu-id="d59ab-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d59ab-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d59ab-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d59ab-142">OUTPUTS</span></span>

### <span data-ttu-id="d59ab-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d59ab-143">System.Boolean</span></span>

## <span data-ttu-id="d59ab-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d59ab-144">NOTES</span></span>

<span data-ttu-id="d59ab-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d59ab-145">ALIASES</span></span>

<span data-ttu-id="d59ab-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d59ab-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d59ab-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d59ab-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d59ab-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d59ab-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d59ab-149">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d59ab-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d59ab-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d59ab-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d59ab-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d59ab-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d59ab-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d59ab-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d59ab-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d59ab-156">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d59ab-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="d59ab-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d59ab-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d59ab-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d59ab-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d59ab-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="d59ab-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d59ab-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d59ab-161">RELATED LINKS</span></span>

