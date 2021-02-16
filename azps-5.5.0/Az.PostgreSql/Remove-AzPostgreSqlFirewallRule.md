---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160346"
---
# <span data-ttu-id="87b40-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87b40-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="87b40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b40-102">SYNOPSIS</span></span>
<span data-ttu-id="87b40-103">Törli a kiszolgáló tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="87b40-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="87b40-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87b40-104">SYNTAX</span></span>

### <span data-ttu-id="87b40-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87b40-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="87b40-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="87b40-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87b40-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87b40-107">DESCRIPTION</span></span>
<span data-ttu-id="87b40-108">Törli a kiszolgáló tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="87b40-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="87b40-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87b40-109">EXAMPLES</span></span>

### <span data-ttu-id="87b40-110">1. példa: A PostgreSql tűzfalszabály eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="87b40-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="87b40-111">Ez a parancsmag név szerint eltávolítja a PostgreSql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="87b40-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="87b40-112">2. példa: A PostgreSql tűzfalszabály eltávolítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="87b40-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="87b40-113">Ezek a parancsmagok identitás szerint eltávolítják a PostgreSql tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="87b40-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="87b40-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87b40-114">PARAMETERS</span></span>

### <span data-ttu-id="87b40-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87b40-115">-AsJob</span></span>
<span data-ttu-id="87b40-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="87b40-116">Run the command as a job</span></span>

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

### <span data-ttu-id="87b40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b40-117">-DefaultProfile</span></span>
<span data-ttu-id="87b40-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87b40-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87b40-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87b40-119">-InputObject</span></span>
<span data-ttu-id="87b40-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="87b40-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="87b40-121">-Name</span><span class="sxs-lookup"><span data-stu-id="87b40-121">-Name</span></span>
<span data-ttu-id="87b40-122">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="87b40-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="87b40-123">-NoWait</span></span>
<span data-ttu-id="87b40-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="87b40-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="87b40-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87b40-125">-PassThru</span></span>
<span data-ttu-id="87b40-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="87b40-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="87b40-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b40-127">-ResourceGroupName</span></span>
<span data-ttu-id="87b40-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-128">The name of the resource group.</span></span>
<span data-ttu-id="87b40-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="87b40-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="87b40-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="87b40-130">-ServerName</span></span>
<span data-ttu-id="87b40-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-131">The name of the server.</span></span>

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

### <span data-ttu-id="87b40-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87b40-132">-SubscriptionId</span></span>
<span data-ttu-id="87b40-133">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87b40-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="87b40-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87b40-134">-Confirm</span></span>
<span data-ttu-id="87b40-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="87b40-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87b40-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b40-136">-WhatIf</span></span>
<span data-ttu-id="87b40-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="87b40-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b40-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87b40-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87b40-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b40-139">CommonParameters</span></span>
<span data-ttu-id="87b40-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b40-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b40-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87b40-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b40-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87b40-142">INPUTS</span></span>

### <span data-ttu-id="87b40-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="87b40-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="87b40-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87b40-144">OUTPUTS</span></span>

### <span data-ttu-id="87b40-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="87b40-145">System.Boolean</span></span>

## <span data-ttu-id="87b40-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87b40-146">NOTES</span></span>

<span data-ttu-id="87b40-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="87b40-147">ALIASES</span></span>

<span data-ttu-id="87b40-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="87b40-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87b40-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="87b40-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87b40-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87b40-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87b40-151">INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="87b40-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87b40-152">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="87b40-153">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="87b40-154">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="87b40-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="87b40-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87b40-156">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="87b40-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="87b40-158">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="87b40-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="87b40-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="87b40-160">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="87b40-161">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87b40-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="87b40-162">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="87b40-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="87b40-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87b40-163">RELATED LINKS</span></span>

