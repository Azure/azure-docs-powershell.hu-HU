---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194109"
---
# <span data-ttu-id="0a89a-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a89a-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="0a89a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a89a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a89a-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0a89a-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="0a89a-104">Ha a AdministratorLoginPassword, az SKU-ot stb. Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="0a89a-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="0a89a-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a89a-105">SYNTAX</span></span>

### <span data-ttu-id="0a89a-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a89a-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0a89a-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0a89a-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a89a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a89a-108">DESCRIPTION</span></span>
<span data-ttu-id="0a89a-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0a89a-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="0a89a-110">Ha a AdministratorLoginPassword, az SKU-ot stb. Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="0a89a-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="0a89a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0a89a-111">EXAMPLES</span></span>

### <span data-ttu-id="0a89a-112">1. példa: a MySql-konfiguráció frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="0a89a-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="0a89a-113">Ez a parancsmag a MySql konfigurációját név szerint frissíti.</span><span class="sxs-lookup"><span data-stu-id="0a89a-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="0a89a-114">2. példa: a MySql-konfiguráció frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="0a89a-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="0a89a-115">Ezek a parancsmagok identitással frissítik a MySql konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0a89a-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="0a89a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a89a-116">PARAMETERS</span></span>

### <span data-ttu-id="0a89a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a89a-117">-AsJob</span></span>
<span data-ttu-id="0a89a-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="0a89a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0a89a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a89a-119">-DefaultProfile</span></span>
<span data-ttu-id="0a89a-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a89a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a89a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a89a-121">-InputObject</span></span>
<span data-ttu-id="0a89a-122">Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="0a89a-122">Identity Parameter.</span></span>
<span data-ttu-id="0a89a-123">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0a89a-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0a89a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a89a-124">-Name</span></span>
<span data-ttu-id="0a89a-125">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="0a89a-126">-Várva</span><span class="sxs-lookup"><span data-stu-id="0a89a-126">-NoWait</span></span>
<span data-ttu-id="0a89a-127">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="0a89a-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a89a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a89a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0a89a-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-129">The name of the resource group.</span></span>
<span data-ttu-id="0a89a-130">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="0a89a-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0a89a-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0a89a-131">-ServerName</span></span>
<span data-ttu-id="0a89a-132">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-132">The name of the server.</span></span>

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

### <span data-ttu-id="0a89a-133">-Forrás</span><span class="sxs-lookup"><span data-stu-id="0a89a-133">-Source</span></span>
<span data-ttu-id="0a89a-134">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="0a89a-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="0a89a-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a89a-135">-SubscriptionId</span></span>
<span data-ttu-id="0a89a-136">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0a89a-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0a89a-137">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="0a89a-137">-Value</span></span>
<span data-ttu-id="0a89a-138">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="0a89a-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="0a89a-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a89a-139">-Confirm</span></span>
<span data-ttu-id="0a89a-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a89a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a89a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a89a-141">-WhatIf</span></span>
<span data-ttu-id="0a89a-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a89a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a89a-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a89a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a89a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a89a-144">CommonParameters</span></span>
<span data-ttu-id="0a89a-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a89a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a89a-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0a89a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a89a-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a89a-147">INPUTS</span></span>

### <span data-ttu-id="0a89a-148">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0a89a-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0a89a-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a89a-149">OUTPUTS</span></span>

### <span data-ttu-id="0a89a-150">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a89a-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="0a89a-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a89a-151">NOTES</span></span>

<span data-ttu-id="0a89a-152">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0a89a-152">ALIASES</span></span>

<span data-ttu-id="0a89a-153">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="0a89a-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a89a-154">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0a89a-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a89a-155">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="0a89a-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a89a-156">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="0a89a-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="0a89a-157">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0a89a-158">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0a89a-159">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0a89a-160">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0a89a-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a89a-161">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0a89a-162">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0a89a-163">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="0a89a-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="0a89a-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0a89a-165">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0a89a-166">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0a89a-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0a89a-167">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0a89a-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0a89a-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a89a-168">RELATED LINKS</span></span>

