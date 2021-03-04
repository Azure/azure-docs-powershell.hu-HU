---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/start-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Start-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Start-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 52ce5b9126fdaae430878c14873a97b0da8737d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919402"
---
# <span data-ttu-id="1f4b2-101">Start-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="1f4b2-101">Start-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="1f4b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f4b2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4b2-103">Kiszolgáló indítása.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-103">Starts a server.</span></span>

## <span data-ttu-id="1f4b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1f4b2-104">SYNTAX</span></span>

### <span data-ttu-id="1f4b2-105">Start (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f4b2-105">Start (Default)</span></span>
```
Start-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f4b2-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f4b2-106">StartViaIdentity</span></span>
```
Start-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f4b2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1f4b2-107">DESCRIPTION</span></span>
<span data-ttu-id="1f4b2-108">Kiszolgáló indítása.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-108">Starts a server.</span></span>

## <span data-ttu-id="1f4b2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1f4b2-109">EXAMPLES</span></span>

### <span data-ttu-id="1f4b2-110">1. példa: A kiszolgáló kezdése erőforrásnév alapján</span><span class="sxs-lookup"><span data-stu-id="1f4b2-110">Example 1: Start the server by resource name</span></span>
```powershell
PS C:\> Start-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="1f4b2-111">A kiszolgáló kezdése név alapján</span><span class="sxs-lookup"><span data-stu-id="1f4b2-111">Start the server by name</span></span>

### <span data-ttu-id="1f4b2-112">2. példa: A kiszolgáló elindítani identitás alapján</span><span class="sxs-lookup"><span data-stu-id="1f4b2-112">Example 2: Start the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/start"
PS C:\> Start-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="1f4b2-113">A kiszolgáló elindítani identitás alapján</span><span class="sxs-lookup"><span data-stu-id="1f4b2-113">Start the server by identity</span></span>

## <span data-ttu-id="1f4b2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f4b2-114">PARAMETERS</span></span>

### <span data-ttu-id="1f4b2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f4b2-115">-AsJob</span></span>
<span data-ttu-id="1f4b2-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="1f4b2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1f4b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4b2-117">-DefaultProfile</span></span>
<span data-ttu-id="1f4b2-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f4b2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f4b2-119">-InputObject</span></span>
<span data-ttu-id="1f4b2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4b2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1f4b2-121">-Name</span></span>
<span data-ttu-id="1f4b2-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f4b2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1f4b2-123">-NoWait</span></span>
<span data-ttu-id="1f4b2-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="1f4b2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1f4b2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f4b2-125">-PassThru</span></span>
<span data-ttu-id="1f4b2-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="1f4b2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1f4b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f4b2-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-128">The name of the resource group.</span></span>
<span data-ttu-id="1f4b2-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="1f4b2-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f4b2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f4b2-130">-SubscriptionId</span></span>
<span data-ttu-id="1f4b2-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f4b2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f4b2-132">-Confirm</span></span>
<span data-ttu-id="1f4b2-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f4b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4b2-134">-WhatIf</span></span>
<span data-ttu-id="1f4b2-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f4b2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f4b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4b2-137">CommonParameters</span></span>
<span data-ttu-id="1f4b2-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4b2-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f4b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4b2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f4b2-140">INPUTS</span></span>

### <span data-ttu-id="1f4b2-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1f4b2-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="1f4b2-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f4b2-142">OUTPUTS</span></span>

### <span data-ttu-id="1f4b2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f4b2-143">System.Boolean</span></span>

## <span data-ttu-id="1f4b2-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1f4b2-144">NOTES</span></span>

<span data-ttu-id="1f4b2-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1f4b2-145">ALIASES</span></span>

<span data-ttu-id="1f4b2-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="1f4b2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f4b2-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f4b2-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f4b2-149">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="1f4b2-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f4b2-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1f4b2-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1f4b2-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1f4b2-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1f4b2-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f4b2-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1f4b2-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1f4b2-156">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="1f4b2-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="1f4b2-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1f4b2-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1f4b2-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1f4b2-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="1f4b2-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1f4b2-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f4b2-161">RELATED LINKS</span></span>

