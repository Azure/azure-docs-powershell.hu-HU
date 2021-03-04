---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restart-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
ms.openlocfilehash: 74174648a1c8b743357bb6036e213f0674ab959d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941113"
---
# <span data-ttu-id="77f87-101">Restart-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="77f87-101">Restart-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="77f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77f87-102">SYNOPSIS</span></span>
<span data-ttu-id="77f87-103">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="77f87-103">Restarts a server.</span></span>

## <span data-ttu-id="77f87-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77f87-104">SYNTAX</span></span>

### <span data-ttu-id="77f87-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77f87-105">Restart (Default)</span></span>
```
Restart-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="77f87-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="77f87-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="77f87-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77f87-107">DESCRIPTION</span></span>
<span data-ttu-id="77f87-108">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="77f87-108">Restarts a server.</span></span>

## <span data-ttu-id="77f87-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77f87-109">EXAMPLES</span></span>

### <span data-ttu-id="77f87-110">1. példa: A kiszolgáló újraindítása erőforrásnév alapján</span><span class="sxs-lookup"><span data-stu-id="77f87-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="77f87-111">A kiszolgáló újraindítása név szerint</span><span class="sxs-lookup"><span data-stu-id="77f87-111">Restart the server by name</span></span>

### <span data-ttu-id="77f87-112">2. példa: A kiszolgáló újraindítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="77f87-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/restart"
PS C:\> Restart-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="77f87-113">A kiszolgáló újraindítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="77f87-113">Restart the server by identity</span></span>

## <span data-ttu-id="77f87-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77f87-114">PARAMETERS</span></span>

### <span data-ttu-id="77f87-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77f87-115">-AsJob</span></span>
<span data-ttu-id="77f87-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="77f87-116">Run the command as a job</span></span>

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

### <span data-ttu-id="77f87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f87-117">-DefaultProfile</span></span>
<span data-ttu-id="77f87-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77f87-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f87-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77f87-119">-InputObject</span></span>
<span data-ttu-id="77f87-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="77f87-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77f87-121">-Name</span><span class="sxs-lookup"><span data-stu-id="77f87-121">-Name</span></span>
<span data-ttu-id="77f87-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-122">The name of the server.</span></span>

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

### <span data-ttu-id="77f87-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="77f87-123">-NoWait</span></span>
<span data-ttu-id="77f87-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="77f87-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="77f87-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77f87-125">-PassThru</span></span>
<span data-ttu-id="77f87-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="77f87-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="77f87-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f87-127">-ResourceGroupName</span></span>
<span data-ttu-id="77f87-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-128">The name of the resource group.</span></span>
<span data-ttu-id="77f87-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="77f87-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="77f87-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77f87-130">-SubscriptionId</span></span>
<span data-ttu-id="77f87-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="77f87-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="77f87-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77f87-132">-Confirm</span></span>
<span data-ttu-id="77f87-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="77f87-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77f87-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f87-134">-WhatIf</span></span>
<span data-ttu-id="77f87-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="77f87-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77f87-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77f87-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77f87-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f87-137">CommonParameters</span></span>
<span data-ttu-id="77f87-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f87-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f87-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77f87-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f87-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77f87-140">INPUTS</span></span>

### <span data-ttu-id="77f87-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="77f87-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="77f87-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77f87-142">OUTPUTS</span></span>

### <span data-ttu-id="77f87-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77f87-143">System.Boolean</span></span>

## <span data-ttu-id="77f87-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77f87-144">NOTES</span></span>

<span data-ttu-id="77f87-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="77f87-145">ALIASES</span></span>

<span data-ttu-id="77f87-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="77f87-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="77f87-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="77f87-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="77f87-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="77f87-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="77f87-149">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="77f87-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="77f87-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="77f87-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="77f87-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="77f87-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="77f87-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="77f87-154">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="77f87-155">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="77f87-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="77f87-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="77f87-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="77f87-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="77f87-159">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="77f87-160">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="77f87-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="77f87-161">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="77f87-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="77f87-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77f87-162">RELATED LINKS</span></span>

