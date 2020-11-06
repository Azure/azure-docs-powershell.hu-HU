---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493925"
---
# <span data-ttu-id="5b0e3-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5b0e3-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="5b0e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0e3-103">Az Azure keresési szolgáltatás lekérdezési kulcsát (s) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5b0e3-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b0e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b0e3-104">SYNTAX</span></span>

### <span data-ttu-id="5b0e3-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b0e3-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b0e3-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b0e3-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b0e3-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b0e3-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b0e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b0e3-108">DESCRIPTION</span></span>
<span data-ttu-id="5b0e3-109">A **Get-AzureRmSearchQueryKey** parancsmag az Azure Search szolgáltatás lekérdezési kulcsát (s) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5b0e3-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="5b0e3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5b0e3-110">EXAMPLES</span></span>

### <span data-ttu-id="5b0e3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5b0e3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="5b0e3-112">A példa beolvassa az Azure Search szolgáltatás minden lekérdezési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="5b0e3-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="5b0e3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b0e3-113">PARAMETERS</span></span>

### <span data-ttu-id="5b0e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0e3-114">-DefaultProfile</span></span>
<span data-ttu-id="5b0e3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b0e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b0e3-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5b0e3-116">-ParentObject</span></span>
<span data-ttu-id="5b0e3-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="5b0e3-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="5b0e3-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5b0e3-118">-ParentResourceId</span></span>
<span data-ttu-id="5b0e3-119">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5b0e3-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5b0e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b0e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b0e3-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5b0e3-121">Resource Group name.</span></span>

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

### <span data-ttu-id="5b0e3-122">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="5b0e3-122">-ServiceName</span></span>
<span data-ttu-id="5b0e3-123">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="5b0e3-123">Search Service name.</span></span>

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

### <span data-ttu-id="5b0e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0e3-124">CommonParameters</span></span>
<span data-ttu-id="5b0e3-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b0e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0e3-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b0e3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0e3-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b0e3-127">INPUTS</span></span>

### <span data-ttu-id="5b0e3-128">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5b0e3-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="5b0e3-129">Paraméterek: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b0e3-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="5b0e3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5b0e3-130">System.String</span></span>

## <span data-ttu-id="5b0e3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b0e3-131">OUTPUTS</span></span>

### <span data-ttu-id="5b0e3-132">Microsoft. Azure. commands. Management. Search. models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5b0e3-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="5b0e3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b0e3-133">NOTES</span></span>

## <span data-ttu-id="5b0e3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b0e3-134">RELATED LINKS</span></span>

[<span data-ttu-id="5b0e3-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5b0e3-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="5b0e3-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5b0e3-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
