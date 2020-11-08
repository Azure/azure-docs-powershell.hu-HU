---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181755"
---
# <span data-ttu-id="e522c-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e522c-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="e522c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e522c-102">SYNOPSIS</span></span>
<span data-ttu-id="e522c-103">A HPC-gyorsítótár eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e522c-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="e522c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e522c-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e522c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e522c-105">DESCRIPTION</span></span>
<span data-ttu-id="e522c-106">A **Remove-AzHpcCache** parancsmag eltávolítja az Azure HPC-gyorsítótárát.</span><span class="sxs-lookup"><span data-stu-id="e522c-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="e522c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e522c-107">EXAMPLES</span></span>

### <span data-ttu-id="e522c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e522c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e522c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e522c-109">PARAMETERS</span></span>

### <span data-ttu-id="e522c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e522c-110">-AsJob</span></span>
<span data-ttu-id="e522c-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e522c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e522c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e522c-112">-DefaultProfile</span></span>
<span data-ttu-id="e522c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e522c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e522c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e522c-114">-Force</span></span>
<span data-ttu-id="e522c-115">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e522c-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e522c-116">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy el szeretné távolítani a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="e522c-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="e522c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e522c-117">-Name</span></span>
<span data-ttu-id="e522c-118">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="e522c-118">Name of cache.</span></span>

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

### <span data-ttu-id="e522c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e522c-119">-PassThru</span></span>
<span data-ttu-id="e522c-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e522c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e522c-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e522c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e522c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e522c-122">-ResourceGroupName</span></span>
<span data-ttu-id="e522c-123">Annak az erőforráscsoport-csoportnak a neve, amelynek a gyorsítótárát el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="e522c-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="e522c-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e522c-124">-Confirm</span></span>
<span data-ttu-id="e522c-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e522c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e522c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e522c-126">-WhatIf</span></span>
<span data-ttu-id="e522c-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e522c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e522c-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e522c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e522c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e522c-129">CommonParameters</span></span>
<span data-ttu-id="e522c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e522c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e522c-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e522c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e522c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e522c-132">INPUTS</span></span>

### <span data-ttu-id="e522c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e522c-133">System.String</span></span>

## <span data-ttu-id="e522c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e522c-134">OUTPUTS</span></span>

## <span data-ttu-id="e522c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e522c-135">NOTES</span></span>

## <span data-ttu-id="e522c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e522c-136">RELATED LINKS</span></span>
