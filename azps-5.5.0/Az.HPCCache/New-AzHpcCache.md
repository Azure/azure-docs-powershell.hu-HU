---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209390"
---
# <span data-ttu-id="b2350-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="b2350-101">New-AzHpcCache</span></span>

## <span data-ttu-id="b2350-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2350-102">SYNOPSIS</span></span>
<span data-ttu-id="b2350-103">HPC-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b2350-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="b2350-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2350-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2350-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2350-105">DESCRIPTION</span></span>
<span data-ttu-id="b2350-106">A **New-AzHpcCache** parancsmag létrehoz egy Azure HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="b2350-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="b2350-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2350-107">EXAMPLES</span></span>

### <span data-ttu-id="b2350-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b2350-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="b2350-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2350-109">PARAMETERS</span></span>

### <span data-ttu-id="b2350-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2350-110">-AsJob</span></span>
<span data-ttu-id="b2350-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b2350-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2350-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="b2350-112">-CacheSize</span></span>
<span data-ttu-id="b2350-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="b2350-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2350-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2350-114">-DefaultProfile</span></span>
<span data-ttu-id="b2350-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2350-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2350-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b2350-116">-Location</span></span>
<span data-ttu-id="b2350-117">Hely.</span><span class="sxs-lookup"><span data-stu-id="b2350-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2350-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b2350-118">-Name</span></span>
<span data-ttu-id="b2350-119">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="b2350-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2350-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2350-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2350-121">Annak az erőforráscsoportnak a neve, amely alatt gyorsítótárat szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="b2350-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2350-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="b2350-122">-Sku</span></span>
<span data-ttu-id="b2350-123">Termékváltozat.</span><span class="sxs-lookup"><span data-stu-id="b2350-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2350-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="b2350-124">-SubnetUri</span></span>
<span data-ttu-id="b2350-125">AlhálózatI.</span><span class="sxs-lookup"><span data-stu-id="b2350-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2350-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2350-126">-Tag</span></span>
<span data-ttu-id="b2350-127">A HPC cache-hez társítva lévő címkék.</span><span class="sxs-lookup"><span data-stu-id="b2350-127">The tags to associate with HPC Cache.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2350-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2350-128">-Confirm</span></span>
<span data-ttu-id="b2350-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b2350-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2350-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2350-130">-WhatIf</span></span>
<span data-ttu-id="b2350-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b2350-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2350-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2350-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2350-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2350-133">CommonParameters</span></span>
<span data-ttu-id="b2350-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2350-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2350-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2350-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2350-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2350-136">INPUTS</span></span>

### <span data-ttu-id="b2350-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b2350-137">System.String</span></span>

### <span data-ttu-id="b2350-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b2350-138">System.Int32</span></span>

## <span data-ttu-id="b2350-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2350-139">OUTPUTS</span></span>

### <span data-ttu-id="b2350-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="b2350-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="b2350-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2350-141">NOTES</span></span>

## <span data-ttu-id="b2350-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2350-142">RELATED LINKS</span></span>
