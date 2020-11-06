---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500128"
---
# <span data-ttu-id="fb6a9-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fb6a9-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="fb6a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6a9-103">Új lekérdezési kulcs létrehozása az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb6a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb6a9-104">SYNTAX</span></span>

### <span data-ttu-id="fb6a9-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb6a9-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb6a9-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a9-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb6a9-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb6a9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb6a9-108">DESCRIPTION</span></span>
<span data-ttu-id="fb6a9-109">A **New-AzureRmSearchQueryKey** parancsmag új lekérdezési kulcsot hoz létre az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="fb6a9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fb6a9-110">EXAMPLES</span></span>

### <span data-ttu-id="fb6a9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb6a9-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="fb6a9-112">A példa létrehoz egy új lekérdezési kulcsot az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="fb6a9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb6a9-113">PARAMETERS</span></span>

### <span data-ttu-id="fb6a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6a9-114">-DefaultProfile</span></span>
<span data-ttu-id="fb6a9-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6a9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb6a9-116">-Name</span></span>
<span data-ttu-id="fb6a9-117">Keresési szolgáltatás lekérdezési kulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="fb6a9-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb6a9-118">-ParentObject</span></span>
<span data-ttu-id="fb6a9-119">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="fb6a9-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fb6a9-120">-ParentResourceId</span></span>
<span data-ttu-id="fb6a9-121">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fb6a9-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="fb6a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb6a9-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-123">Resource Group name.</span></span>

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

### <span data-ttu-id="fb6a9-124">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="fb6a9-124">-ServiceName</span></span>
<span data-ttu-id="fb6a9-125">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="fb6a9-125">Search Service name.</span></span>

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

### <span data-ttu-id="fb6a9-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb6a9-126">-Confirm</span></span>
<span data-ttu-id="fb6a9-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6a9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6a9-128">-WhatIf</span></span>
<span data-ttu-id="fb6a9-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb6a9-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6a9-131">CommonParameters</span></span>
<span data-ttu-id="fb6a9-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb6a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6a9-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6a9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6a9-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb6a9-134">INPUTS</span></span>

### <span data-ttu-id="fb6a9-135">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="fb6a9-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="fb6a9-136">Paraméterek: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fb6a9-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="fb6a9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fb6a9-137">System.String</span></span>

## <span data-ttu-id="fb6a9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb6a9-138">OUTPUTS</span></span>

### <span data-ttu-id="fb6a9-139">Microsoft. Azure. commands. Management. Search. models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fb6a9-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="fb6a9-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb6a9-140">NOTES</span></span>

## <span data-ttu-id="fb6a9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb6a9-141">RELATED LINKS</span></span>

[<span data-ttu-id="fb6a9-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fb6a9-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="fb6a9-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fb6a9-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
