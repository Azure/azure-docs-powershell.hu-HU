---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328198"
---
# <span data-ttu-id="15919-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="15919-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="15919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15919-102">SYNOPSIS</span></span>
<span data-ttu-id="15919-103">Frissíti a HPC-gyorsítótár címkéit.</span><span class="sxs-lookup"><span data-stu-id="15919-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="15919-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15919-104">SYNTAX</span></span>

### <span data-ttu-id="15919-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15919-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15919-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15919-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15919-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15919-107">DESCRIPTION</span></span>
<span data-ttu-id="15919-108">A **Set-AzHpcCache** parancsmag frissíti az Azure HPC-gyorsítótár címkéit.</span><span class="sxs-lookup"><span data-stu-id="15919-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="15919-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15919-109">EXAMPLES</span></span>

### <span data-ttu-id="15919-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="15919-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="15919-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15919-111">PARAMETERS</span></span>

### <span data-ttu-id="15919-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15919-112">-AsJob</span></span>
<span data-ttu-id="15919-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="15919-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15919-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15919-114">-DefaultProfile</span></span>
<span data-ttu-id="15919-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15919-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15919-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15919-116">-InputObject</span></span>
<span data-ttu-id="15919-117">A frissítendve lévő gyorsítótárobjektum.</span><span class="sxs-lookup"><span data-stu-id="15919-117">The cache object to update.</span></span>

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

### <span data-ttu-id="15919-118">-Name</span><span class="sxs-lookup"><span data-stu-id="15919-118">-Name</span></span>
<span data-ttu-id="15919-119">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="15919-119">Name of cache.</span></span>

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

### <span data-ttu-id="15919-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15919-120">-ResourceGroupName</span></span>
<span data-ttu-id="15919-121">Annak az erőforráscsoportnak a neve, amely alatt frissíteni szeretné a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="15919-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="15919-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="15919-122">-Tag</span></span>
<span data-ttu-id="15919-123">A HPC cache-hez társítva lévő címkék.</span><span class="sxs-lookup"><span data-stu-id="15919-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15919-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15919-124">-Confirm</span></span>
<span data-ttu-id="15919-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="15919-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15919-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15919-126">-WhatIf</span></span>
<span data-ttu-id="15919-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="15919-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15919-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15919-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15919-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15919-129">CommonParameters</span></span>
<span data-ttu-id="15919-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15919-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15919-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15919-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15919-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15919-132">INPUTS</span></span>

### <span data-ttu-id="15919-133">System.String</span><span class="sxs-lookup"><span data-stu-id="15919-133">System.String</span></span>

### <span data-ttu-id="15919-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="15919-134">System.Int32</span></span>

## <span data-ttu-id="15919-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15919-135">OUTPUTS</span></span>

### <span data-ttu-id="15919-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="15919-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="15919-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15919-137">NOTES</span></span>

## <span data-ttu-id="15919-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15919-138">RELATED LINKS</span></span>
