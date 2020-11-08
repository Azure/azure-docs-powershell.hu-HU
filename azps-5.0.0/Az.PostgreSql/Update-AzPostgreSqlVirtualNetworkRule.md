---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194207"
---
# <span data-ttu-id="6d8cb-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6d8cb-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="6d8cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8cb-103">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="6d8cb-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="6d8cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d8cb-104">SYNTAX</span></span>

### <span data-ttu-id="6d8cb-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d8cb-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d8cb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6d8cb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d8cb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d8cb-107">DESCRIPTION</span></span>
<span data-ttu-id="6d8cb-108">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="6d8cb-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="6d8cb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6d8cb-109">EXAMPLES</span></span>

### <span data-ttu-id="6d8cb-110">1. példa: a PostgreSql virtuális hálózat szabályának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="6d8cb-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="6d8cb-111">Ez a parancsmag a PostgreSql virtuális hálózati szabályát frissíti név szerint.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="6d8cb-112">2. példa: a PostgreSql virtuális hálózat szabályának frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="6d8cb-113">Ezek a parancsmagok a PostgreSql virtuális hálózati szabályát identitás szerint frissítik.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="6d8cb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d8cb-114">PARAMETERS</span></span>

### <span data-ttu-id="6d8cb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d8cb-115">-AsJob</span></span>
<span data-ttu-id="6d8cb-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="6d8cb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6d8cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8cb-117">-DefaultProfile</span></span>
<span data-ttu-id="6d8cb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d8cb-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d8cb-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="6d8cb-120">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="6d8cb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d8cb-121">-InputObject</span></span>
<span data-ttu-id="6d8cb-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d8cb-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d8cb-123">-Name</span></span>
<span data-ttu-id="6d8cb-124">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6d8cb-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="6d8cb-125">-NoWait</span></span>
<span data-ttu-id="6d8cb-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="6d8cb-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d8cb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d8cb-127">-PassThru</span></span>
<span data-ttu-id="6d8cb-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="6d8cb-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6d8cb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8cb-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d8cb-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-130">The name of the resource group.</span></span>
<span data-ttu-id="6d8cb-131">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6d8cb-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6d8cb-132">-ServerName</span></span>
<span data-ttu-id="6d8cb-133">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-133">The name of the server.</span></span>

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

### <span data-ttu-id="6d8cb-134">– NetI</span><span class="sxs-lookup"><span data-stu-id="6d8cb-134">-SubnetId</span></span>
<span data-ttu-id="6d8cb-135">A virtuális hálózati alhálózat ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d8cb-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d8cb-136">-SubscriptionId</span></span>
<span data-ttu-id="6d8cb-137">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6d8cb-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d8cb-138">-Confirm</span></span>
<span data-ttu-id="6d8cb-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d8cb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d8cb-140">-WhatIf</span></span>
<span data-ttu-id="6d8cb-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d8cb-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d8cb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8cb-143">CommonParameters</span></span>
<span data-ttu-id="6d8cb-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d8cb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8cb-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8cb-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d8cb-146">INPUTS</span></span>

### <span data-ttu-id="6d8cb-147">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6d8cb-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6d8cb-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d8cb-148">OUTPUTS</span></span>

### <span data-ttu-id="6d8cb-149">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6d8cb-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="6d8cb-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d8cb-150">NOTES</span></span>

<span data-ttu-id="6d8cb-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6d8cb-151">ALIASES</span></span>

<span data-ttu-id="6d8cb-152">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6d8cb-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d8cb-153">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d8cb-154">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d8cb-155">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6d8cb-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d8cb-156">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6d8cb-157">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6d8cb-158">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6d8cb-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6d8cb-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d8cb-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6d8cb-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6d8cb-162">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="6d8cb-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6d8cb-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6d8cb-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6d8cb-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6d8cb-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6d8cb-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d8cb-167">RELATED LINKS</span></span>
