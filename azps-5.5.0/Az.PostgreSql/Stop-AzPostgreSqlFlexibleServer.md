---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/stop-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 02a7d917a63fa7913603a8bc5672f6a41ca8ed2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206247"
---
# <span data-ttu-id="30a00-101">Stop-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="30a00-101">Stop-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="30a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30a00-102">SYNOPSIS</span></span>
<span data-ttu-id="30a00-103">Leállítja a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="30a00-103">Stops a server.</span></span>

## <span data-ttu-id="30a00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30a00-104">SYNTAX</span></span>

### <span data-ttu-id="30a00-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30a00-105">Stop (Default)</span></span>
```
Stop-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30a00-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30a00-106">StopViaIdentity</span></span>
```
Stop-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30a00-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30a00-107">DESCRIPTION</span></span>
<span data-ttu-id="30a00-108">Leállítja a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="30a00-108">Stops a server.</span></span>

## <span data-ttu-id="30a00-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30a00-109">EXAMPLES</span></span>

### <span data-ttu-id="30a00-110">1. példa: A kiszolgáló leállítása erőforrásnév szerint</span><span class="sxs-lookup"><span data-stu-id="30a00-110">Example 1: Stop the server by resource name</span></span>
```powershell
PS C:\> Stop-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="30a00-111">A kiszolgáló név szerint való leállítása</span><span class="sxs-lookup"><span data-stu-id="30a00-111">Stop the server by name</span></span>

### <span data-ttu-id="30a00-112">2. példa: A kiszolgáló leállítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="30a00-112">Example 2: Stop the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/stop"
PS C:\> Stop-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="30a00-113">A kiszolgáló leállítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="30a00-113">Stop the server by identity</span></span>

## <span data-ttu-id="30a00-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30a00-114">PARAMETERS</span></span>

### <span data-ttu-id="30a00-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30a00-115">-AsJob</span></span>
<span data-ttu-id="30a00-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="30a00-116">Run the command as a job</span></span>

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

### <span data-ttu-id="30a00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a00-117">-DefaultProfile</span></span>
<span data-ttu-id="30a00-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30a00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a00-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30a00-119">-InputObject</span></span>
<span data-ttu-id="30a00-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="30a00-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30a00-121">-Name</span><span class="sxs-lookup"><span data-stu-id="30a00-121">-Name</span></span>
<span data-ttu-id="30a00-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a00-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="30a00-123">-NoWait</span></span>
<span data-ttu-id="30a00-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="30a00-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30a00-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30a00-125">-PassThru</span></span>
<span data-ttu-id="30a00-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="30a00-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="30a00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a00-127">-ResourceGroupName</span></span>
<span data-ttu-id="30a00-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-128">The name of the resource group.</span></span>
<span data-ttu-id="30a00-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="30a00-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a00-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30a00-130">-SubscriptionId</span></span>
<span data-ttu-id="30a00-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="30a00-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a00-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30a00-132">-Confirm</span></span>
<span data-ttu-id="30a00-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="30a00-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a00-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a00-134">-WhatIf</span></span>
<span data-ttu-id="30a00-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="30a00-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a00-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30a00-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a00-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a00-137">CommonParameters</span></span>
<span data-ttu-id="30a00-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a00-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a00-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30a00-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a00-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30a00-140">INPUTS</span></span>

### <span data-ttu-id="30a00-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="30a00-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="30a00-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30a00-142">OUTPUTS</span></span>

### <span data-ttu-id="30a00-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30a00-143">System.Boolean</span></span>

## <span data-ttu-id="30a00-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30a00-144">NOTES</span></span>

<span data-ttu-id="30a00-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="30a00-145">ALIASES</span></span>

<span data-ttu-id="30a00-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="30a00-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30a00-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="30a00-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30a00-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30a00-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30a00-149">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="30a00-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30a00-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="30a00-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="30a00-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="30a00-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="30a00-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30a00-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="30a00-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="30a00-156">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="30a00-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="30a00-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="30a00-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="30a00-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="30a00-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="30a00-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="30a00-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="30a00-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30a00-161">RELATED LINKS</span></span>

