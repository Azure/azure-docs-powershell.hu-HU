---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467702"
---
# <span data-ttu-id="28a0e-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="28a0e-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="28a0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="28a0e-103">Leállítja a HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="28a0e-103">Stops HPC cache.</span></span>

## <span data-ttu-id="28a0e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28a0e-104">SYNTAX</span></span>

### <span data-ttu-id="28a0e-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28a0e-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a0e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28a0e-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a0e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28a0e-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28a0e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28a0e-108">DESCRIPTION</span></span>
<span data-ttu-id="28a0e-109">A **Stop-AzHpcCache** parancsmag leállítja az Azure HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="28a0e-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="28a0e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28a0e-110">EXAMPLES</span></span>

### <span data-ttu-id="28a0e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="28a0e-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="28a0e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28a0e-112">PARAMETERS</span></span>

### <span data-ttu-id="28a0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a0e-113">-DefaultProfile</span></span>
<span data-ttu-id="28a0e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28a0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a0e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="28a0e-115">-Force</span></span>
<span data-ttu-id="28a0e-116">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28a0e-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="28a0e-117">Ez a parancsmag alapértelmezés szerint megkérdezi, hogy le szeretné-e állítani a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="28a0e-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="28a0e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a0e-118">-InputObject</span></span>
<span data-ttu-id="28a0e-119">A leállíthatja a gyorsítótárobjektumot.</span><span class="sxs-lookup"><span data-stu-id="28a0e-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="28a0e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="28a0e-120">-Name</span></span>
<span data-ttu-id="28a0e-121">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="28a0e-121">Name of cache.</span></span>

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

### <span data-ttu-id="28a0e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28a0e-122">-PassThru</span></span>
<span data-ttu-id="28a0e-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="28a0e-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28a0e-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="28a0e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28a0e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a0e-125">-ResourceGroupName</span></span>
<span data-ttu-id="28a0e-126">Annak az erőforráscsoportnak a neve, amely alatt le szeretné állítani a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="28a0e-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="28a0e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28a0e-127">-ResourceId</span></span>
<span data-ttu-id="28a0e-128">A gyorsítótár erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="28a0e-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="28a0e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28a0e-129">-Confirm</span></span>
<span data-ttu-id="28a0e-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="28a0e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28a0e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28a0e-131">-WhatIf</span></span>
<span data-ttu-id="28a0e-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="28a0e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28a0e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28a0e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28a0e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a0e-134">CommonParameters</span></span>
<span data-ttu-id="28a0e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a0e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a0e-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28a0e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a0e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28a0e-137">INPUTS</span></span>

### <span data-ttu-id="28a0e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="28a0e-138">System.String</span></span>

## <span data-ttu-id="28a0e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28a0e-139">OUTPUTS</span></span>

## <span data-ttu-id="28a0e-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28a0e-140">NOTES</span></span>

## <span data-ttu-id="28a0e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28a0e-141">RELATED LINKS</span></span>
