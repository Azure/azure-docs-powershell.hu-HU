---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 67c5ccb24267825313612cc539f243551ad1894e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669274"
---
# <span data-ttu-id="d37a2-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d37a2-101">New-AzSearchService</span></span>

## <span data-ttu-id="d37a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d37a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d37a2-103">Azure keresési szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d37a2-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="d37a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d37a2-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d37a2-105">DESCRIPTION</span></span>
<span data-ttu-id="d37a2-106">A **New-AzSearchService** parancsmag egy Azure keresési szolgáltatást hoz létre a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="d37a2-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="d37a2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d37a2-107">EXAMPLES</span></span>

### <span data-ttu-id="d37a2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d37a2-108">Example 1</span></span>
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

<span data-ttu-id="d37a2-109">A parancs Azure keresési szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d37a2-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="d37a2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d37a2-110">PARAMETERS</span></span>

### <span data-ttu-id="d37a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37a2-111">-DefaultProfile</span></span>
<span data-ttu-id="d37a2-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d37a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37a2-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="d37a2-113">-HostingMode</span></span>
<span data-ttu-id="d37a2-114">Keresési szolgáltatás üzemeltetése üzemmód.</span><span class="sxs-lookup"><span data-stu-id="d37a2-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="d37a2-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="d37a2-115">-Location</span></span>
<span data-ttu-id="d37a2-116">Keresési szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="d37a2-116">Search Service location.</span></span>

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

### <span data-ttu-id="d37a2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d37a2-117">-Name</span></span>
<span data-ttu-id="d37a2-118">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="d37a2-118">Search Service name.</span></span>

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

### <span data-ttu-id="d37a2-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="d37a2-119">-PartitionCount</span></span>
<span data-ttu-id="d37a2-120">Keresési szolgáltatás partícióinak száma.</span><span class="sxs-lookup"><span data-stu-id="d37a2-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="d37a2-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="d37a2-121">-ReplicaCount</span></span>
<span data-ttu-id="d37a2-122">Keresési szolgáltatás replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="d37a2-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="d37a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="d37a2-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d37a2-124">Resource Group name.</span></span>

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

### <span data-ttu-id="d37a2-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="d37a2-125">-Sku</span></span>
<span data-ttu-id="d37a2-126">Keresési szolgáltatás SKU.</span><span class="sxs-lookup"><span data-stu-id="d37a2-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="d37a2-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d37a2-127">-Confirm</span></span>
<span data-ttu-id="d37a2-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d37a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37a2-129">-WhatIf</span></span>
<span data-ttu-id="d37a2-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d37a2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d37a2-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d37a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37a2-132">CommonParameters</span></span>
<span data-ttu-id="d37a2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d37a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37a2-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37a2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37a2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37a2-135">INPUTS</span></span>

### <span data-ttu-id="d37a2-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="d37a2-136">None</span></span>

## <span data-ttu-id="d37a2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37a2-137">OUTPUTS</span></span>

### <span data-ttu-id="d37a2-138">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d37a2-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="d37a2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d37a2-139">NOTES</span></span>

## <span data-ttu-id="d37a2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d37a2-140">RELATED LINKS</span></span>

[<span data-ttu-id="d37a2-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d37a2-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="d37a2-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d37a2-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="d37a2-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d37a2-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)