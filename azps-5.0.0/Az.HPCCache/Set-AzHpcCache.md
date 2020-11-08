---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187394"
---
# <span data-ttu-id="abd15-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="abd15-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="abd15-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abd15-102">SYNOPSIS</span></span>
<span data-ttu-id="abd15-103">A HPC-gyorsítótárban lévő címkéket frissíti.</span><span class="sxs-lookup"><span data-stu-id="abd15-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="abd15-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abd15-104">SYNTAX</span></span>

### <span data-ttu-id="abd15-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abd15-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abd15-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abd15-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abd15-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="abd15-107">DESCRIPTION</span></span>
<span data-ttu-id="abd15-108">A **set-AzHpcCache** parancsmag egy Azure HPC-gyorsítótárban tárolt címkét frissít.</span><span class="sxs-lookup"><span data-stu-id="abd15-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="abd15-109">Példák</span><span class="sxs-lookup"><span data-stu-id="abd15-109">EXAMPLES</span></span>

### <span data-ttu-id="abd15-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="abd15-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="abd15-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abd15-111">PARAMETERS</span></span>

### <span data-ttu-id="abd15-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abd15-112">-AsJob</span></span>
<span data-ttu-id="abd15-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="abd15-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="abd15-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd15-114">-DefaultProfile</span></span>
<span data-ttu-id="abd15-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abd15-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abd15-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abd15-116">-InputObject</span></span>
<span data-ttu-id="abd15-117">A frissítendő gyorsítótár-objektum.</span><span class="sxs-lookup"><span data-stu-id="abd15-117">The cache object to update.</span></span>

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

### <span data-ttu-id="abd15-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abd15-118">-Name</span></span>
<span data-ttu-id="abd15-119">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="abd15-119">Name of cache.</span></span>

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

### <span data-ttu-id="abd15-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd15-120">-ResourceGroupName</span></span>
<span data-ttu-id="abd15-121">Annak az erőforráscsoport-csoportnak a neve, amely alatt frissíteni szeretné a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="abd15-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="abd15-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="abd15-122">-Tag</span></span>
<span data-ttu-id="abd15-123">A HPC-gyorsítótárral társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="abd15-123">The tags to associate with HPC Cache.</span></span> 

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

### <span data-ttu-id="abd15-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abd15-124">-Confirm</span></span>
<span data-ttu-id="abd15-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abd15-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abd15-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abd15-126">-WhatIf</span></span>
<span data-ttu-id="abd15-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abd15-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abd15-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abd15-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abd15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd15-129">CommonParameters</span></span>
<span data-ttu-id="abd15-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abd15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd15-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="abd15-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd15-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd15-132">INPUTS</span></span>

### <span data-ttu-id="abd15-133">System. String</span><span class="sxs-lookup"><span data-stu-id="abd15-133">System.String</span></span>

### <span data-ttu-id="abd15-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="abd15-134">System.Int32</span></span>

## <span data-ttu-id="abd15-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd15-135">OUTPUTS</span></span>

### <span data-ttu-id="abd15-136">Microsoft. Azure. PowerShell. parancsmagok. HPCCache. models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="abd15-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="abd15-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abd15-137">NOTES</span></span>

## <span data-ttu-id="abd15-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abd15-138">RELATED LINKS</span></span>
