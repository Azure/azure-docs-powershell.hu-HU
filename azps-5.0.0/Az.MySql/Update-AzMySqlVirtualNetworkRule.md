---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186574"
---
# <span data-ttu-id="6df76-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6df76-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="6df76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6df76-102">SYNOPSIS</span></span>
<span data-ttu-id="6df76-103">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="6df76-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="6df76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6df76-104">SYNTAX</span></span>

### <span data-ttu-id="6df76-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6df76-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6df76-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6df76-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6df76-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6df76-107">DESCRIPTION</span></span>
<span data-ttu-id="6df76-108">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="6df76-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="6df76-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6df76-109">EXAMPLES</span></span>

### <span data-ttu-id="6df76-110">1. példa: a virtuális virtuális hálózat szabályának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="6df76-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="6df76-111">Ez a parancsmag a MySql virtuális hálózati szabály név szerint frissül.</span><span class="sxs-lookup"><span data-stu-id="6df76-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="6df76-112">2. példa: a virtuális virtuális hálózat szabályának frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="6df76-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="6df76-113">Ezek a parancsmagok a MySql virtuális hálózati szabályt identitás szerint frissítik.</span><span class="sxs-lookup"><span data-stu-id="6df76-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="6df76-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6df76-114">PARAMETERS</span></span>

### <span data-ttu-id="6df76-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6df76-115">-AsJob</span></span>
<span data-ttu-id="6df76-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="6df76-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6df76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df76-117">-DefaultProfile</span></span>
<span data-ttu-id="6df76-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6df76-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df76-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6df76-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="6df76-120">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="6df76-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="6df76-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6df76-121">-InputObject</span></span>
<span data-ttu-id="6df76-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6df76-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6df76-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6df76-123">-Name</span></span>
<span data-ttu-id="6df76-124">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6df76-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="6df76-125">-NoWait</span></span>
<span data-ttu-id="6df76-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="6df76-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6df76-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6df76-127">-PassThru</span></span>
<span data-ttu-id="6df76-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="6df76-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6df76-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df76-129">-ResourceGroupName</span></span>
<span data-ttu-id="6df76-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-130">The name of the resource group.</span></span>
<span data-ttu-id="6df76-131">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6df76-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6df76-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6df76-132">-ServerName</span></span>
<span data-ttu-id="6df76-133">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-133">The name of the server.</span></span>

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

### <span data-ttu-id="6df76-134">– NetI</span><span class="sxs-lookup"><span data-stu-id="6df76-134">-SubnetId</span></span>
<span data-ttu-id="6df76-135">A virtuális hálózati alhálózat ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6df76-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="6df76-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6df76-136">-SubscriptionId</span></span>
<span data-ttu-id="6df76-137">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6df76-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6df76-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6df76-138">-Confirm</span></span>
<span data-ttu-id="6df76-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6df76-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df76-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df76-140">-WhatIf</span></span>
<span data-ttu-id="6df76-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6df76-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6df76-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6df76-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df76-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df76-143">CommonParameters</span></span>
<span data-ttu-id="6df76-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6df76-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df76-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6df76-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df76-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6df76-146">INPUTS</span></span>

### <span data-ttu-id="6df76-147">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6df76-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="6df76-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6df76-148">OUTPUTS</span></span>

### <span data-ttu-id="6df76-149">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6df76-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="6df76-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6df76-150">NOTES</span></span>

<span data-ttu-id="6df76-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6df76-151">ALIASES</span></span>

<span data-ttu-id="6df76-152">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6df76-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6df76-153">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6df76-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6df76-154">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6df76-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6df76-155">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6df76-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6df76-156">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6df76-157">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6df76-158">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6df76-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6df76-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6df76-160">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6df76-161">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6df76-162">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6df76-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="6df76-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6df76-164">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6df76-165">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6df76-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6df76-166">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6df76-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6df76-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6df76-167">RELATED LINKS</span></span>
