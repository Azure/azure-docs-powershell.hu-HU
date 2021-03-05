---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 2d3fd9d44a06c8538233b1f130010e905055912e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013429"
---
# <span data-ttu-id="efbda-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="efbda-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="efbda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efbda-102">SYNOPSIS</span></span>
<span data-ttu-id="efbda-103">Leállítja a HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="efbda-103">Stops HPC cache.</span></span>

## <span data-ttu-id="efbda-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efbda-104">SYNTAX</span></span>

### <span data-ttu-id="efbda-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efbda-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efbda-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efbda-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efbda-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efbda-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efbda-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efbda-108">DESCRIPTION</span></span>
<span data-ttu-id="efbda-109">A **Stop-AzHpcCache** parancsmag leállítja az Azure HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="efbda-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="efbda-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efbda-110">EXAMPLES</span></span>

### <span data-ttu-id="efbda-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="efbda-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="efbda-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efbda-112">PARAMETERS</span></span>

### <span data-ttu-id="efbda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efbda-113">-DefaultProfile</span></span>
<span data-ttu-id="efbda-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efbda-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efbda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="efbda-115">-Force</span></span>
<span data-ttu-id="efbda-116">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="efbda-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="efbda-117">Ez a parancsmag alapértelmezés szerint megkérdezi, hogy le szeretné-e állítani a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="efbda-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="efbda-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efbda-118">-InputObject</span></span>
<span data-ttu-id="efbda-119">A leállíthatja a gyorsítótárobjektumot.</span><span class="sxs-lookup"><span data-stu-id="efbda-119">The cache object to stop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efbda-120">-Name</span><span class="sxs-lookup"><span data-stu-id="efbda-120">-Name</span></span>
<span data-ttu-id="efbda-121">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="efbda-121">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efbda-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efbda-122">-PassThru</span></span>
<span data-ttu-id="efbda-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="efbda-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="efbda-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="efbda-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efbda-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efbda-125">-ResourceGroupName</span></span>
<span data-ttu-id="efbda-126">Annak az erőforráscsoportnak a neve, amely alatt le szeretné állítani a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="efbda-126">Name of resource group under which you want to stop cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efbda-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efbda-127">-ResourceId</span></span>
<span data-ttu-id="efbda-128">A gyorsítótár erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="efbda-128">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efbda-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efbda-129">-Confirm</span></span>
<span data-ttu-id="efbda-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="efbda-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efbda-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efbda-131">-WhatIf</span></span>
<span data-ttu-id="efbda-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="efbda-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efbda-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efbda-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efbda-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbda-134">CommonParameters</span></span>
<span data-ttu-id="efbda-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efbda-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbda-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efbda-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efbda-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efbda-137">INPUTS</span></span>

### <span data-ttu-id="efbda-138">System.String</span><span class="sxs-lookup"><span data-stu-id="efbda-138">System.String</span></span>

## <span data-ttu-id="efbda-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efbda-139">OUTPUTS</span></span>

## <span data-ttu-id="efbda-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efbda-140">NOTES</span></span>

## <span data-ttu-id="efbda-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efbda-141">RELATED LINKS</span></span>
