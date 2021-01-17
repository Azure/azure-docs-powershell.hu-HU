---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351102"
---
# <span data-ttu-id="9ea22-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9ea22-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="9ea22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ea22-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea22-103">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="9ea22-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="9ea22-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ea22-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ea22-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ea22-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea22-106">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="9ea22-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="9ea22-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ea22-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea22-108">1. példa: Virtuális hálózati szabály létrehozása a MariaDB-hez</span><span class="sxs-lookup"><span data-stu-id="9ea22-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="9ea22-109">Ez a parancs virtuális hálózati szabályt hoz létre a MariaDB-hez.</span><span class="sxs-lookup"><span data-stu-id="9ea22-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="9ea22-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ea22-110">PARAMETERS</span></span>

### <span data-ttu-id="9ea22-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ea22-111">-AsJob</span></span>
<span data-ttu-id="9ea22-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="9ea22-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9ea22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea22-113">-DefaultProfile</span></span>
<span data-ttu-id="9ea22-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ea22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ea22-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ea22-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="9ea22-116">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="9ea22-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="9ea22-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ea22-117">-Name</span></span>
<span data-ttu-id="9ea22-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9ea22-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="9ea22-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9ea22-119">-NoWait</span></span>
<span data-ttu-id="9ea22-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="9ea22-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9ea22-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ea22-121">-PassThru</span></span>
<span data-ttu-id="9ea22-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="9ea22-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9ea22-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea22-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ea22-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9ea22-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9ea22-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="9ea22-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9ea22-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9ea22-126">-ServerName</span></span>
<span data-ttu-id="9ea22-127">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9ea22-127">The name of the server.</span></span>

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

### <span data-ttu-id="9ea22-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9ea22-128">-SubnetId</span></span>
<span data-ttu-id="9ea22-129">A ARM alhálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9ea22-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="9ea22-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ea22-130">-SubscriptionId</span></span>
<span data-ttu-id="9ea22-131">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="9ea22-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9ea22-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ea22-132">-Confirm</span></span>
<span data-ttu-id="9ea22-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9ea22-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea22-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea22-134">-WhatIf</span></span>
<span data-ttu-id="9ea22-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9ea22-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea22-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ea22-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea22-137">CommonParameters</span></span>
<span data-ttu-id="9ea22-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ea22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea22-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ea22-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea22-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ea22-140">INPUTS</span></span>

## <span data-ttu-id="9ea22-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ea22-141">OUTPUTS</span></span>

### <span data-ttu-id="9ea22-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9ea22-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="9ea22-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ea22-143">NOTES</span></span>

<span data-ttu-id="9ea22-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9ea22-144">ALIASES</span></span>

## <span data-ttu-id="9ea22-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ea22-145">RELATED LINKS</span></span>

