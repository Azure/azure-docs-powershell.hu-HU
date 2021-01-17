---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339438"
---
# <span data-ttu-id="84917-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="84917-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="84917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84917-102">SYNOPSIS</span></span>
<span data-ttu-id="84917-103">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="84917-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="84917-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84917-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84917-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84917-105">DESCRIPTION</span></span>
<span data-ttu-id="84917-106">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="84917-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="84917-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84917-107">EXAMPLES</span></span>

### <span data-ttu-id="84917-108">1. példa: Új MySql-kiszolgáló virtuális hálózatszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="84917-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="84917-109">Ezek a parancsmagok MySql-kiszolgáló virtuális hálózatszabályt hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="84917-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="84917-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84917-110">PARAMETERS</span></span>

### <span data-ttu-id="84917-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84917-111">-AsJob</span></span>
<span data-ttu-id="84917-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="84917-112">Run the command as a job</span></span>

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

### <span data-ttu-id="84917-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84917-113">-DefaultProfile</span></span>
<span data-ttu-id="84917-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84917-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84917-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="84917-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="84917-116">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="84917-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="84917-117">-Name</span><span class="sxs-lookup"><span data-stu-id="84917-117">-Name</span></span>
<span data-ttu-id="84917-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="84917-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="84917-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="84917-119">-NoWait</span></span>
<span data-ttu-id="84917-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="84917-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84917-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84917-121">-PassThru</span></span>
<span data-ttu-id="84917-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="84917-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="84917-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84917-123">-ResourceGroupName</span></span>
<span data-ttu-id="84917-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="84917-124">The name of the resource group.</span></span>
<span data-ttu-id="84917-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="84917-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="84917-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="84917-126">-ServerName</span></span>
<span data-ttu-id="84917-127">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="84917-127">The name of the server.</span></span>

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

### <span data-ttu-id="84917-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="84917-128">-SubnetId</span></span>
<span data-ttu-id="84917-129">A ARM alhálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="84917-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="84917-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84917-130">-SubscriptionId</span></span>
<span data-ttu-id="84917-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="84917-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="84917-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84917-132">-Confirm</span></span>
<span data-ttu-id="84917-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="84917-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84917-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84917-134">-WhatIf</span></span>
<span data-ttu-id="84917-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="84917-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84917-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84917-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84917-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84917-137">CommonParameters</span></span>
<span data-ttu-id="84917-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84917-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84917-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84917-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84917-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84917-140">INPUTS</span></span>

## <span data-ttu-id="84917-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84917-141">OUTPUTS</span></span>

### <span data-ttu-id="84917-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="84917-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="84917-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84917-143">NOTES</span></span>

<span data-ttu-id="84917-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="84917-144">ALIASES</span></span>

## <span data-ttu-id="84917-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84917-145">RELATED LINKS</span></span>

