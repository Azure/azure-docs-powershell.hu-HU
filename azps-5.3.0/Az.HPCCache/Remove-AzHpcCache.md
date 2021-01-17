---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466040"
---
# <span data-ttu-id="073d8-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="073d8-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="073d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="073d8-102">SYNOPSIS</span></span>
<span data-ttu-id="073d8-103">Eltávolítja a HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="073d8-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="073d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="073d8-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="073d8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="073d8-105">DESCRIPTION</span></span>
<span data-ttu-id="073d8-106">A **Remove-AzHpcCache** parancsmag eltávolítja az Azure HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="073d8-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="073d8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="073d8-107">EXAMPLES</span></span>

### <span data-ttu-id="073d8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="073d8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="073d8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="073d8-109">PARAMETERS</span></span>

### <span data-ttu-id="073d8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="073d8-110">-AsJob</span></span>
<span data-ttu-id="073d8-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="073d8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="073d8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073d8-112">-DefaultProfile</span></span>
<span data-ttu-id="073d8-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="073d8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="073d8-114">-Force</span><span class="sxs-lookup"><span data-stu-id="073d8-114">-Force</span></span>
<span data-ttu-id="073d8-115">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="073d8-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="073d8-116">Ez a parancsmag alapértelmezés szerint kérni fogja, hogy erősítse meg a gyorsítótár eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="073d8-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="073d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="073d8-117">-Name</span></span>
<span data-ttu-id="073d8-118">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="073d8-118">Name of cache.</span></span>

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

### <span data-ttu-id="073d8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="073d8-119">-PassThru</span></span>
<span data-ttu-id="073d8-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="073d8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="073d8-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="073d8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="073d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="073d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="073d8-123">Annak az erőforráscsoportnak a neve, amely alatt el szeretné távolítani a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="073d8-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="073d8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="073d8-124">-Confirm</span></span>
<span data-ttu-id="073d8-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="073d8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="073d8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="073d8-126">-WhatIf</span></span>
<span data-ttu-id="073d8-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="073d8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="073d8-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="073d8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="073d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073d8-129">CommonParameters</span></span>
<span data-ttu-id="073d8-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="073d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073d8-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="073d8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073d8-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="073d8-132">INPUTS</span></span>

### <span data-ttu-id="073d8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="073d8-133">System.String</span></span>

## <span data-ttu-id="073d8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="073d8-134">OUTPUTS</span></span>

## <span data-ttu-id="073d8-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="073d8-135">NOTES</span></span>

## <span data-ttu-id="073d8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="073d8-136">RELATED LINKS</span></span>
