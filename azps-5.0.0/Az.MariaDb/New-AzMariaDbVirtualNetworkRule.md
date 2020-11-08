---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194354"
---
# <span data-ttu-id="3e539-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3e539-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="3e539-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e539-102">SYNOPSIS</span></span>
<span data-ttu-id="3e539-103">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="3e539-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="3e539-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e539-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e539-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e539-105">DESCRIPTION</span></span>
<span data-ttu-id="3e539-106">Meglévő virtuális hálózati szabály létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="3e539-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="3e539-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3e539-107">EXAMPLES</span></span>

### <span data-ttu-id="3e539-108">Példa 1: virtuális hálózati szabály létrehozása MariaDB</span><span class="sxs-lookup"><span data-stu-id="3e539-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="3e539-109">Ez a parancs virtuális hálózati szabályt hoz létre egy MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3e539-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="3e539-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e539-110">PARAMETERS</span></span>

### <span data-ttu-id="3e539-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e539-111">-AsJob</span></span>
<span data-ttu-id="3e539-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="3e539-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3e539-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e539-113">-DefaultProfile</span></span>
<span data-ttu-id="3e539-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e539-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e539-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e539-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="3e539-116">Tűzfalszabály létrehozása: mielőtt a virtuális hálózat vnet-szolgáltatási végpont engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="3e539-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="3e539-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e539-117">-Name</span></span>
<span data-ttu-id="3e539-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3e539-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="3e539-119">-Várva</span><span class="sxs-lookup"><span data-stu-id="3e539-119">-NoWait</span></span>
<span data-ttu-id="3e539-120">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="3e539-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3e539-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e539-121">-PassThru</span></span>
<span data-ttu-id="3e539-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="3e539-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3e539-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e539-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e539-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e539-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3e539-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="3e539-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3e539-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3e539-126">-ServerName</span></span>
<span data-ttu-id="3e539-127">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3e539-127">The name of the server.</span></span>

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

### <span data-ttu-id="3e539-128">– NetI</span><span class="sxs-lookup"><span data-stu-id="3e539-128">-SubnetId</span></span>
<span data-ttu-id="3e539-129">A virtuális hálózati alhálózat ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3e539-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="3e539-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e539-130">-SubscriptionId</span></span>
<span data-ttu-id="3e539-131">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3e539-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3e539-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e539-132">-Confirm</span></span>
<span data-ttu-id="3e539-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e539-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e539-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e539-134">-WhatIf</span></span>
<span data-ttu-id="3e539-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e539-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e539-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e539-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e539-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e539-137">CommonParameters</span></span>
<span data-ttu-id="3e539-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e539-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e539-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3e539-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e539-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e539-140">INPUTS</span></span>

## <span data-ttu-id="3e539-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e539-141">OUTPUTS</span></span>

### <span data-ttu-id="3e539-142">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3e539-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="3e539-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e539-143">NOTES</span></span>

<span data-ttu-id="3e539-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3e539-144">ALIASES</span></span>

## <span data-ttu-id="3e539-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e539-145">RELATED LINKS</span></span>

