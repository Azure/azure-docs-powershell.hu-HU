---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: bff7f24ef88c8f6fc5022aae019a9c6f32bf95f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927017"
---
# <span data-ttu-id="235c1-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="235c1-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="235c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="235c1-102">SYNOPSIS</span></span>
<span data-ttu-id="235c1-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="235c1-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="235c1-104">Használja Update-AzMySqlServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="235c1-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="235c1-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="235c1-105">SYNTAX</span></span>

### <span data-ttu-id="235c1-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="235c1-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="235c1-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="235c1-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="235c1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="235c1-108">DESCRIPTION</span></span>
<span data-ttu-id="235c1-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="235c1-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="235c1-110">Használja Update-AzMySqlServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="235c1-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="235c1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="235c1-111">EXAMPLES</span></span>

### <span data-ttu-id="235c1-112">1. példa: A MySql-konfiguráció frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="235c1-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="235c1-113">Ez a parancsmag név szerint frissíti a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="235c1-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="235c1-114">2. példa: A MySql konfigurációjának frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="235c1-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="235c1-115">Ezek a parancsmagok identitás szerint frissítik a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="235c1-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="235c1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="235c1-116">PARAMETERS</span></span>

### <span data-ttu-id="235c1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="235c1-117">-AsJob</span></span>
<span data-ttu-id="235c1-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="235c1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="235c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235c1-119">-DefaultProfile</span></span>
<span data-ttu-id="235c1-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="235c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="235c1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="235c1-121">-InputObject</span></span>
<span data-ttu-id="235c1-122">Identitás paramétere.</span><span class="sxs-lookup"><span data-stu-id="235c1-122">Identity Parameter.</span></span>
<span data-ttu-id="235c1-123">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="235c1-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="235c1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="235c1-124">-Name</span></span>
<span data-ttu-id="235c1-125">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="235c1-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="235c1-126">-NoWait</span></span>
<span data-ttu-id="235c1-127">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="235c1-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="235c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="235c1-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-129">The name of the resource group.</span></span>
<span data-ttu-id="235c1-130">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="235c1-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="235c1-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="235c1-131">-ServerName</span></span>
<span data-ttu-id="235c1-132">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-132">The name of the server.</span></span>

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

### <span data-ttu-id="235c1-133">-Source</span><span class="sxs-lookup"><span data-stu-id="235c1-133">-Source</span></span>
<span data-ttu-id="235c1-134">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="235c1-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="235c1-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="235c1-135">-SubscriptionId</span></span>
<span data-ttu-id="235c1-136">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="235c1-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="235c1-137">-Érték</span><span class="sxs-lookup"><span data-stu-id="235c1-137">-Value</span></span>
<span data-ttu-id="235c1-138">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="235c1-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="235c1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="235c1-139">-Confirm</span></span>
<span data-ttu-id="235c1-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="235c1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="235c1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235c1-141">-WhatIf</span></span>
<span data-ttu-id="235c1-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="235c1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="235c1-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="235c1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="235c1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235c1-144">CommonParameters</span></span>
<span data-ttu-id="235c1-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="235c1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235c1-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="235c1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235c1-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="235c1-147">INPUTS</span></span>

### <span data-ttu-id="235c1-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="235c1-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="235c1-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="235c1-149">OUTPUTS</span></span>

### <span data-ttu-id="235c1-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="235c1-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="235c1-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="235c1-151">NOTES</span></span>

<span data-ttu-id="235c1-152">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="235c1-152">ALIASES</span></span>

<span data-ttu-id="235c1-153">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="235c1-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="235c1-154">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="235c1-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="235c1-155">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="235c1-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="235c1-156">INPUTOBJECT: <IMySqlIdentity> Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="235c1-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="235c1-157">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="235c1-158">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="235c1-159">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="235c1-160">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="235c1-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="235c1-161">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="235c1-162">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="235c1-163">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="235c1-164">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="235c1-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="235c1-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="235c1-166">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="235c1-167">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="235c1-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="235c1-168">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="235c1-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="235c1-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="235c1-169">RELATED LINKS</span></span>

