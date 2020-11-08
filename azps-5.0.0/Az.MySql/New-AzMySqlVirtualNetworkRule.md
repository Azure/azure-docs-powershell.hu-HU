---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194110"
---
# <span data-ttu-id="08931-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="08931-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="08931-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08931-102">SYNOPSIS</span></span>
<span data-ttu-id="08931-103">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="08931-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="08931-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08931-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08931-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08931-105">DESCRIPTION</span></span>
<span data-ttu-id="08931-106">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="08931-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="08931-107">Példák</span><span class="sxs-lookup"><span data-stu-id="08931-107">EXAMPLES</span></span>

### <span data-ttu-id="08931-108">Példa 1: új MySql-kiszolgáló virtuális hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="08931-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="08931-109">Ezekkel a parancsmagokkal létrehozhatja a virtuális kiszolgáló virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="08931-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="08931-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08931-110">PARAMETERS</span></span>

### <span data-ttu-id="08931-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08931-111">-AsJob</span></span>
<span data-ttu-id="08931-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="08931-112">Run the command as a job</span></span>

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

### <span data-ttu-id="08931-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08931-113">-DefaultProfile</span></span>
<span data-ttu-id="08931-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08931-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08931-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="08931-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="08931-116">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="08931-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="08931-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08931-117">-Name</span></span>
<span data-ttu-id="08931-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="08931-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08931-119">-Várva</span><span class="sxs-lookup"><span data-stu-id="08931-119">-NoWait</span></span>
<span data-ttu-id="08931-120">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="08931-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="08931-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08931-121">-PassThru</span></span>
<span data-ttu-id="08931-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="08931-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="08931-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08931-123">-ResourceGroupName</span></span>
<span data-ttu-id="08931-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="08931-124">The name of the resource group.</span></span>
<span data-ttu-id="08931-125">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="08931-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="08931-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="08931-126">-ServerName</span></span>
<span data-ttu-id="08931-127">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="08931-127">The name of the server.</span></span>

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

### <span data-ttu-id="08931-128">– NetI</span><span class="sxs-lookup"><span data-stu-id="08931-128">-SubnetId</span></span>
<span data-ttu-id="08931-129">A virtuális hálózati alhálózat ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="08931-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="08931-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08931-130">-SubscriptionId</span></span>
<span data-ttu-id="08931-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="08931-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08931-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08931-132">-Confirm</span></span>
<span data-ttu-id="08931-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08931-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08931-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08931-134">-WhatIf</span></span>
<span data-ttu-id="08931-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08931-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08931-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08931-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08931-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08931-137">CommonParameters</span></span>
<span data-ttu-id="08931-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08931-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08931-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="08931-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08931-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08931-140">INPUTS</span></span>

## <span data-ttu-id="08931-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08931-141">OUTPUTS</span></span>

### <span data-ttu-id="08931-142">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="08931-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="08931-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08931-143">NOTES</span></span>

<span data-ttu-id="08931-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="08931-144">ALIASES</span></span>

## <span data-ttu-id="08931-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08931-145">RELATED LINKS</span></span>

