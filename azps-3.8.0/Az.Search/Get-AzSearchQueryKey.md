---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845818"
---
# <span data-ttu-id="8e20e-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8e20e-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="8e20e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e20e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e20e-103">Az Azure keresési szolgáltatás lekérdezési kulcsát (s) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8e20e-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="8e20e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e20e-104">SYNTAX</span></span>

### <span data-ttu-id="8e20e-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e20e-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e20e-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e20e-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e20e-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e20e-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e20e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e20e-108">DESCRIPTION</span></span>
<span data-ttu-id="8e20e-109">A **Get-AzSearchQueryKey** parancsmag az Azure Search szolgáltatás lekérdezési kulcsát (s) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8e20e-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="8e20e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8e20e-110">EXAMPLES</span></span>

### <span data-ttu-id="8e20e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e20e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="8e20e-112">A példa beolvassa az Azure Search szolgáltatás minden lekérdezési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="8e20e-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="8e20e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e20e-113">PARAMETERS</span></span>

### <span data-ttu-id="8e20e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e20e-114">-DefaultProfile</span></span>
<span data-ttu-id="8e20e-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e20e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e20e-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e20e-116">-ParentObject</span></span>
<span data-ttu-id="8e20e-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="8e20e-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="8e20e-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8e20e-118">-ParentResourceId</span></span>
<span data-ttu-id="8e20e-119">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8e20e-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="8e20e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e20e-120">-ResourceGroupName</span></span>
<span data-ttu-id="8e20e-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8e20e-121">Resource Group name.</span></span>

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

### <span data-ttu-id="8e20e-122">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="8e20e-122">-ServiceName</span></span>
<span data-ttu-id="8e20e-123">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="8e20e-123">Search Service name.</span></span>

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

### <span data-ttu-id="8e20e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e20e-124">CommonParameters</span></span>
<span data-ttu-id="8e20e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e20e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e20e-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e20e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e20e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e20e-127">INPUTS</span></span>

### <span data-ttu-id="8e20e-128">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8e20e-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="8e20e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8e20e-129">System.String</span></span>

## <span data-ttu-id="8e20e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e20e-130">OUTPUTS</span></span>

### <span data-ttu-id="8e20e-131">Microsoft. Azure. commands. Management. Search. models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8e20e-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="8e20e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e20e-132">NOTES</span></span>

## <span data-ttu-id="8e20e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e20e-133">RELATED LINKS</span></span>

[<span data-ttu-id="8e20e-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8e20e-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="8e20e-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8e20e-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)