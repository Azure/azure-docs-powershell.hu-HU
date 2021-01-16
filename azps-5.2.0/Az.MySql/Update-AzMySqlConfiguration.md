---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360260"
---
# <span data-ttu-id="c7812-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7812-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="c7812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7812-102">SYNOPSIS</span></span>
<span data-ttu-id="c7812-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c7812-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="c7812-104">Használja Update-AzMySqlServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="c7812-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="c7812-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7812-105">SYNTAX</span></span>

### <span data-ttu-id="c7812-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7812-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7812-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c7812-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7812-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7812-108">DESCRIPTION</span></span>
<span data-ttu-id="c7812-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c7812-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="c7812-110">Használja Update-AzMySqlServer, ha frissíteni szeretné a AdministratorLoginPassword, a termékváltozat stb. frissítést.</span><span class="sxs-lookup"><span data-stu-id="c7812-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="c7812-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7812-111">EXAMPLES</span></span>

### <span data-ttu-id="c7812-112">1. példa: A MySql-konfiguráció frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="c7812-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="c7812-113">Ez a parancsmag név szerint frissíti a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="c7812-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="c7812-114">2. példa: A MySql konfigurációjának frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="c7812-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="c7812-115">Ezek a parancsmagok identitás szerint frissítik a MySql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="c7812-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="c7812-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7812-116">PARAMETERS</span></span>

### <span data-ttu-id="c7812-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7812-117">-AsJob</span></span>
<span data-ttu-id="c7812-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="c7812-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c7812-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7812-119">-DefaultProfile</span></span>
<span data-ttu-id="c7812-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7812-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7812-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7812-121">-InputObject</span></span>
<span data-ttu-id="c7812-122">Identitás paramétere.</span><span class="sxs-lookup"><span data-stu-id="c7812-122">Identity Parameter.</span></span>
<span data-ttu-id="c7812-123">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="c7812-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c7812-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c7812-124">-Name</span></span>
<span data-ttu-id="c7812-125">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="c7812-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c7812-126">-NoWait</span></span>
<span data-ttu-id="c7812-127">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="c7812-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c7812-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7812-128">-ResourceGroupName</span></span>
<span data-ttu-id="c7812-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-129">The name of the resource group.</span></span>
<span data-ttu-id="c7812-130">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c7812-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c7812-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c7812-131">-ServerName</span></span>
<span data-ttu-id="c7812-132">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-132">The name of the server.</span></span>

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

### <span data-ttu-id="c7812-133">-Source</span><span class="sxs-lookup"><span data-stu-id="c7812-133">-Source</span></span>
<span data-ttu-id="c7812-134">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="c7812-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="c7812-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7812-135">-SubscriptionId</span></span>
<span data-ttu-id="c7812-136">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7812-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c7812-137">-Érték</span><span class="sxs-lookup"><span data-stu-id="c7812-137">-Value</span></span>
<span data-ttu-id="c7812-138">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="c7812-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="c7812-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7812-139">-Confirm</span></span>
<span data-ttu-id="c7812-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c7812-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7812-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7812-141">-WhatIf</span></span>
<span data-ttu-id="c7812-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c7812-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7812-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7812-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7812-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7812-144">CommonParameters</span></span>
<span data-ttu-id="c7812-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7812-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7812-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7812-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7812-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7812-147">INPUTS</span></span>

### <span data-ttu-id="c7812-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c7812-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c7812-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7812-149">OUTPUTS</span></span>

### <span data-ttu-id="c7812-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7812-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="c7812-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7812-151">NOTES</span></span>

<span data-ttu-id="c7812-152">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c7812-152">ALIASES</span></span>

<span data-ttu-id="c7812-153">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c7812-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7812-154">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c7812-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7812-155">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7812-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7812-156">INPUTOBJECT: <IMySqlIdentity> Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="c7812-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="c7812-157">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c7812-158">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c7812-159">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c7812-160">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c7812-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7812-161">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c7812-162">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c7812-163">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c7812-164">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c7812-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="c7812-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c7812-166">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c7812-167">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7812-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c7812-168">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="c7812-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c7812-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7812-169">RELATED LINKS</span></span>

