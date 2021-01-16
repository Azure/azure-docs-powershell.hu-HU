---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333858"
---
# <span data-ttu-id="89712-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="89712-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="89712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89712-102">SYNOPSIS</span></span>
<span data-ttu-id="89712-103">Hozzon létre egy új lekérdezéskulcsot az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="89712-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="89712-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89712-104">SYNTAX</span></span>

### <span data-ttu-id="89712-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89712-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89712-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89712-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89712-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89712-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89712-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89712-108">DESCRIPTION</span></span>
<span data-ttu-id="89712-109">A **New-AzSearchQueryKey** parancsmag létrehoz egy új lekérdezéskulcsot az Azure Search Szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="89712-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="89712-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89712-110">EXAMPLES</span></span>

### <span data-ttu-id="89712-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="89712-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="89712-112">A példa létrehoz egy új lekérdezéskulcsot az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="89712-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="89712-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89712-113">PARAMETERS</span></span>

### <span data-ttu-id="89712-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89712-114">-DefaultProfile</span></span>
<span data-ttu-id="89712-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89712-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89712-116">-Name</span><span class="sxs-lookup"><span data-stu-id="89712-116">-Name</span></span>
<span data-ttu-id="89712-117">Search Service query key name.</span><span class="sxs-lookup"><span data-stu-id="89712-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="89712-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="89712-118">-ParentObject</span></span>
<span data-ttu-id="89712-119">Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="89712-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="89712-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="89712-120">-ParentResourceId</span></span>
<span data-ttu-id="89712-121">Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="89712-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="89712-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89712-122">-ResourceGroupName</span></span>
<span data-ttu-id="89712-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89712-123">Resource Group name.</span></span>

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

### <span data-ttu-id="89712-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="89712-124">-ServiceName</span></span>
<span data-ttu-id="89712-125">Keresés a szolgáltatásnévben</span><span class="sxs-lookup"><span data-stu-id="89712-125">Search Service name.</span></span>

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

### <span data-ttu-id="89712-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89712-126">-Confirm</span></span>
<span data-ttu-id="89712-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89712-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89712-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89712-128">-WhatIf</span></span>
<span data-ttu-id="89712-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89712-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89712-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89712-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89712-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89712-131">CommonParameters</span></span>
<span data-ttu-id="89712-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89712-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89712-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89712-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89712-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89712-134">INPUTS</span></span>

### <span data-ttu-id="89712-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="89712-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="89712-136">System.String</span><span class="sxs-lookup"><span data-stu-id="89712-136">System.String</span></span>

## <span data-ttu-id="89712-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89712-137">OUTPUTS</span></span>

### <span data-ttu-id="89712-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="89712-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="89712-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89712-139">NOTES</span></span>

## <span data-ttu-id="89712-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89712-140">RELATED LINKS</span></span>

[<span data-ttu-id="89712-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="89712-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="89712-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="89712-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
