---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194892"
---
# <span data-ttu-id="1e705-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1e705-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="1e705-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e705-102">SYNOPSIS</span></span>
<span data-ttu-id="1e705-103">Virtuális hálózati szabály kap.</span><span class="sxs-lookup"><span data-stu-id="1e705-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="1e705-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e705-104">SYNTAX</span></span>

### <span data-ttu-id="1e705-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e705-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1e705-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1e705-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1e705-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1e705-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="1e705-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e705-108">DESCRIPTION</span></span>
<span data-ttu-id="1e705-109">Virtuális hálózati szabály kap.</span><span class="sxs-lookup"><span data-stu-id="1e705-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="1e705-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1e705-110">EXAMPLES</span></span>

### <span data-ttu-id="1e705-111">Példa 1: a megadott PostgreSql-kiszolgálón található virtuális hálózati szabályok felsorolása</span><span class="sxs-lookup"><span data-stu-id="1e705-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="1e705-112">Ez a parancsmag felsorolja az összes virtuális hálózati szabályt a megadott PostgreSql-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="1e705-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="1e705-113">2. példa: virtuális hálózati szabály beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="1e705-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="1e705-114">Ez a parancsmag név szerint kapja meg a virtuális hálózat szabályát.</span><span class="sxs-lookup"><span data-stu-id="1e705-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="1e705-115">3. példa: virtuális hálózati szabály beszerzése identitással</span><span class="sxs-lookup"><span data-stu-id="1e705-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="1e705-116">Ez a parancsmag identitással kapja meg a virtuális hálózat szabályát.</span><span class="sxs-lookup"><span data-stu-id="1e705-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="1e705-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e705-117">PARAMETERS</span></span>

### <span data-ttu-id="1e705-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e705-118">-DefaultProfile</span></span>
<span data-ttu-id="1e705-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e705-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e705-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e705-120">-InputObject</span></span>
<span data-ttu-id="1e705-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e705-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e705-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e705-122">-Name</span></span>
<span data-ttu-id="1e705-123">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="1e705-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e705-124">-PassThru</span></span>
<span data-ttu-id="1e705-125">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="1e705-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1e705-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e705-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e705-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-127">The name of the resource group.</span></span>
<span data-ttu-id="1e705-128">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="1e705-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1e705-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1e705-129">-ServerName</span></span>
<span data-ttu-id="1e705-130">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-130">The name of the server.</span></span>

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

### <span data-ttu-id="1e705-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e705-131">-SubscriptionId</span></span>
<span data-ttu-id="1e705-132">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1e705-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1e705-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e705-133">CommonParameters</span></span>
<span data-ttu-id="1e705-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e705-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e705-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e705-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e705-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e705-136">INPUTS</span></span>

### <span data-ttu-id="1e705-137">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1e705-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="1e705-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e705-138">OUTPUTS</span></span>

### <span data-ttu-id="1e705-139">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1e705-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="1e705-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e705-140">NOTES</span></span>

<span data-ttu-id="1e705-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1e705-141">ALIASES</span></span>

<span data-ttu-id="1e705-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="1e705-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e705-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1e705-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e705-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1e705-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e705-145">INPUTOBJECT <IPostgreSqlIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1e705-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e705-146">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1e705-147">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1e705-148">`[FirewallRuleName <String>]`: A kiszolgáló tűzfala szabály neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1e705-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1e705-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e705-150">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1e705-151">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1e705-152">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="1e705-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="1e705-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági figyelmeztetés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1e705-154">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1e705-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1e705-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1e705-156">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="1e705-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1e705-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e705-157">RELATED LINKS</span></span>
