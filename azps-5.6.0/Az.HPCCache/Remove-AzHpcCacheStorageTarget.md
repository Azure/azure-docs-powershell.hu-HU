---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 2de3856a51ce8b55d6db7a82f6e50027b60d9d87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013510"
---
# <span data-ttu-id="2787f-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="2787f-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="2787f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2787f-102">SYNOPSIS</span></span>
<span data-ttu-id="2787f-103">Eltávolítja a tárterület célhelyét.</span><span class="sxs-lookup"><span data-stu-id="2787f-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="2787f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2787f-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2787f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2787f-105">DESCRIPTION</span></span>
<span data-ttu-id="2787f-106">A **Remove-AzHpcCacheStorageTarget** parancsmag eltávolítja a tárterület célhelyét az Azure HPC-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="2787f-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="2787f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2787f-107">EXAMPLES</span></span>

### <span data-ttu-id="2787f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2787f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="2787f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2787f-109">PARAMETERS</span></span>

### <span data-ttu-id="2787f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2787f-110">-AsJob</span></span>
<span data-ttu-id="2787f-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2787f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2787f-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="2787f-112">-CacheName</span></span>
<span data-ttu-id="2787f-113">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="2787f-113">Name of cache.</span></span>

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

### <span data-ttu-id="2787f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2787f-114">-DefaultProfile</span></span>
<span data-ttu-id="2787f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2787f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2787f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2787f-116">-Force</span></span>
<span data-ttu-id="2787f-117">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2787f-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="2787f-118">Ez a parancsmag alapértelmezés szerint kérni fogja, hogy erősítse meg a tárterület célhelyének eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="2787f-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="2787f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2787f-119">-Name</span></span>
<span data-ttu-id="2787f-120">A tárolási cél neve.</span><span class="sxs-lookup"><span data-stu-id="2787f-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2787f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2787f-121">-PassThru</span></span>
<span data-ttu-id="2787f-122">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="2787f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2787f-123">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2787f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2787f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2787f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2787f-125">Annak az erőforráscsoportnak a neve, amely alatt el szeretné távolítani a tárterület célhelyét a gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="2787f-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="2787f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2787f-126">-Confirm</span></span>
<span data-ttu-id="2787f-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2787f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2787f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2787f-128">-WhatIf</span></span>
<span data-ttu-id="2787f-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2787f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2787f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2787f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2787f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2787f-131">CommonParameters</span></span>
<span data-ttu-id="2787f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2787f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2787f-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2787f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2787f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2787f-134">INPUTS</span></span>

### <span data-ttu-id="2787f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2787f-135">System.String</span></span>

## <span data-ttu-id="2787f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2787f-136">OUTPUTS</span></span>

## <span data-ttu-id="2787f-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2787f-137">NOTES</span></span>

## <span data-ttu-id="2787f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2787f-138">RELATED LINKS</span></span>
