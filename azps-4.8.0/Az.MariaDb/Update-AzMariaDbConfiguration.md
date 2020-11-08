---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183526"
---
# <span data-ttu-id="6b090-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b090-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="6b090-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b090-102">SYNOPSIS</span></span>
<span data-ttu-id="6b090-103">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6b090-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="6b090-104">Ha a AdministratorLoginPassword, az SKU-ot stb. Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="6b090-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6b090-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b090-105">SYNTAX</span></span>

### <span data-ttu-id="6b090-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b090-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b090-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6b090-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b090-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b090-108">DESCRIPTION</span></span>
<span data-ttu-id="6b090-109">Frissíti a kiszolgáló konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6b090-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="6b090-110">Ha a AdministratorLoginPassword, az SKU-ot stb. Update-AzMariaDberver</span><span class="sxs-lookup"><span data-stu-id="6b090-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6b090-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6b090-111">EXAMPLES</span></span>

### <span data-ttu-id="6b090-112">Példa 1: a MariaDB konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="6b090-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="6b090-113">Ez a parancs frissíti a MariaDB konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6b090-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="6b090-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b090-114">PARAMETERS</span></span>

### <span data-ttu-id="6b090-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b090-115">-AsJob</span></span>
<span data-ttu-id="6b090-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="6b090-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6b090-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b090-117">-DefaultProfile</span></span>
<span data-ttu-id="6b090-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b090-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b090-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b090-119">-InputObject</span></span>
<span data-ttu-id="6b090-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6b090-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b090-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b090-121">-Name</span></span>
<span data-ttu-id="6b090-122">A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="6b090-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="6b090-123">-NoWait</span></span>
<span data-ttu-id="6b090-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="6b090-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6b090-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b090-125">-ResourceGroupName</span></span>
<span data-ttu-id="6b090-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6b090-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="6b090-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6b090-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6b090-128">-ServerName</span></span>
<span data-ttu-id="6b090-129">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-129">The name of the server.</span></span>

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

### <span data-ttu-id="6b090-130">-Forrás</span><span class="sxs-lookup"><span data-stu-id="6b090-130">-Source</span></span>
<span data-ttu-id="6b090-131">A konfiguráció forrása.</span><span class="sxs-lookup"><span data-stu-id="6b090-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="6b090-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b090-132">-SubscriptionId</span></span>
<span data-ttu-id="6b090-133">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="6b090-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6b090-134">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="6b090-134">-Value</span></span>
<span data-ttu-id="6b090-135">A konfiguráció értéke.</span><span class="sxs-lookup"><span data-stu-id="6b090-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="6b090-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6b090-136">-Confirm</span></span>
<span data-ttu-id="6b090-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b090-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b090-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b090-138">-WhatIf</span></span>
<span data-ttu-id="6b090-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6b090-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b090-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b090-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b090-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b090-141">CommonParameters</span></span>
<span data-ttu-id="6b090-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b090-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b090-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6b090-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b090-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b090-144">INPUTS</span></span>

### <span data-ttu-id="6b090-145">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="6b090-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="6b090-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b090-146">OUTPUTS</span></span>

### <span data-ttu-id="6b090-147">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b090-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="6b090-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b090-148">NOTES</span></span>

<span data-ttu-id="6b090-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6b090-149">ALIASES</span></span>

<span data-ttu-id="6b090-150">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6b090-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b090-151">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6b090-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b090-152">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6b090-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b090-153">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6b090-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b090-154">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6b090-155">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6b090-156">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6b090-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6b090-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b090-158">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6b090-159">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6b090-160">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="6b090-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6b090-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6b090-162">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6b090-163">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="6b090-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="6b090-164">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6b090-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6b090-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b090-165">RELATED LINKS</span></span>

