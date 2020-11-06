---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494928"
---
# <span data-ttu-id="25330-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="25330-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="25330-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25330-102">SYNOPSIS</span></span>
<span data-ttu-id="25330-103">Azure Search szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="25330-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25330-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25330-104">SYNTAX</span></span>

### <span data-ttu-id="25330-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25330-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25330-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25330-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25330-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25330-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25330-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="25330-108">DESCRIPTION</span></span>
<span data-ttu-id="25330-109">A **set-AzureRmSearchService** parancsmag az Azure keresési szolgáltatását módosítja.</span><span class="sxs-lookup"><span data-stu-id="25330-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="25330-110">Példák</span><span class="sxs-lookup"><span data-stu-id="25330-110">EXAMPLES</span></span>

### <span data-ttu-id="25330-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25330-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="25330-112">A példa a partíciók számát és az Azure keresési szolgáltatás replikáját 2 értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="25330-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="25330-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25330-113">PARAMETERS</span></span>

### <span data-ttu-id="25330-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25330-114">-DefaultProfile</span></span>
<span data-ttu-id="25330-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25330-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25330-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25330-116">-InputObject</span></span>
<span data-ttu-id="25330-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="25330-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25330-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25330-118">-Name</span></span>
<span data-ttu-id="25330-119">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="25330-119">Search Service name.</span></span>

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

### <span data-ttu-id="25330-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="25330-120">-PartitionCount</span></span>
<span data-ttu-id="25330-121">Keresési szolgáltatás partícióinak száma.</span><span class="sxs-lookup"><span data-stu-id="25330-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="25330-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="25330-122">-ReplicaCount</span></span>
<span data-ttu-id="25330-123">Keresési szolgáltatás replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="25330-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="25330-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25330-124">-ResourceGroupName</span></span>
<span data-ttu-id="25330-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="25330-125">Resource Group name.</span></span>

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

### <span data-ttu-id="25330-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25330-126">-ResourceId</span></span>
<span data-ttu-id="25330-127">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="25330-127">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25330-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="25330-128">-Confirm</span></span>
<span data-ttu-id="25330-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="25330-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25330-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25330-130">-WhatIf</span></span>
<span data-ttu-id="25330-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="25330-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25330-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25330-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25330-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25330-133">CommonParameters</span></span>
<span data-ttu-id="25330-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25330-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25330-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25330-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25330-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25330-136">INPUTS</span></span>

### <span data-ttu-id="25330-137">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="25330-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="25330-138">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25330-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="25330-139">System. String</span><span class="sxs-lookup"><span data-stu-id="25330-139">System.String</span></span>

## <span data-ttu-id="25330-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25330-140">OUTPUTS</span></span>

### <span data-ttu-id="25330-141">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="25330-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="25330-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25330-142">NOTES</span></span>

## <span data-ttu-id="25330-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25330-143">RELATED LINKS</span></span>

[<span data-ttu-id="25330-144">Új – AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="25330-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="25330-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="25330-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="25330-146">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="25330-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
