---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013483"
---
# <span data-ttu-id="cfc35-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="cfc35-101">Set-AzSearchService</span></span>

## <span data-ttu-id="cfc35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfc35-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc35-103">Azure Search szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="cfc35-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="cfc35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfc35-104">SYNTAX</span></span>

### <span data-ttu-id="cfc35-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cfc35-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc35-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfc35-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc35-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfc35-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfc35-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfc35-108">DESCRIPTION</span></span>
<span data-ttu-id="cfc35-109">A **set-AzSearchService** parancsmag az Azure keresési szolgáltatását módosítja.</span><span class="sxs-lookup"><span data-stu-id="cfc35-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="cfc35-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cfc35-110">EXAMPLES</span></span>

### <span data-ttu-id="cfc35-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cfc35-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="cfc35-112">A példa a partíciók számát és az Azure keresési szolgáltatás replikáját 2 értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="cfc35-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="cfc35-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfc35-113">PARAMETERS</span></span>

### <span data-ttu-id="cfc35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc35-114">-DefaultProfile</span></span>
<span data-ttu-id="cfc35-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfc35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc35-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfc35-116">-InputObject</span></span>
<span data-ttu-id="cfc35-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="cfc35-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="cfc35-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cfc35-118">-Name</span></span>
<span data-ttu-id="cfc35-119">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="cfc35-119">Search Service name.</span></span>

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

### <span data-ttu-id="cfc35-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="cfc35-120">-PartitionCount</span></span>
<span data-ttu-id="cfc35-121">Keresési szolgáltatás partícióinak száma.</span><span class="sxs-lookup"><span data-stu-id="cfc35-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="cfc35-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="cfc35-122">-ReplicaCount</span></span>
<span data-ttu-id="cfc35-123">Keresési szolgáltatás replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="cfc35-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="cfc35-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfc35-124">-ResourceGroupName</span></span>
<span data-ttu-id="cfc35-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="cfc35-125">Resource Group name.</span></span>

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

### <span data-ttu-id="cfc35-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfc35-126">-ResourceId</span></span>
<span data-ttu-id="cfc35-127">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cfc35-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="cfc35-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cfc35-128">-Confirm</span></span>
<span data-ttu-id="cfc35-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfc35-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfc35-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc35-130">-WhatIf</span></span>
<span data-ttu-id="cfc35-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cfc35-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfc35-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfc35-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfc35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc35-133">CommonParameters</span></span>
<span data-ttu-id="cfc35-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfc35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc35-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc35-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc35-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfc35-136">INPUTS</span></span>

### <span data-ttu-id="cfc35-137">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="cfc35-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="cfc35-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cfc35-138">System.String</span></span>

## <span data-ttu-id="cfc35-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfc35-139">OUTPUTS</span></span>

### <span data-ttu-id="cfc35-140">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="cfc35-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="cfc35-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfc35-141">NOTES</span></span>

## <span data-ttu-id="cfc35-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfc35-142">RELATED LINKS</span></span>

[<span data-ttu-id="cfc35-143">Új – AzSearchService</span><span class="sxs-lookup"><span data-stu-id="cfc35-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="cfc35-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="cfc35-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="cfc35-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="cfc35-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)