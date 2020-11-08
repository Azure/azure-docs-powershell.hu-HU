---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182220"
---
# <span data-ttu-id="da96d-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="da96d-101">New-AzHpcCache</span></span>

## <span data-ttu-id="da96d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da96d-102">SYNOPSIS</span></span>
<span data-ttu-id="da96d-103">HPC-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da96d-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="da96d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da96d-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da96d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da96d-105">DESCRIPTION</span></span>
<span data-ttu-id="da96d-106">A **New-AzHpcCache** parancsmag egy Azure HPC-gyorsítótárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da96d-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="da96d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da96d-107">EXAMPLES</span></span>

### <span data-ttu-id="da96d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da96d-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="da96d-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da96d-109">PARAMETERS</span></span>

### <span data-ttu-id="da96d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da96d-110">-AsJob</span></span>
<span data-ttu-id="da96d-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da96d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da96d-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="da96d-112">-CacheSize</span></span>
<span data-ttu-id="da96d-113">CACHESIZE.</span><span class="sxs-lookup"><span data-stu-id="da96d-113">CacheSize.</span></span>

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

### <span data-ttu-id="da96d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da96d-114">-DefaultProfile</span></span>
<span data-ttu-id="da96d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da96d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da96d-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="da96d-116">-Location</span></span>
<span data-ttu-id="da96d-117">Helyre.</span><span class="sxs-lookup"><span data-stu-id="da96d-117">Location.</span></span>

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

### <span data-ttu-id="da96d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da96d-118">-Name</span></span>
<span data-ttu-id="da96d-119">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="da96d-119">Name of cache.</span></span>

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

### <span data-ttu-id="da96d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da96d-120">-ResourceGroupName</span></span>
<span data-ttu-id="da96d-121">Annak az erőforráscsoport-csoportnak a neve, amelyben a gyorsítótárat létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="da96d-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="da96d-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="da96d-122">-Sku</span></span>
<span data-ttu-id="da96d-123">Termékváltozat.</span><span class="sxs-lookup"><span data-stu-id="da96d-123">Sku.</span></span>

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

### <span data-ttu-id="da96d-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="da96d-124">-SubnetUri</span></span>
<span data-ttu-id="da96d-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="da96d-125">SubnetURI.</span></span>

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

### <span data-ttu-id="da96d-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="da96d-126">-Tag</span></span>
<span data-ttu-id="da96d-127">A HPC-gyorsítótárral társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="da96d-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="da96d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da96d-128">-Confirm</span></span>
<span data-ttu-id="da96d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da96d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da96d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da96d-130">-WhatIf</span></span>
<span data-ttu-id="da96d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da96d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da96d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da96d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da96d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da96d-133">CommonParameters</span></span>
<span data-ttu-id="da96d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da96d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da96d-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da96d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da96d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da96d-136">INPUTS</span></span>

### <span data-ttu-id="da96d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="da96d-137">System.String</span></span>

### <span data-ttu-id="da96d-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="da96d-138">System.Int32</span></span>

## <span data-ttu-id="da96d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da96d-139">OUTPUTS</span></span>

### <span data-ttu-id="da96d-140">Microsoft. Azure. PowerShell. parancsmagok. HPCCache. models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="da96d-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="da96d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da96d-141">NOTES</span></span>

## <span data-ttu-id="da96d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da96d-142">RELATED LINKS</span></span>
