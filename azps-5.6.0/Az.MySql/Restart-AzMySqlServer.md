---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restart-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
ms.openlocfilehash: 3dfdf0129e8324220b20872964b68f324cb53cf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003733"
---
# <span data-ttu-id="33743-101">Restart-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="33743-101">Restart-AzMySqlServer</span></span>

## <span data-ttu-id="33743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33743-102">SYNOPSIS</span></span>
<span data-ttu-id="33743-103">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="33743-103">Restarts a server.</span></span>

## <span data-ttu-id="33743-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33743-104">SYNTAX</span></span>

### <span data-ttu-id="33743-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33743-105">Restart (Default)</span></span>
```
Restart-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="33743-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="33743-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33743-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33743-107">DESCRIPTION</span></span>
<span data-ttu-id="33743-108">Újraindít egy kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="33743-108">Restarts a server.</span></span>

## <span data-ttu-id="33743-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33743-109">EXAMPLES</span></span>

### <span data-ttu-id="33743-110">1. példa: A MySql-kiszolgáló újraindítása erőforráscsoport és kiszolgálónév alapján</span><span class="sxs-lookup"><span data-stu-id="33743-110">Example 1: Restart MySql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="33743-111">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint újraindítja a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="33743-111">This cmdlet restarts MySql server by resource group and server name.</span></span>

### <span data-ttu-id="33743-112">2. példa: A MySql-kiszolgáló újraindítása identitás alapján</span><span class="sxs-lookup"><span data-stu-id="33743-112">Example 2: Restart MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/restart"
PS C:\> Restart-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="33743-113">Ezek a parancsmagok identitás alapján indítják újra a MySql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="33743-113">These cmdlets restart MySql server by identity.</span></span>

## <span data-ttu-id="33743-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33743-114">PARAMETERS</span></span>

### <span data-ttu-id="33743-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33743-115">-AsJob</span></span>
<span data-ttu-id="33743-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="33743-116">Run the command as a job</span></span>

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

### <span data-ttu-id="33743-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33743-117">-DefaultProfile</span></span>
<span data-ttu-id="33743-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33743-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33743-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33743-119">-InputObject</span></span>
<span data-ttu-id="33743-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="33743-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="33743-121">-Name</span><span class="sxs-lookup"><span data-stu-id="33743-121">-Name</span></span>
<span data-ttu-id="33743-122">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="33743-122">The name of the server.</span></span>

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

### <span data-ttu-id="33743-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="33743-123">-NoWait</span></span>
<span data-ttu-id="33743-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="33743-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="33743-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33743-125">-PassThru</span></span>
<span data-ttu-id="33743-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="33743-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="33743-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33743-127">-ResourceGroupName</span></span>
<span data-ttu-id="33743-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="33743-128">The name of the resource group.</span></span>
<span data-ttu-id="33743-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="33743-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="33743-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33743-130">-SubscriptionId</span></span>
<span data-ttu-id="33743-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="33743-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="33743-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33743-132">-Confirm</span></span>
<span data-ttu-id="33743-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="33743-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33743-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33743-134">-WhatIf</span></span>
<span data-ttu-id="33743-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="33743-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33743-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33743-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33743-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33743-137">CommonParameters</span></span>
<span data-ttu-id="33743-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33743-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33743-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33743-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33743-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33743-140">INPUTS</span></span>

### <span data-ttu-id="33743-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="33743-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="33743-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33743-142">OUTPUTS</span></span>

### <span data-ttu-id="33743-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33743-143">System.Boolean</span></span>

## <span data-ttu-id="33743-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33743-144">NOTES</span></span>

<span data-ttu-id="33743-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="33743-145">ALIASES</span></span>

<span data-ttu-id="33743-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="33743-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33743-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="33743-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33743-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33743-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33743-149">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="33743-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33743-150">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="33743-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="33743-151">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="33743-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="33743-152">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="33743-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="33743-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="33743-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33743-154">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="33743-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="33743-155">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="33743-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="33743-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="33743-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="33743-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="33743-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="33743-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="33743-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="33743-159">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="33743-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="33743-160">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="33743-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="33743-161">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="33743-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="33743-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33743-162">RELATED LINKS</span></span>

