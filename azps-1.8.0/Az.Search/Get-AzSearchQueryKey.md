---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9283fb0a2fd366029a5ca2bc618daf7ad8a3de3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669280"
---
# <span data-ttu-id="fca98-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fca98-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="fca98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fca98-102">SYNOPSIS</span></span>
<span data-ttu-id="fca98-103">Az Azure keresési szolgáltatás lekérdezési kulcsát (s) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fca98-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="fca98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fca98-104">SYNTAX</span></span>

### <span data-ttu-id="fca98-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fca98-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fca98-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca98-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fca98-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca98-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fca98-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fca98-108">DESCRIPTION</span></span>
<span data-ttu-id="fca98-109">A **Get-AzSearchQueryKey** parancsmag az Azure Search szolgáltatás lekérdezési kulcsát (s) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fca98-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="fca98-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fca98-110">EXAMPLES</span></span>

### <span data-ttu-id="fca98-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fca98-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="fca98-112">A példa beolvassa az Azure Search szolgáltatás minden lekérdezési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="fca98-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="fca98-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fca98-113">PARAMETERS</span></span>

### <span data-ttu-id="fca98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca98-114">-DefaultProfile</span></span>
<span data-ttu-id="fca98-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fca98-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fca98-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fca98-116">-ParentObject</span></span>
<span data-ttu-id="fca98-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="fca98-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="fca98-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fca98-118">-ParentResourceId</span></span>
<span data-ttu-id="fca98-119">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fca98-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="fca98-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca98-120">-ResourceGroupName</span></span>
<span data-ttu-id="fca98-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fca98-121">Resource Group name.</span></span>

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

### <span data-ttu-id="fca98-122">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="fca98-122">-ServiceName</span></span>
<span data-ttu-id="fca98-123">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="fca98-123">Search Service name.</span></span>

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

### <span data-ttu-id="fca98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca98-124">CommonParameters</span></span>
<span data-ttu-id="fca98-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fca98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca98-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca98-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca98-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fca98-127">INPUTS</span></span>

### <span data-ttu-id="fca98-128">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="fca98-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="fca98-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fca98-129">System.String</span></span>

## <span data-ttu-id="fca98-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fca98-130">OUTPUTS</span></span>

### <span data-ttu-id="fca98-131">Microsoft. Azure. commands. Management. Search. models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fca98-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="fca98-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fca98-132">NOTES</span></span>

## <span data-ttu-id="fca98-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fca98-133">RELATED LINKS</span></span>

[<span data-ttu-id="fca98-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fca98-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="fca98-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fca98-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)