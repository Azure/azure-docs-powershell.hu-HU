---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 4836a7c016a86ad5fcbb1c926bc27f43215a44f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838094"
---
# <span data-ttu-id="fd3b0-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fd3b0-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="fd3b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3b0-103">Új lekérdezési kulcs létrehozása az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="fd3b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd3b0-104">SYNTAX</span></span>

### <span data-ttu-id="fd3b0-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd3b0-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd3b0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd3b0-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd3b0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd3b0-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd3b0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd3b0-108">DESCRIPTION</span></span>
<span data-ttu-id="fd3b0-109">A **New-AzSearchQueryKey** parancsmag új lekérdezési kulcsot hoz létre az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="fd3b0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fd3b0-110">EXAMPLES</span></span>

### <span data-ttu-id="fd3b0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd3b0-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="fd3b0-112">A példa létrehoz egy új lekérdezési kulcsot az Azure Search szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="fd3b0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd3b0-113">PARAMETERS</span></span>

### <span data-ttu-id="fd3b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3b0-114">-DefaultProfile</span></span>
<span data-ttu-id="fd3b0-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd3b0-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd3b0-116">-Name</span></span>
<span data-ttu-id="fd3b0-117">Keresési szolgáltatás lekérdezési kulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="fd3b0-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fd3b0-118">-ParentObject</span></span>
<span data-ttu-id="fd3b0-119">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="fd3b0-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fd3b0-120">-ParentResourceId</span></span>
<span data-ttu-id="fd3b0-121">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fd3b0-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="fd3b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd3b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd3b0-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-123">Resource Group name.</span></span>

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

### <span data-ttu-id="fd3b0-124">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="fd3b0-124">-ServiceName</span></span>
<span data-ttu-id="fd3b0-125">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="fd3b0-125">Search Service name.</span></span>

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

### <span data-ttu-id="fd3b0-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd3b0-126">-Confirm</span></span>
<span data-ttu-id="fd3b0-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd3b0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd3b0-128">-WhatIf</span></span>
<span data-ttu-id="fd3b0-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd3b0-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd3b0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd3b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3b0-131">CommonParameters</span></span>
<span data-ttu-id="fd3b0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd3b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3b0-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd3b0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3b0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd3b0-134">INPUTS</span></span>

### <span data-ttu-id="fd3b0-135">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="fd3b0-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="fd3b0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fd3b0-136">System.String</span></span>

## <span data-ttu-id="fd3b0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd3b0-137">OUTPUTS</span></span>

### <span data-ttu-id="fd3b0-138">Microsoft. Azure. commands. Management. Search. models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fd3b0-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="fd3b0-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd3b0-139">NOTES</span></span>

## <span data-ttu-id="fd3b0-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd3b0-140">RELATED LINKS</span></span>

[<span data-ttu-id="fd3b0-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fd3b0-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="fd3b0-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fd3b0-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
