---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331854"
---
# <span data-ttu-id="6ffba-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="6ffba-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="6ffba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ffba-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffba-103">Frissíti a HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="6ffba-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="6ffba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ffba-104">SYNTAX</span></span>

### <span data-ttu-id="6ffba-105">FlushParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ffba-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffba-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffba-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffba-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffba-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffba-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffba-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ffba-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ffba-109">DESCRIPTION</span></span>
<span data-ttu-id="6ffba-110">Az **Update-AzHpcCache** parancsmag frissíti az Azure HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="6ffba-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="6ffba-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ffba-111">EXAMPLES</span></span>

### <span data-ttu-id="6ffba-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6ffba-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="6ffba-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ffba-113">PARAMETERS</span></span>

### <span data-ttu-id="6ffba-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ffba-114">-AsJob</span></span>
<span data-ttu-id="6ffba-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6ffba-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ffba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffba-116">-DefaultProfile</span></span>
<span data-ttu-id="6ffba-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ffba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ffba-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="6ffba-118">-Flush</span></span>
<span data-ttu-id="6ffba-119">A HPC-gyorsítótár kiürítése.</span><span class="sxs-lookup"><span data-stu-id="6ffba-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ffba-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6ffba-120">-Force</span></span>
<span data-ttu-id="6ffba-121">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ffba-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="6ffba-122">Ez a parancsmag alapértelmezés szerint kérni fogja, hogy erősítse meg a gyorsítótár frissítését.</span><span class="sxs-lookup"><span data-stu-id="6ffba-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="6ffba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ffba-123">-InputObject</span></span>
<span data-ttu-id="6ffba-124">A frissítendve lévő gyorsítótárobjektum.</span><span class="sxs-lookup"><span data-stu-id="6ffba-124">The cache object to update.</span></span>

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

### <span data-ttu-id="6ffba-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6ffba-125">-Name</span></span>
<span data-ttu-id="6ffba-126">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="6ffba-126">Name of cache.</span></span>

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

### <span data-ttu-id="6ffba-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ffba-127">-PassThru</span></span>
<span data-ttu-id="6ffba-128">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="6ffba-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6ffba-129">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6ffba-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6ffba-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffba-130">-ResourceGroupName</span></span>
<span data-ttu-id="6ffba-131">Annak az erőforráscsoportnak a neve, amely alatt frissíteni szeretné a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="6ffba-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="6ffba-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffba-132">-ResourceId</span></span>
<span data-ttu-id="6ffba-133">A gyorsítótár erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6ffba-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="6ffba-134">-Frissítés</span><span class="sxs-lookup"><span data-stu-id="6ffba-134">-Upgrade</span></span>
<span data-ttu-id="6ffba-135">Frissítse a HpcCache-t.</span><span class="sxs-lookup"><span data-stu-id="6ffba-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ffba-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ffba-136">-Confirm</span></span>
<span data-ttu-id="6ffba-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6ffba-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ffba-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ffba-138">-WhatIf</span></span>
<span data-ttu-id="6ffba-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6ffba-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ffba-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ffba-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ffba-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffba-141">CommonParameters</span></span>
<span data-ttu-id="6ffba-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffba-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffba-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ffba-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffba-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ffba-144">INPUTS</span></span>

### <span data-ttu-id="6ffba-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6ffba-145">System.String</span></span>

## <span data-ttu-id="6ffba-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ffba-146">OUTPUTS</span></span>

## <span data-ttu-id="6ffba-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ffba-147">NOTES</span></span>

## <span data-ttu-id="6ffba-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ffba-148">RELATED LINKS</span></span>
