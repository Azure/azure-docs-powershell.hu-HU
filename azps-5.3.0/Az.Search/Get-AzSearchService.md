---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467194"
---
# <span data-ttu-id="b7f8c-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b7f8c-101">Get-AzSearchService</span></span>

## <span data-ttu-id="b7f8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f8c-103">Azure Search-szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="b7f8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7f8c-104">SYNTAX</span></span>

### <span data-ttu-id="b7f8c-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7f8c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7f8c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f8c-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7f8c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7f8c-107">DESCRIPTION</span></span>
<span data-ttu-id="b7f8c-108">A **Get-AzSearchService** parancsmag megkapja a megadott Azure Search szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="b7f8c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7f8c-109">EXAMPLES</span></span>

### <span data-ttu-id="b7f8c-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b7f8c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="b7f8c-111">Azure Search-szolgáltatás lekérte a megadott paramétereket.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="b7f8c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7f8c-112">PARAMETERS</span></span>

### <span data-ttu-id="b7f8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f8c-113">-DefaultProfile</span></span>
<span data-ttu-id="b7f8c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f8c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b7f8c-115">-Name</span></span>
<span data-ttu-id="b7f8c-116">Keresés a szolgáltatásnévben</span><span class="sxs-lookup"><span data-stu-id="b7f8c-116">Search Service name.</span></span>

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

### <span data-ttu-id="b7f8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7f8c-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-118">Resource Group name.</span></span>

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

### <span data-ttu-id="b7f8c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7f8c-119">-ResourceId</span></span>
<span data-ttu-id="b7f8c-120">Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b7f8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f8c-121">CommonParameters</span></span>
<span data-ttu-id="b7f8c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f8c-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f8c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f8c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7f8c-124">INPUTS</span></span>

### <span data-ttu-id="b7f8c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b7f8c-125">System.String</span></span>

## <span data-ttu-id="b7f8c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7f8c-126">OUTPUTS</span></span>

### <span data-ttu-id="b7f8c-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b7f8c-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="b7f8c-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7f8c-128">NOTES</span></span>

## <span data-ttu-id="b7f8c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7f8c-129">RELATED LINKS</span></span>

[<span data-ttu-id="b7f8c-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b7f8c-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="b7f8c-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b7f8c-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="b7f8c-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b7f8c-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)