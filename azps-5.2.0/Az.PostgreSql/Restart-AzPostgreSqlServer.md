---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331170"
---
# <span data-ttu-id="6aae8-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="6aae8-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="6aae8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aae8-102">SYNOPSIS</span></span>
<span data-ttu-id="6aae8-103">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6aae8-103">Restarts a server.</span></span>

## <span data-ttu-id="6aae8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6aae8-104">SYNTAX</span></span>

### <span data-ttu-id="6aae8-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6aae8-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6aae8-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6aae8-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6aae8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6aae8-107">DESCRIPTION</span></span>
<span data-ttu-id="6aae8-108">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6aae8-108">Restarts a server.</span></span>

## <span data-ttu-id="6aae8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6aae8-109">EXAMPLES</span></span>

### <span data-ttu-id="6aae8-110">1. példa: A PostgreSql-kiszolgáló újraindítása erőforráscsoport és kiszolgálónév alapján</span><span class="sxs-lookup"><span data-stu-id="6aae8-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="6aae8-111">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint újraindítja a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6aae8-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="6aae8-112">2. példa: A PostgreSql-kiszolgáló újraindítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="6aae8-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="6aae8-113">Ezek a parancsmagok identitás szerint indítják újra a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6aae8-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="6aae8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6aae8-114">PARAMETERS</span></span>

### <span data-ttu-id="6aae8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6aae8-115">-AsJob</span></span>
<span data-ttu-id="6aae8-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="6aae8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6aae8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aae8-117">-DefaultProfile</span></span>
<span data-ttu-id="6aae8-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6aae8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aae8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6aae8-119">-InputObject</span></span>
<span data-ttu-id="6aae8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6aae8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6aae8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6aae8-121">-Name</span></span>
<span data-ttu-id="6aae8-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-122">The name of the server.</span></span>

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

### <span data-ttu-id="6aae8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6aae8-123">-NoWait</span></span>
<span data-ttu-id="6aae8-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="6aae8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6aae8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6aae8-125">-PassThru</span></span>
<span data-ttu-id="6aae8-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="6aae8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6aae8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aae8-127">-ResourceGroupName</span></span>
<span data-ttu-id="6aae8-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-128">The name of the resource group.</span></span>
<span data-ttu-id="6aae8-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6aae8-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6aae8-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6aae8-130">-SubscriptionId</span></span>
<span data-ttu-id="6aae8-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6aae8-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6aae8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aae8-132">-Confirm</span></span>
<span data-ttu-id="6aae8-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6aae8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aae8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aae8-134">-WhatIf</span></span>
<span data-ttu-id="6aae8-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6aae8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aae8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6aae8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aae8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aae8-137">CommonParameters</span></span>
<span data-ttu-id="6aae8-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aae8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aae8-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6aae8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aae8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6aae8-140">INPUTS</span></span>

### <span data-ttu-id="6aae8-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6aae8-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6aae8-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6aae8-142">OUTPUTS</span></span>

### <span data-ttu-id="6aae8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6aae8-143">System.Boolean</span></span>

## <span data-ttu-id="6aae8-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6aae8-144">NOTES</span></span>

<span data-ttu-id="6aae8-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6aae8-145">ALIASES</span></span>

<span data-ttu-id="6aae8-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6aae8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6aae8-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6aae8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6aae8-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6aae8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6aae8-149">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6aae8-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6aae8-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6aae8-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6aae8-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6aae8-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6aae8-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6aae8-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6aae8-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6aae8-156">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6aae8-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="6aae8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6aae8-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6aae8-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6aae8-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6aae8-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6aae8-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6aae8-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6aae8-161">RELATED LINKS</span></span>

