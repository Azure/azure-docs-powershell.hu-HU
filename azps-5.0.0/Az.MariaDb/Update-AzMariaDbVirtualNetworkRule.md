---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195799"
---
# <span data-ttu-id="dc0bd-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dc0bd-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="dc0bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0bd-103">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="dc0bd-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="dc0bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc0bd-104">SYNTAX</span></span>

### <span data-ttu-id="dc0bd-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc0bd-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dc0bd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dc0bd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dc0bd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc0bd-107">DESCRIPTION</span></span>
<span data-ttu-id="dc0bd-108">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="dc0bd-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="dc0bd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dc0bd-109">EXAMPLES</span></span>

### <span data-ttu-id="dc0bd-110">Példa 1: a MariaDB virtuális hálózati szabályának frissítése</span><span class="sxs-lookup"><span data-stu-id="dc0bd-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="dc0bd-111">Ez a parancs frissíti a virtuális hálózati szabályokat.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="dc0bd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc0bd-112">PARAMETERS</span></span>

### <span data-ttu-id="dc0bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc0bd-113">-AsJob</span></span>
<span data-ttu-id="dc0bd-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="dc0bd-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dc0bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0bd-115">-DefaultProfile</span></span>
<span data-ttu-id="dc0bd-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc0bd-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc0bd-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="dc0bd-118">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="dc0bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc0bd-119">-InputObject</span></span>
<span data-ttu-id="dc0bd-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc0bd-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc0bd-121">-Name</span></span>
<span data-ttu-id="dc0bd-122">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0bd-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="dc0bd-123">-NoWait</span></span>
<span data-ttu-id="dc0bd-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="dc0bd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc0bd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc0bd-125">-PassThru</span></span>
<span data-ttu-id="dc0bd-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="dc0bd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dc0bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc0bd-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dc0bd-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dc0bd-130">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="dc0bd-130">-ServerName</span></span>
<span data-ttu-id="dc0bd-131">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-131">The name of the server.</span></span>

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

### <span data-ttu-id="dc0bd-132">– NetI</span><span class="sxs-lookup"><span data-stu-id="dc0bd-132">-SubnetId</span></span>
<span data-ttu-id="dc0bd-133">A virtuális hálózati alhálózat ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="dc0bd-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc0bd-134">-SubscriptionId</span></span>
<span data-ttu-id="dc0bd-135">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="dc0bd-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc0bd-136">-Confirm</span></span>
<span data-ttu-id="dc0bd-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc0bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc0bd-138">-WhatIf</span></span>
<span data-ttu-id="dc0bd-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc0bd-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc0bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0bd-141">CommonParameters</span></span>
<span data-ttu-id="dc0bd-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc0bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0bd-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0bd-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc0bd-144">INPUTS</span></span>

### <span data-ttu-id="dc0bd-145">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="dc0bd-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="dc0bd-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc0bd-146">OUTPUTS</span></span>

### <span data-ttu-id="dc0bd-147">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dc0bd-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="dc0bd-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc0bd-148">NOTES</span></span>

<span data-ttu-id="dc0bd-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dc0bd-149">ALIASES</span></span>

<span data-ttu-id="dc0bd-150">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="dc0bd-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc0bd-151">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc0bd-152">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc0bd-153">INPUTOBJECT <IMariaDbIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="dc0bd-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc0bd-154">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dc0bd-155">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dc0bd-156">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dc0bd-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="dc0bd-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc0bd-158">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dc0bd-159">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="dc0bd-160">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="dc0bd-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dc0bd-162">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dc0bd-163">`[SubscriptionId <String>]`: Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="dc0bd-164">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="dc0bd-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dc0bd-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc0bd-165">RELATED LINKS</span></span>
