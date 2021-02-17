---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147818"
---
# <span data-ttu-id="94402-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="94402-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="94402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94402-102">SYNOPSIS</span></span>
<span data-ttu-id="94402-103">Elindítja a HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="94402-103">Starts HPC cache.</span></span>

## <span data-ttu-id="94402-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94402-104">SYNTAX</span></span>

### <span data-ttu-id="94402-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94402-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94402-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94402-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94402-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94402-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94402-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94402-108">DESCRIPTION</span></span>
<span data-ttu-id="94402-109">A **Start-AzHpcCache** parancsmag elindít egy Azure HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="94402-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="94402-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94402-110">EXAMPLES</span></span>

### <span data-ttu-id="94402-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="94402-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="94402-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94402-112">PARAMETERS</span></span>

### <span data-ttu-id="94402-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94402-113">-AsJob</span></span>
<span data-ttu-id="94402-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="94402-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94402-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94402-115">-DefaultProfile</span></span>
<span data-ttu-id="94402-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94402-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94402-117">-Force</span><span class="sxs-lookup"><span data-stu-id="94402-117">-Force</span></span>
<span data-ttu-id="94402-118">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94402-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="94402-119">Ez a parancsmag alapértelmezés szerint megkérdezi, hogy szeretné-e elindítani a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="94402-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="94402-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94402-120">-InputObject</span></span>
<span data-ttu-id="94402-121">A elindított gyorsítótárobjektum.</span><span class="sxs-lookup"><span data-stu-id="94402-121">The cache object to start.</span></span>

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

### <span data-ttu-id="94402-122">-Name</span><span class="sxs-lookup"><span data-stu-id="94402-122">-Name</span></span>
<span data-ttu-id="94402-123">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="94402-123">Name of cache.</span></span>

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

### <span data-ttu-id="94402-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94402-124">-PassThru</span></span>
<span data-ttu-id="94402-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="94402-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94402-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="94402-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94402-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94402-127">-ResourceGroupName</span></span>
<span data-ttu-id="94402-128">Annak az erőforráscsoportnak a neve, amely alatt el szeretné kezdeni a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="94402-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="94402-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94402-129">-ResourceId</span></span>
<span data-ttu-id="94402-130">A gyorsítótár erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="94402-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="94402-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94402-131">-Confirm</span></span>
<span data-ttu-id="94402-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="94402-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94402-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94402-133">-WhatIf</span></span>
<span data-ttu-id="94402-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="94402-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94402-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94402-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94402-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94402-136">CommonParameters</span></span>
<span data-ttu-id="94402-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94402-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94402-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94402-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94402-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94402-139">INPUTS</span></span>

### <span data-ttu-id="94402-140">System.String</span><span class="sxs-lookup"><span data-stu-id="94402-140">System.String</span></span>

## <span data-ttu-id="94402-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94402-141">OUTPUTS</span></span>

## <span data-ttu-id="94402-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94402-142">NOTES</span></span>

## <span data-ttu-id="94402-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94402-143">RELATED LINKS</span></span>
