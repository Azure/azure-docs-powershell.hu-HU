---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 98e476b2a1732d2c984d200265d817c3ff6d71a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927009"
---
# <span data-ttu-id="05fe0-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="05fe0-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="05fe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="05fe0-103">A mySQL rugalmas kiszolgáló konfigurációjának információit frissíti.</span><span class="sxs-lookup"><span data-stu-id="05fe0-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="05fe0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05fe0-104">SYNTAX</span></span>

### <span data-ttu-id="05fe0-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05fe0-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05fe0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="05fe0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05fe0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05fe0-107">DESCRIPTION</span></span>
<span data-ttu-id="05fe0-108">A mySQL rugalmas kiszolgáló konfigurációjának információit frissíti.</span><span class="sxs-lookup"><span data-stu-id="05fe0-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="05fe0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05fe0-109">EXAMPLES</span></span>

### <span data-ttu-id="05fe0-110">1. példa: A MySql-konfiguráció frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="05fe0-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="05fe0-111">Ez a parancsmag név szerint frissíti a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="05fe0-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="05fe0-112">2. példa: A MySql konfigurációjának frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="05fe0-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="05fe0-113">Ezek a parancsmagok identitás szerint frissítik a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="05fe0-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="05fe0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05fe0-114">PARAMETERS</span></span>

### <span data-ttu-id="05fe0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05fe0-115">-AsJob</span></span>
<span data-ttu-id="05fe0-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="05fe0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="05fe0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05fe0-117">-DefaultProfile</span></span>
<span data-ttu-id="05fe0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05fe0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05fe0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05fe0-119">-InputObject</span></span>
<span data-ttu-id="05fe0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="05fe0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05fe0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="05fe0-121">-Name</span></span>
<span data-ttu-id="05fe0-122">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-122">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05fe0-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="05fe0-123">-NoWait</span></span>
<span data-ttu-id="05fe0-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="05fe0-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="05fe0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05fe0-125">-ResourceGroupName</span></span>
<span data-ttu-id="05fe0-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-126">The name of the resource group.</span></span>
<span data-ttu-id="05fe0-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="05fe0-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05fe0-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05fe0-128">-ServerName</span></span>
<span data-ttu-id="05fe0-129">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05fe0-130">-Source</span><span class="sxs-lookup"><span data-stu-id="05fe0-130">-Source</span></span>
<span data-ttu-id="05fe0-131">A frissítési érték forrása.</span><span class="sxs-lookup"><span data-stu-id="05fe0-131">The source of the updating value.</span></span>
<span data-ttu-id="05fe0-132">Az alapértelmezett érték a felhasználói felülbírálás.</span><span class="sxs-lookup"><span data-stu-id="05fe0-132">The default value is user-override</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05fe0-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05fe0-133">-SubscriptionId</span></span>
<span data-ttu-id="05fe0-134">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="05fe0-134">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05fe0-135">-Érték</span><span class="sxs-lookup"><span data-stu-id="05fe0-135">-Value</span></span>
<span data-ttu-id="05fe0-136">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="05fe0-136">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05fe0-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05fe0-137">-Confirm</span></span>
<span data-ttu-id="05fe0-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="05fe0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05fe0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05fe0-139">-WhatIf</span></span>
<span data-ttu-id="05fe0-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="05fe0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05fe0-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05fe0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05fe0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05fe0-142">CommonParameters</span></span>
<span data-ttu-id="05fe0-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05fe0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05fe0-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05fe0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05fe0-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05fe0-145">INPUTS</span></span>

### <span data-ttu-id="05fe0-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="05fe0-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="05fe0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05fe0-147">OUTPUTS</span></span>

### <span data-ttu-id="05fe0-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="05fe0-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="05fe0-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05fe0-149">NOTES</span></span>

<span data-ttu-id="05fe0-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="05fe0-150">ALIASES</span></span>

<span data-ttu-id="05fe0-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="05fe0-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05fe0-152">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="05fe0-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05fe0-153">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05fe0-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05fe0-154">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="05fe0-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05fe0-155">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="05fe0-156">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="05fe0-157">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="05fe0-158">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="05fe0-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05fe0-159">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="05fe0-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="05fe0-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="05fe0-162">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="05fe0-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="05fe0-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="05fe0-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="05fe0-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="05fe0-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="05fe0-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="05fe0-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="05fe0-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05fe0-167">RELATED LINKS</span></span>

