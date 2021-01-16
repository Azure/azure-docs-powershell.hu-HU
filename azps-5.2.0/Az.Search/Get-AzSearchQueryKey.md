---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333870"
---
# <span data-ttu-id="dccaa-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="dccaa-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="dccaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dccaa-102">SYNOPSIS</span></span>
<span data-ttu-id="dccaa-103">Lekérdezi az Azure Search szolgáltatás lekérdezéskulcsát.</span><span class="sxs-lookup"><span data-stu-id="dccaa-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="dccaa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dccaa-104">SYNTAX</span></span>

### <span data-ttu-id="dccaa-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dccaa-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dccaa-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dccaa-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dccaa-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dccaa-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dccaa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dccaa-108">DESCRIPTION</span></span>
<span data-ttu-id="dccaa-109">A **Get-AzSearchQueryKey** parancsmag lekérdezi az Azure Search szolgáltatás lekérdezéskulcsát.</span><span class="sxs-lookup"><span data-stu-id="dccaa-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="dccaa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dccaa-110">EXAMPLES</span></span>

### <span data-ttu-id="dccaa-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="dccaa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="dccaa-112">A példa az Azure Search szolgáltatás összes lekérdezéskulcsát beszerszi.</span><span class="sxs-lookup"><span data-stu-id="dccaa-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="dccaa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dccaa-113">PARAMETERS</span></span>

### <span data-ttu-id="dccaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccaa-114">-DefaultProfile</span></span>
<span data-ttu-id="dccaa-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dccaa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dccaa-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dccaa-116">-ParentObject</span></span>
<span data-ttu-id="dccaa-117">Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="dccaa-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="dccaa-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dccaa-118">-ParentResourceId</span></span>
<span data-ttu-id="dccaa-119">Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="dccaa-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="dccaa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dccaa-120">-ResourceGroupName</span></span>
<span data-ttu-id="dccaa-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dccaa-121">Resource Group name.</span></span>

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

### <span data-ttu-id="dccaa-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dccaa-122">-ServiceName</span></span>
<span data-ttu-id="dccaa-123">Keresés a szolgáltatásnévben</span><span class="sxs-lookup"><span data-stu-id="dccaa-123">Search Service name.</span></span>

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

### <span data-ttu-id="dccaa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccaa-124">CommonParameters</span></span>
<span data-ttu-id="dccaa-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccaa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccaa-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dccaa-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccaa-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dccaa-127">INPUTS</span></span>

### <span data-ttu-id="dccaa-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="dccaa-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="dccaa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dccaa-129">System.String</span></span>

## <span data-ttu-id="dccaa-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dccaa-130">OUTPUTS</span></span>

### <span data-ttu-id="dccaa-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="dccaa-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="dccaa-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dccaa-132">NOTES</span></span>

## <span data-ttu-id="dccaa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dccaa-133">RELATED LINKS</span></span>

[<span data-ttu-id="dccaa-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="dccaa-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="dccaa-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="dccaa-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)