---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187807"
---
# <span data-ttu-id="ff56f-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="ff56f-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="ff56f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff56f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff56f-103">Eltávolít egy tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="ff56f-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="ff56f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff56f-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff56f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff56f-105">DESCRIPTION</span></span>
<span data-ttu-id="ff56f-106">A **Remove-AzHpcCacheStorageTarget** parancsmag eltávolítja az Azure HPC-gyorsítótárból származó tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="ff56f-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="ff56f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff56f-107">EXAMPLES</span></span>

### <span data-ttu-id="ff56f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ff56f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="ff56f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff56f-109">PARAMETERS</span></span>

### <span data-ttu-id="ff56f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff56f-110">-AsJob</span></span>
<span data-ttu-id="ff56f-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ff56f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff56f-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="ff56f-112">-CacheName</span></span>
<span data-ttu-id="ff56f-113">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="ff56f-113">Name of cache.</span></span>

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

### <span data-ttu-id="ff56f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff56f-114">-DefaultProfile</span></span>
<span data-ttu-id="ff56f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff56f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff56f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ff56f-116">-Force</span></span>
<span data-ttu-id="ff56f-117">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff56f-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ff56f-118">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy el szeretné távolítani a tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="ff56f-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="ff56f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff56f-119">-Name</span></span>
<span data-ttu-id="ff56f-120">A tárolási cél neve</span><span class="sxs-lookup"><span data-stu-id="ff56f-120">Name of storage target.</span></span>

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

### <span data-ttu-id="ff56f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff56f-121">-PassThru</span></span>
<span data-ttu-id="ff56f-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ff56f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ff56f-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ff56f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ff56f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff56f-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff56f-125">Annak az erőforráscsoport-csoportnak a neve, amely alatt el szeretné távolítani a tárterület-tárolót a gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="ff56f-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="ff56f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff56f-126">-Confirm</span></span>
<span data-ttu-id="ff56f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff56f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff56f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff56f-128">-WhatIf</span></span>
<span data-ttu-id="ff56f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff56f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff56f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff56f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff56f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff56f-131">CommonParameters</span></span>
<span data-ttu-id="ff56f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff56f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff56f-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ff56f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff56f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff56f-134">INPUTS</span></span>

### <span data-ttu-id="ff56f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ff56f-135">System.String</span></span>

## <span data-ttu-id="ff56f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff56f-136">OUTPUTS</span></span>

## <span data-ttu-id="ff56f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff56f-137">NOTES</span></span>

## <span data-ttu-id="ff56f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff56f-138">RELATED LINKS</span></span>
