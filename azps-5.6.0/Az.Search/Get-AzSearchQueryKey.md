---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9bd662c5164660f6bc330e3b2ee2eced2893dbce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937361"
---
# <span data-ttu-id="75cbe-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="75cbe-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="75cbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="75cbe-103">Lekérdezi az Azure Kognitív keresés szolgáltatás lekérdezéskulcsát.</span><span class="sxs-lookup"><span data-stu-id="75cbe-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="75cbe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75cbe-104">SYNTAX</span></span>

### <span data-ttu-id="75cbe-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75cbe-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75cbe-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75cbe-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75cbe-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75cbe-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75cbe-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75cbe-108">DESCRIPTION</span></span>
<span data-ttu-id="75cbe-109">A **Get-AzSearchQueryKey** parancsmag lekérdezi az Azure Kognitív keresés szolgáltatás lekérdezéskulcsát.</span><span class="sxs-lookup"><span data-stu-id="75cbe-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="75cbe-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75cbe-110">EXAMPLES</span></span>

### <span data-ttu-id="75cbe-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="75cbe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="75cbe-112">A példa az Azure Kognitív keresési szolgáltatás összes lekérdezéskulcsát beszeri.</span><span class="sxs-lookup"><span data-stu-id="75cbe-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="75cbe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cbe-113">PARAMETERS</span></span>

### <span data-ttu-id="75cbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cbe-114">-DefaultProfile</span></span>
<span data-ttu-id="75cbe-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75cbe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75cbe-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="75cbe-116">-ParentObject</span></span>
<span data-ttu-id="75cbe-117">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="75cbe-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="75cbe-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="75cbe-118">-ParentResourceId</span></span>
<span data-ttu-id="75cbe-119">Azure Kognitív keresési szolgáltatás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="75cbe-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="75cbe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75cbe-120">-ResourceGroupName</span></span>
<span data-ttu-id="75cbe-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="75cbe-121">Resource Group name.</span></span>

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

### <span data-ttu-id="75cbe-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="75cbe-122">-ServiceName</span></span>
<span data-ttu-id="75cbe-123">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="75cbe-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="75cbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cbe-124">CommonParameters</span></span>
<span data-ttu-id="75cbe-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cbe-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75cbe-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cbe-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75cbe-127">INPUTS</span></span>

### <span data-ttu-id="75cbe-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="75cbe-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="75cbe-129">System.String</span><span class="sxs-lookup"><span data-stu-id="75cbe-129">System.String</span></span>

## <span data-ttu-id="75cbe-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75cbe-130">OUTPUTS</span></span>

### <span data-ttu-id="75cbe-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="75cbe-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="75cbe-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75cbe-132">NOTES</span></span>

## <span data-ttu-id="75cbe-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75cbe-133">RELATED LINKS</span></span>

[<span data-ttu-id="75cbe-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="75cbe-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="75cbe-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="75cbe-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)