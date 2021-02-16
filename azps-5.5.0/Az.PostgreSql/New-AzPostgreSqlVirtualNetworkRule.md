---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160347"
---
# <span data-ttu-id="92e0c-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="92e0c-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="92e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="92e0c-103">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="92e0c-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="92e0c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92e0c-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92e0c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="92e0c-106">Egy meglévő virtuális hálózati szabály létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="92e0c-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="92e0c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="92e0c-108">1. példa: Új PostgreSql-kiszolgáló virtuális hálózatszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="92e0c-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="92e0c-109">Ezek a parancsmagok PostgreSql-kiszolgáló virtuális hálózatszabályt hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="92e0c-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="92e0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92e0c-110">PARAMETERS</span></span>

### <span data-ttu-id="92e0c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92e0c-111">-AsJob</span></span>
<span data-ttu-id="92e0c-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="92e0c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="92e0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e0c-113">-DefaultProfile</span></span>
<span data-ttu-id="92e0c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92e0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e0c-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e0c-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="92e0c-116">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="92e0c-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="92e0c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="92e0c-117">-Name</span></span>
<span data-ttu-id="92e0c-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="92e0c-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="92e0c-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92e0c-119">-NoWait</span></span>
<span data-ttu-id="92e0c-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="92e0c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="92e0c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92e0c-121">-PassThru</span></span>
<span data-ttu-id="92e0c-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="92e0c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92e0c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e0c-123">-ResourceGroupName</span></span>
<span data-ttu-id="92e0c-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92e0c-124">The name of the resource group.</span></span>
<span data-ttu-id="92e0c-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="92e0c-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="92e0c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="92e0c-126">-ServerName</span></span>
<span data-ttu-id="92e0c-127">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="92e0c-127">The name of the server.</span></span>

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

### <span data-ttu-id="92e0c-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="92e0c-128">-SubnetId</span></span>
<span data-ttu-id="92e0c-129">A ARM alhálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92e0c-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="92e0c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92e0c-130">-SubscriptionId</span></span>
<span data-ttu-id="92e0c-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92e0c-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="92e0c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92e0c-132">-Confirm</span></span>
<span data-ttu-id="92e0c-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92e0c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92e0c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92e0c-134">-WhatIf</span></span>
<span data-ttu-id="92e0c-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92e0c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e0c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92e0c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92e0c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e0c-137">CommonParameters</span></span>
<span data-ttu-id="92e0c-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e0c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e0c-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92e0c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e0c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92e0c-140">INPUTS</span></span>

## <span data-ttu-id="92e0c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92e0c-141">OUTPUTS</span></span>

### <span data-ttu-id="92e0c-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="92e0c-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="92e0c-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92e0c-143">NOTES</span></span>

<span data-ttu-id="92e0c-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="92e0c-144">ALIASES</span></span>

## <span data-ttu-id="92e0c-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92e0c-145">RELATED LINKS</span></span>

