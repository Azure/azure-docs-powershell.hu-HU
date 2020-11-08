---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194861"
---
# <span data-ttu-id="4a3a6-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="4a3a6-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="4a3a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3a6-103">Az Azure keresési szolgáltatás lekérdezési kulcsát (s) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4a3a6-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="4a3a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a3a6-104">SYNTAX</span></span>

### <span data-ttu-id="4a3a6-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a3a6-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a3a6-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a3a6-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a3a6-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a3a6-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a3a6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a3a6-108">DESCRIPTION</span></span>
<span data-ttu-id="4a3a6-109">A **Get-AzSearchQueryKey** parancsmag az Azure Search szolgáltatás lekérdezési kulcsát (s) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4a3a6-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="4a3a6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4a3a6-110">EXAMPLES</span></span>

### <span data-ttu-id="4a3a6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4a3a6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="4a3a6-112">A példa beolvassa az Azure Search szolgáltatás minden lekérdezési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="4a3a6-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="4a3a6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a3a6-113">PARAMETERS</span></span>

### <span data-ttu-id="4a3a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3a6-114">-DefaultProfile</span></span>
<span data-ttu-id="4a3a6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a3a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a3a6-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4a3a6-116">-ParentObject</span></span>
<span data-ttu-id="4a3a6-117">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="4a3a6-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="4a3a6-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4a3a6-118">-ParentResourceId</span></span>
<span data-ttu-id="4a3a6-119">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4a3a6-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="4a3a6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a3a6-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a3a6-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4a3a6-121">Resource Group name.</span></span>

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

### <span data-ttu-id="4a3a6-122">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="4a3a6-122">-ServiceName</span></span>
<span data-ttu-id="4a3a6-123">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="4a3a6-123">Search Service name.</span></span>

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

### <span data-ttu-id="4a3a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3a6-124">CommonParameters</span></span>
<span data-ttu-id="4a3a6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a3a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3a6-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a3a6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3a6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a3a6-127">INPUTS</span></span>

### <span data-ttu-id="4a3a6-128">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4a3a6-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="4a3a6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4a3a6-129">System.String</span></span>

## <span data-ttu-id="4a3a6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a3a6-130">OUTPUTS</span></span>

### <span data-ttu-id="4a3a6-131">Microsoft. Azure. commands. Management. Search. models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="4a3a6-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="4a3a6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a3a6-132">NOTES</span></span>

## <span data-ttu-id="4a3a6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a3a6-133">RELATED LINKS</span></span>

[<span data-ttu-id="4a3a6-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="4a3a6-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="4a3a6-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="4a3a6-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)