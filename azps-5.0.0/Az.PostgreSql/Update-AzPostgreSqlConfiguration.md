---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194891"
---
# <span data-ttu-id="3f3da-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f3da-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="3f3da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f3da-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3da-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="3f3da-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="3f3da-104">Ha a AdministratorLoginPassword, az SKU-ot stb. Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="3f3da-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="3f3da-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f3da-105">SYNTAX</span></span>

### <span data-ttu-id="3f3da-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f3da-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f3da-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3f3da-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f3da-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f3da-108">DESCRIPTION</span></span>
<span data-ttu-id="3f3da-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="3f3da-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="3f3da-110">Ha a AdministratorLoginPassword, az SKU-ot stb. Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="3f3da-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="3f3da-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3f3da-111">EXAMPLES</span></span>

### <span data-ttu-id="3f3da-112">1. példa: a PostgreSql-konfiguráció frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="3f3da-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="3f3da-113">Ez a parancsmag frissíti a PostgreSql-konfigurációt név szerint.</span><span class="sxs-lookup"><span data-stu-id="3f3da-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="3f3da-114">2. példa: a PostgreSql-konfiguráció frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="3f3da-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="3f3da-115">Ezek a parancsmagok identitással frissítik a PostgreSql-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="3f3da-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="3f3da-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f3da-116">PARAMETERS</span></span>

### <span data-ttu-id="3f3da-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f3da-117">-AsJob</span></span>
<span data-ttu-id="3f3da-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="3f3da-118">Run the command as a job</span></span>

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

### <span data-ttu-id="3f3da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3da-119">-DefaultProfile</span></span>
<span data-ttu-id="3f3da-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f3da-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f3da-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f3da-121">-InputObject</span></span>
<span data-ttu-id="3f3da-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3f3da-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f3da-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f3da-123">-Name</span></span>
<span data-ttu-id="3f3da-124">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="3f3da-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="3f3da-125">-NoWait</span></span>
<span data-ttu-id="3f3da-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="3f3da-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f3da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f3da-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f3da-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-128">The name of the resource group.</span></span>
<span data-ttu-id="3f3da-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="3f3da-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3f3da-130">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3f3da-130">-ServerName</span></span>
<span data-ttu-id="3f3da-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-131">The name of the server.</span></span>

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

### <span data-ttu-id="3f3da-132">-Forrás</span><span class="sxs-lookup"><span data-stu-id="3f3da-132">-Source</span></span>
<span data-ttu-id="3f3da-133">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="3f3da-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="3f3da-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f3da-134">-SubscriptionId</span></span>
<span data-ttu-id="3f3da-135">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3f3da-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3f3da-136">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="3f3da-136">-Value</span></span>
<span data-ttu-id="3f3da-137">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="3f3da-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="3f3da-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f3da-138">-Confirm</span></span>
<span data-ttu-id="3f3da-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f3da-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f3da-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f3da-140">-WhatIf</span></span>
<span data-ttu-id="3f3da-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f3da-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f3da-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f3da-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f3da-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3da-143">CommonParameters</span></span>
<span data-ttu-id="3f3da-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f3da-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3da-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3f3da-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3da-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f3da-146">INPUTS</span></span>

### <span data-ttu-id="3f3da-147">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3f3da-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3f3da-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f3da-148">OUTPUTS</span></span>

### <span data-ttu-id="3f3da-149">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f3da-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="3f3da-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f3da-150">NOTES</span></span>

<span data-ttu-id="3f3da-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3f3da-151">ALIASES</span></span>

<span data-ttu-id="3f3da-152">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3f3da-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f3da-153">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3f3da-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f3da-154">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3f3da-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f3da-155">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3f3da-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f3da-156">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3f3da-157">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3f3da-158">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3f3da-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3f3da-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f3da-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3f3da-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3f3da-162">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="3f3da-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="3f3da-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3f3da-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3f3da-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3f3da-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3f3da-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3f3da-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3f3da-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f3da-167">RELATED LINKS</span></span>
