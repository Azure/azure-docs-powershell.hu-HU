---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467192"
---
# <span data-ttu-id="66ae3-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="66ae3-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="66ae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="66ae3-103">Hozzon létre egy új lekérdezéskulcsot az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="66ae3-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="66ae3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66ae3-104">SYNTAX</span></span>

### <span data-ttu-id="66ae3-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66ae3-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ae3-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66ae3-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ae3-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66ae3-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ae3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66ae3-108">DESCRIPTION</span></span>
<span data-ttu-id="66ae3-109">A **New-AzSearchQueryKey** parancsmag létrehoz egy új lekérdezéskulcsot az Azure Search Szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="66ae3-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="66ae3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66ae3-110">EXAMPLES</span></span>

### <span data-ttu-id="66ae3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="66ae3-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="66ae3-112">A példa létrehoz egy új lekérdezéskulcsot az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="66ae3-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="66ae3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66ae3-113">PARAMETERS</span></span>

### <span data-ttu-id="66ae3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ae3-114">-DefaultProfile</span></span>
<span data-ttu-id="66ae3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66ae3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66ae3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="66ae3-116">-Name</span></span>
<span data-ttu-id="66ae3-117">Search Service query key name.</span><span class="sxs-lookup"><span data-stu-id="66ae3-117">Search Service query key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ae3-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="66ae3-118">-ParentObject</span></span>
<span data-ttu-id="66ae3-119">Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="66ae3-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66ae3-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="66ae3-120">-ParentResourceId</span></span>
<span data-ttu-id="66ae3-121">Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="66ae3-121">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ae3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ae3-122">-ResourceGroupName</span></span>
<span data-ttu-id="66ae3-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="66ae3-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ae3-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="66ae3-124">-ServiceName</span></span>
<span data-ttu-id="66ae3-125">Keresés a szolgáltatásnévben</span><span class="sxs-lookup"><span data-stu-id="66ae3-125">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ae3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66ae3-126">-Confirm</span></span>
<span data-ttu-id="66ae3-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="66ae3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ae3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ae3-128">-WhatIf</span></span>
<span data-ttu-id="66ae3-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="66ae3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66ae3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66ae3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ae3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ae3-131">CommonParameters</span></span>
<span data-ttu-id="66ae3-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66ae3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ae3-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ae3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ae3-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66ae3-134">INPUTS</span></span>

### <span data-ttu-id="66ae3-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="66ae3-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="66ae3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="66ae3-136">System.String</span></span>

## <span data-ttu-id="66ae3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66ae3-137">OUTPUTS</span></span>

### <span data-ttu-id="66ae3-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="66ae3-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="66ae3-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66ae3-139">NOTES</span></span>

## <span data-ttu-id="66ae3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66ae3-140">RELATED LINKS</span></span>

[<span data-ttu-id="66ae3-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="66ae3-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="66ae3-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="66ae3-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
