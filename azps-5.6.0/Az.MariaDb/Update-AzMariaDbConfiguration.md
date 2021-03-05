---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: dc2a36a9ac8c2595ef2f60b8edc40582ad864ff8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003893"
---
# <span data-ttu-id="35ca6-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="35ca6-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="35ca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="35ca6-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="35ca6-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="35ca6-104">Használja Update-AzMariaDbServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="35ca6-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="35ca6-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35ca6-105">SYNTAX</span></span>

### <span data-ttu-id="35ca6-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35ca6-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35ca6-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="35ca6-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35ca6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="35ca6-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="35ca6-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="35ca6-110">Használja Update-AzMariaDberver, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="35ca6-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="35ca6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35ca6-111">EXAMPLES</span></span>

### <span data-ttu-id="35ca6-112">1. példa: A MariaDB-konfiguráció frissítése</span><span class="sxs-lookup"><span data-stu-id="35ca6-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="35ca6-113">Ez a parancs frissíti a MariaDB konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="35ca6-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="35ca6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35ca6-114">PARAMETERS</span></span>

### <span data-ttu-id="35ca6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35ca6-115">-AsJob</span></span>
<span data-ttu-id="35ca6-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="35ca6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="35ca6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ca6-117">-DefaultProfile</span></span>
<span data-ttu-id="35ca6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35ca6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ca6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35ca6-119">-InputObject</span></span>
<span data-ttu-id="35ca6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="35ca6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35ca6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="35ca6-121">-Name</span></span>
<span data-ttu-id="35ca6-122">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="35ca6-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="35ca6-123">-NoWait</span></span>
<span data-ttu-id="35ca6-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="35ca6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35ca6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ca6-125">-ResourceGroupName</span></span>
<span data-ttu-id="35ca6-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="35ca6-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="35ca6-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="35ca6-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="35ca6-128">-ServerName</span></span>
<span data-ttu-id="35ca6-129">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-129">The name of the server.</span></span>

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

### <span data-ttu-id="35ca6-130">-Source</span><span class="sxs-lookup"><span data-stu-id="35ca6-130">-Source</span></span>
<span data-ttu-id="35ca6-131">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="35ca6-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="35ca6-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35ca6-132">-SubscriptionId</span></span>
<span data-ttu-id="35ca6-133">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="35ca6-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="35ca6-134">-Érték</span><span class="sxs-lookup"><span data-stu-id="35ca6-134">-Value</span></span>
<span data-ttu-id="35ca6-135">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="35ca6-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="35ca6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35ca6-136">-Confirm</span></span>
<span data-ttu-id="35ca6-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="35ca6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ca6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ca6-138">-WhatIf</span></span>
<span data-ttu-id="35ca6-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="35ca6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ca6-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35ca6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ca6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ca6-141">CommonParameters</span></span>
<span data-ttu-id="35ca6-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ca6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ca6-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35ca6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ca6-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35ca6-144">INPUTS</span></span>

### <span data-ttu-id="35ca6-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="35ca6-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="35ca6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35ca6-146">OUTPUTS</span></span>

### <span data-ttu-id="35ca6-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="35ca6-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="35ca6-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35ca6-148">NOTES</span></span>

<span data-ttu-id="35ca6-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="35ca6-149">ALIASES</span></span>

<span data-ttu-id="35ca6-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="35ca6-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35ca6-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="35ca6-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35ca6-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35ca6-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35ca6-153">INPUTOBJECT: <IMariaDbIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="35ca6-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35ca6-154">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="35ca6-155">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="35ca6-156">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="35ca6-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="35ca6-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35ca6-158">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="35ca6-159">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="35ca6-160">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="35ca6-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="35ca6-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="35ca6-162">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="35ca6-163">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="35ca6-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="35ca6-164">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="35ca6-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="35ca6-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35ca6-165">RELATED LINKS</span></span>

