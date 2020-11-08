---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 91d774931ac7ef4b8f1d41a70953d4a5b3a322cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187690"
---
# <span data-ttu-id="9e9aa-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9e9aa-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="9e9aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9aa-103">Virtuális hálózati szabály kap.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="9e9aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e9aa-104">SYNTAX</span></span>

### <span data-ttu-id="9e9aa-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e9aa-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9e9aa-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="9e9aa-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9e9aa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e9aa-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="9e9aa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e9aa-108">DESCRIPTION</span></span>
<span data-ttu-id="9e9aa-109">Virtuális hálózati szabály kap.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="9e9aa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9e9aa-110">EXAMPLES</span></span>

### <span data-ttu-id="9e9aa-111">Példa 1: a virtuális hálózati szabályok listája a megadott MySql-kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="9e9aa-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9e9aa-112">Ez a parancsmag felsorolja a virtuális hálózati szabályokat a megadott MySql-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="9e9aa-113">2. példa: virtuális hálózati szabály beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="9e9aa-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9e9aa-114">Ez a parancsmag név szerint kapja meg a virtuális hálózat szabályát.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="9e9aa-115">3. példa: virtuális hálózati szabály beszerzése identitással</span><span class="sxs-lookup"><span data-stu-id="9e9aa-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9e9aa-116">Ez a parancsmag identitással kapja meg a virtuális hálózat szabályát.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="9e9aa-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e9aa-117">PARAMETERS</span></span>

### <span data-ttu-id="9e9aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9aa-118">-DefaultProfile</span></span>
<span data-ttu-id="9e9aa-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e9aa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e9aa-120">-InputObject</span></span>
<span data-ttu-id="9e9aa-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9aa-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e9aa-122">-Name</span></span>
<span data-ttu-id="9e9aa-123">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9aa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e9aa-124">-PassThru</span></span>
<span data-ttu-id="9e9aa-125">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="9e9aa-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9e9aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e9aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="9e9aa-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-127">The name of the resource group.</span></span>
<span data-ttu-id="9e9aa-128">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-128">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9aa-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="9e9aa-129">-ServerName</span></span>
<span data-ttu-id="9e9aa-130">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-130">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9aa-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e9aa-131">-SubscriptionId</span></span>
<span data-ttu-id="9e9aa-132">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-132">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9aa-133">CommonParameters</span></span>
<span data-ttu-id="9e9aa-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e9aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9aa-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9aa-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e9aa-136">INPUTS</span></span>

### <span data-ttu-id="9e9aa-137">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9e9aa-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9e9aa-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e9aa-138">OUTPUTS</span></span>

### <span data-ttu-id="9e9aa-139">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9e9aa-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="9e9aa-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e9aa-140">NOTES</span></span>

<span data-ttu-id="9e9aa-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9e9aa-141">ALIASES</span></span>

<span data-ttu-id="9e9aa-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="9e9aa-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e9aa-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e9aa-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e9aa-145">INPUTOBJECT <IMySqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="9e9aa-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e9aa-146">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9e9aa-147">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9e9aa-148">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9e9aa-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9e9aa-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e9aa-150">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9e9aa-151">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9e9aa-152">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="9e9aa-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9e9aa-154">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9e9aa-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9e9aa-156">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9e9aa-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e9aa-157">RELATED LINKS</span></span>

