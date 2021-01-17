---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
ms.openlocfilehash: 6b0544bb2394b4d69c496ec4f2502360ddf173bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467271"
---
# <span data-ttu-id="63f0d-101">Remove-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="63f0d-101">Remove-AzPostgreSqlServer</span></span>

## <span data-ttu-id="63f0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="63f0d-103">Töröl egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="63f0d-103">Deletes a server.</span></span>

## <span data-ttu-id="63f0d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63f0d-104">SYNTAX</span></span>

### <span data-ttu-id="63f0d-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63f0d-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="63f0d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="63f0d-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="63f0d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63f0d-107">DESCRIPTION</span></span>
<span data-ttu-id="63f0d-108">Töröl egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="63f0d-108">Deletes a server.</span></span>

## <span data-ttu-id="63f0d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63f0d-109">EXAMPLES</span></span>

### <span data-ttu-id="63f0d-110">1. példa: A PostgreSql-kiszolgáló eltávolítása az resourceGroup és a kiszolgáló neve alapján</span><span class="sxs-lookup"><span data-stu-id="63f0d-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="63f0d-111">Ez a parancsmag eltávolítja a PostgreSql-kiszolgálót az resourceGroup és a kiszolgáló neve alapján.</span><span class="sxs-lookup"><span data-stu-id="63f0d-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="63f0d-112">2. példa: A PostgreSql-kiszolgáló eltávolítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="63f0d-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer"
PS C:\> Remove-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="63f0d-113">Ezek a parancsmagok identitás szerint eltávolítják a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="63f0d-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="63f0d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63f0d-114">PARAMETERS</span></span>

### <span data-ttu-id="63f0d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63f0d-115">-AsJob</span></span>
<span data-ttu-id="63f0d-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="63f0d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="63f0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f0d-117">-DefaultProfile</span></span>
<span data-ttu-id="63f0d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63f0d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f0d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63f0d-119">-InputObject</span></span>
<span data-ttu-id="63f0d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="63f0d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f0d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="63f0d-121">-Name</span></span>
<span data-ttu-id="63f0d-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-122">The name of the server.</span></span>

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

### <span data-ttu-id="63f0d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="63f0d-123">-NoWait</span></span>
<span data-ttu-id="63f0d-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="63f0d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="63f0d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63f0d-125">-PassThru</span></span>
<span data-ttu-id="63f0d-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="63f0d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="63f0d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f0d-127">-ResourceGroupName</span></span>
<span data-ttu-id="63f0d-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-128">The name of the resource group.</span></span>
<span data-ttu-id="63f0d-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="63f0d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="63f0d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63f0d-130">-SubscriptionId</span></span>
<span data-ttu-id="63f0d-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="63f0d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="63f0d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63f0d-132">-Confirm</span></span>
<span data-ttu-id="63f0d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="63f0d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f0d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f0d-134">-WhatIf</span></span>
<span data-ttu-id="63f0d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="63f0d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f0d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63f0d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f0d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f0d-137">CommonParameters</span></span>
<span data-ttu-id="63f0d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f0d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f0d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63f0d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f0d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63f0d-140">INPUTS</span></span>

### <span data-ttu-id="63f0d-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="63f0d-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="63f0d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63f0d-142">OUTPUTS</span></span>

### <span data-ttu-id="63f0d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63f0d-143">System.Boolean</span></span>

## <span data-ttu-id="63f0d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63f0d-144">NOTES</span></span>

<span data-ttu-id="63f0d-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="63f0d-145">ALIASES</span></span>

<span data-ttu-id="63f0d-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="63f0d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="63f0d-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="63f0d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="63f0d-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="63f0d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="63f0d-149">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="63f0d-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="63f0d-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="63f0d-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="63f0d-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="63f0d-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="63f0d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="63f0d-154">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="63f0d-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="63f0d-156">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="63f0d-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="63f0d-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="63f0d-158">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="63f0d-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="63f0d-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="63f0d-160">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="63f0d-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="63f0d-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63f0d-161">RELATED LINKS</span></span>

