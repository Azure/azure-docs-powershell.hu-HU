---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493921"
---
# <span data-ttu-id="d04fa-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="d04fa-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="d04fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d04fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d04fa-103">Azure Search szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="d04fa-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d04fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d04fa-104">SYNTAX</span></span>

### <span data-ttu-id="d04fa-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d04fa-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d04fa-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d04fa-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d04fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d04fa-107">DESCRIPTION</span></span>
<span data-ttu-id="d04fa-108">A **Get-AzureRmSearchService** parancsmag megkapja a megadott Azure keresési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d04fa-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="d04fa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d04fa-109">EXAMPLES</span></span>

### <span data-ttu-id="d04fa-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d04fa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="d04fa-111">Azure Search szolgáltatás beszerzése meghatározott paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="d04fa-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="d04fa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d04fa-112">PARAMETERS</span></span>

### <span data-ttu-id="d04fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04fa-113">-DefaultProfile</span></span>
<span data-ttu-id="d04fa-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d04fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d04fa-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d04fa-115">-Name</span></span>
<span data-ttu-id="d04fa-116">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="d04fa-116">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="d04fa-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d04fa-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04fa-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d04fa-119">-ResourceId</span></span>
<span data-ttu-id="d04fa-120">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d04fa-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d04fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04fa-121">CommonParameters</span></span>
<span data-ttu-id="d04fa-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d04fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04fa-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d04fa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04fa-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d04fa-124">INPUTS</span></span>

### <span data-ttu-id="d04fa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d04fa-125">System.String</span></span>

## <span data-ttu-id="d04fa-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d04fa-126">OUTPUTS</span></span>

### <span data-ttu-id="d04fa-127">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d04fa-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="d04fa-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d04fa-128">NOTES</span></span>

## <span data-ttu-id="d04fa-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d04fa-129">RELATED LINKS</span></span>

[<span data-ttu-id="d04fa-130">Új – AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="d04fa-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="d04fa-131">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="d04fa-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="d04fa-132">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="d04fa-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
