---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183331"
---
# <span data-ttu-id="7a813-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7a813-101">New-AzSearchService</span></span>

## <span data-ttu-id="7a813-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a813-102">SYNOPSIS</span></span>
<span data-ttu-id="7a813-103">Azure keresési szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7a813-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="7a813-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a813-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a813-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a813-105">DESCRIPTION</span></span>
<span data-ttu-id="7a813-106">A **New-AzSearchService** parancsmag egy Azure keresési szolgáltatást hoz létre a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="7a813-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="7a813-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a813-107">EXAMPLES</span></span>

### <span data-ttu-id="7a813-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7a813-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="7a813-109">A parancs Azure keresési szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7a813-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="7a813-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a813-110">PARAMETERS</span></span>

### <span data-ttu-id="7a813-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a813-111">-DefaultProfile</span></span>
<span data-ttu-id="7a813-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a813-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a813-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="7a813-113">-HostingMode</span></span>
<span data-ttu-id="7a813-114">Keresési szolgáltatás üzemeltetése üzemmód.</span><span class="sxs-lookup"><span data-stu-id="7a813-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a813-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="7a813-115">-Location</span></span>
<span data-ttu-id="7a813-116">Keresési szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="7a813-116">Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a813-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a813-117">-Name</span></span>
<span data-ttu-id="7a813-118">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="7a813-118">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a813-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="7a813-119">-PartitionCount</span></span>
<span data-ttu-id="7a813-120">Keresési szolgáltatás partícióinak száma.</span><span class="sxs-lookup"><span data-stu-id="7a813-120">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a813-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7a813-121">-ReplicaCount</span></span>
<span data-ttu-id="7a813-122">Keresési szolgáltatás replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="7a813-122">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a813-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a813-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a813-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7a813-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a813-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="7a813-125">-Sku</span></span>
<span data-ttu-id="7a813-126">Keresési szolgáltatás SKU.</span><span class="sxs-lookup"><span data-stu-id="7a813-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a813-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a813-127">-Confirm</span></span>
<span data-ttu-id="7a813-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a813-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a813-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a813-129">-WhatIf</span></span>
<span data-ttu-id="7a813-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a813-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a813-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a813-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a813-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a813-132">CommonParameters</span></span>
<span data-ttu-id="7a813-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a813-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a813-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a813-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a813-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a813-135">INPUTS</span></span>

### <span data-ttu-id="7a813-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="7a813-136">None</span></span>

## <span data-ttu-id="7a813-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a813-137">OUTPUTS</span></span>

### <span data-ttu-id="7a813-138">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7a813-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="7a813-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a813-139">NOTES</span></span>

## <span data-ttu-id="7a813-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a813-140">RELATED LINKS</span></span>

[<span data-ttu-id="7a813-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7a813-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="7a813-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7a813-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="7a813-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7a813-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)