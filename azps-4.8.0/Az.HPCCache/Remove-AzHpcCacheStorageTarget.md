---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183383"
---
# <span data-ttu-id="c8e33-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="c8e33-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="c8e33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8e33-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e33-103">Eltávolít egy tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="c8e33-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="c8e33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8e33-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8e33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8e33-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e33-106">A **Remove-AzHpcCacheStorageTarget** parancsmag eltávolítja az Azure HPC-gyorsítótárból származó tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="c8e33-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="c8e33-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8e33-107">EXAMPLES</span></span>

### <span data-ttu-id="c8e33-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c8e33-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="c8e33-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8e33-109">PARAMETERS</span></span>

### <span data-ttu-id="c8e33-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8e33-110">-AsJob</span></span>
<span data-ttu-id="c8e33-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c8e33-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8e33-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="c8e33-112">-CacheName</span></span>
<span data-ttu-id="c8e33-113">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="c8e33-113">Name of cache.</span></span>

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

### <span data-ttu-id="c8e33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e33-114">-DefaultProfile</span></span>
<span data-ttu-id="c8e33-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8e33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8e33-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c8e33-116">-Force</span></span>
<span data-ttu-id="c8e33-117">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8e33-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="c8e33-118">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy el szeretné távolítani a tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="c8e33-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="c8e33-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8e33-119">-Name</span></span>
<span data-ttu-id="c8e33-120">A tárolási cél neve</span><span class="sxs-lookup"><span data-stu-id="c8e33-120">Name of storage target.</span></span>

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

### <span data-ttu-id="c8e33-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8e33-121">-PassThru</span></span>
<span data-ttu-id="c8e33-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c8e33-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8e33-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c8e33-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8e33-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e33-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8e33-125">Annak az erőforráscsoport-csoportnak a neve, amely alatt el szeretné távolítani a tárterület-tárolót a gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="c8e33-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="c8e33-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8e33-126">-Confirm</span></span>
<span data-ttu-id="c8e33-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8e33-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8e33-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e33-128">-WhatIf</span></span>
<span data-ttu-id="c8e33-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8e33-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8e33-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8e33-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8e33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e33-131">CommonParameters</span></span>
<span data-ttu-id="c8e33-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8e33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e33-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8e33-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e33-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8e33-134">INPUTS</span></span>

### <span data-ttu-id="c8e33-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c8e33-135">System.String</span></span>

## <span data-ttu-id="c8e33-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8e33-136">OUTPUTS</span></span>

## <span data-ttu-id="c8e33-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8e33-137">NOTES</span></span>

## <span data-ttu-id="c8e33-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8e33-138">RELATED LINKS</span></span>
