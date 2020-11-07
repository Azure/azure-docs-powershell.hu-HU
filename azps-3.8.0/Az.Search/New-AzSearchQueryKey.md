---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846777"
---
# <span data-ttu-id="ca0df-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="ca0df-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="ca0df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca0df-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0df-103">Új lekérdezési kulcs létrehozása az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ca0df-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="ca0df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca0df-104">SYNTAX</span></span>

### <span data-ttu-id="ca0df-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca0df-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca0df-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca0df-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca0df-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca0df-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca0df-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca0df-108">DESCRIPTION</span></span>
<span data-ttu-id="ca0df-109">A **New-AzSearchQueryKey** parancsmag új lekérdezési kulcsot hoz létre az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ca0df-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="ca0df-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ca0df-110">EXAMPLES</span></span>

### <span data-ttu-id="ca0df-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca0df-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="ca0df-112">A példa létrehoz egy új lekérdezési kulcsot az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ca0df-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="ca0df-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca0df-113">PARAMETERS</span></span>

### <span data-ttu-id="ca0df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0df-114">-DefaultProfile</span></span>
<span data-ttu-id="ca0df-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca0df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca0df-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca0df-116">-Name</span></span>
<span data-ttu-id="ca0df-117">Keresési szolgáltatás lekérdezési kulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="ca0df-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="ca0df-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ca0df-118">-ParentObject</span></span>
<span data-ttu-id="ca0df-119">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="ca0df-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="ca0df-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ca0df-120">-ParentResourceId</span></span>
<span data-ttu-id="ca0df-121">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ca0df-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="ca0df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0df-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca0df-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ca0df-123">Resource Group name.</span></span>

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

### <span data-ttu-id="ca0df-124">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="ca0df-124">-ServiceName</span></span>
<span data-ttu-id="ca0df-125">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="ca0df-125">Search Service name.</span></span>

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

### <span data-ttu-id="ca0df-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca0df-126">-Confirm</span></span>
<span data-ttu-id="ca0df-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca0df-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca0df-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca0df-128">-WhatIf</span></span>
<span data-ttu-id="ca0df-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca0df-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca0df-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca0df-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca0df-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0df-131">CommonParameters</span></span>
<span data-ttu-id="ca0df-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca0df-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0df-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca0df-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0df-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca0df-134">INPUTS</span></span>

### <span data-ttu-id="ca0df-135">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="ca0df-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="ca0df-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ca0df-136">System.String</span></span>

## <span data-ttu-id="ca0df-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca0df-137">OUTPUTS</span></span>

### <span data-ttu-id="ca0df-138">Microsoft. Azure. commands. Management. Search. models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="ca0df-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="ca0df-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca0df-139">NOTES</span></span>

## <span data-ttu-id="ca0df-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca0df-140">RELATED LINKS</span></span>

[<span data-ttu-id="ca0df-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="ca0df-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="ca0df-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="ca0df-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
