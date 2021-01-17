---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 7e3c3855fb36d1dbc96b399d5348f033ca74908e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467518"
---
# <span data-ttu-id="a3964-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3964-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="a3964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3964-102">SYNOPSIS</span></span>
<span data-ttu-id="a3964-103">A mySQL rugalmas kiszolgáló konfigurációjának információit frissíti.</span><span class="sxs-lookup"><span data-stu-id="a3964-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="a3964-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3964-104">SYNTAX</span></span>

### <span data-ttu-id="a3964-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3964-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3964-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a3964-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3964-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3964-107">DESCRIPTION</span></span>
<span data-ttu-id="a3964-108">A mySQL rugalmas kiszolgáló konfigurációjának információit frissíti.</span><span class="sxs-lookup"><span data-stu-id="a3964-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="a3964-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3964-109">EXAMPLES</span></span>

### <span data-ttu-id="a3964-110">1. példa: A MySql-konfiguráció frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="a3964-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="a3964-111">Ez a parancsmag név szerint frissíti a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a3964-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="a3964-112">2. példa: A MySql konfigurációjának frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="a3964-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="a3964-113">Ezek a parancsmagok identitás szerint frissítik a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a3964-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="a3964-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3964-114">PARAMETERS</span></span>

### <span data-ttu-id="a3964-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3964-115">-AsJob</span></span>
<span data-ttu-id="a3964-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="a3964-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a3964-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3964-117">-DefaultProfile</span></span>
<span data-ttu-id="a3964-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3964-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3964-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3964-119">-InputObject</span></span>
<span data-ttu-id="a3964-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a3964-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3964-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3964-121">-Name</span></span>
<span data-ttu-id="a3964-122">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="a3964-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a3964-123">-NoWait</span></span>
<span data-ttu-id="a3964-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="a3964-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a3964-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3964-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3964-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-126">The name of the resource group.</span></span>
<span data-ttu-id="a3964-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a3964-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a3964-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a3964-128">-ServerName</span></span>
<span data-ttu-id="a3964-129">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-129">The name of the server.</span></span>

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

### <span data-ttu-id="a3964-130">-Source</span><span class="sxs-lookup"><span data-stu-id="a3964-130">-Source</span></span>
<span data-ttu-id="a3964-131">A frissítési érték forrása.</span><span class="sxs-lookup"><span data-stu-id="a3964-131">The source of the updating value.</span></span>
<span data-ttu-id="a3964-132">Az alapértelmezett érték a felhasználói felülbírálás.</span><span class="sxs-lookup"><span data-stu-id="a3964-132">The default value is user-override</span></span>

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

### <span data-ttu-id="a3964-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3964-133">-SubscriptionId</span></span>
<span data-ttu-id="a3964-134">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3964-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a3964-135">-Érték</span><span class="sxs-lookup"><span data-stu-id="a3964-135">-Value</span></span>
<span data-ttu-id="a3964-136">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="a3964-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="a3964-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3964-137">-Confirm</span></span>
<span data-ttu-id="a3964-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a3964-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3964-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3964-139">-WhatIf</span></span>
<span data-ttu-id="a3964-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a3964-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3964-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3964-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3964-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3964-142">CommonParameters</span></span>
<span data-ttu-id="a3964-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3964-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3964-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3964-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3964-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3964-145">INPUTS</span></span>

### <span data-ttu-id="a3964-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a3964-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a3964-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3964-147">OUTPUTS</span></span>

### <span data-ttu-id="a3964-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a3964-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="a3964-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3964-149">NOTES</span></span>

<span data-ttu-id="a3964-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a3964-150">ALIASES</span></span>

<span data-ttu-id="a3964-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a3964-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3964-152">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a3964-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3964-153">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3964-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3964-154">INPUTOBJECT: <IMySqlIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a3964-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3964-155">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a3964-156">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a3964-157">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a3964-158">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a3964-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3964-159">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a3964-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a3964-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a3964-162">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a3964-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="a3964-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a3964-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a3964-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3964-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a3964-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="a3964-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a3964-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3964-167">RELATED LINKS</span></span>

