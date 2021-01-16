---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353693"
---
# <span data-ttu-id="fd721-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="fd721-101">New-AzSearchService</span></span>

## <span data-ttu-id="fd721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd721-102">SYNOPSIS</span></span>
<span data-ttu-id="fd721-103">Létrehoz egy Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="fd721-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="fd721-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd721-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd721-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd721-105">DESCRIPTION</span></span>
<span data-ttu-id="fd721-106">A **New-AzSearchService** parancsmag megadott paraméterekkel létrehoz egy Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="fd721-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="fd721-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd721-107">EXAMPLES</span></span>

### <span data-ttu-id="fd721-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd721-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="fd721-109">A parancs létrehoz egy Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="fd721-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="fd721-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd721-110">PARAMETERS</span></span>

### <span data-ttu-id="fd721-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd721-111">-DefaultProfile</span></span>
<span data-ttu-id="fd721-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd721-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd721-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="fd721-113">-HostingMode</span></span>
<span data-ttu-id="fd721-114">Keresés szolgáltatás-üzemeltető módban.</span><span class="sxs-lookup"><span data-stu-id="fd721-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd721-115">-Location</span><span class="sxs-lookup"><span data-stu-id="fd721-115">-Location</span></span>
<span data-ttu-id="fd721-116">Keresés a szolgáltatás helyében</span><span class="sxs-lookup"><span data-stu-id="fd721-116">Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd721-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fd721-117">-Name</span></span>
<span data-ttu-id="fd721-118">Keresés a szolgáltatásnévben</span><span class="sxs-lookup"><span data-stu-id="fd721-118">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd721-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="fd721-119">-PartitionCount</span></span>
<span data-ttu-id="fd721-120">Search Service partition count.</span><span class="sxs-lookup"><span data-stu-id="fd721-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="fd721-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="fd721-121">-ReplicaCount</span></span>
<span data-ttu-id="fd721-122">Keresési szolgáltatás replikaszáma</span><span class="sxs-lookup"><span data-stu-id="fd721-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="fd721-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd721-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd721-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd721-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd721-125">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="fd721-125">-Sku</span></span>
<span data-ttu-id="fd721-126">Keresési szolgáltatás termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="fd721-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd721-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd721-127">-Confirm</span></span>
<span data-ttu-id="fd721-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fd721-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd721-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd721-129">-WhatIf</span></span>
<span data-ttu-id="fd721-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fd721-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd721-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd721-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd721-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd721-132">CommonParameters</span></span>
<span data-ttu-id="fd721-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd721-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd721-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd721-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd721-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd721-135">INPUTS</span></span>

### <span data-ttu-id="fd721-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="fd721-136">None</span></span>

## <span data-ttu-id="fd721-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd721-137">OUTPUTS</span></span>

### <span data-ttu-id="fd721-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="fd721-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="fd721-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd721-139">NOTES</span></span>

## <span data-ttu-id="fd721-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd721-140">RELATED LINKS</span></span>

[<span data-ttu-id="fd721-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="fd721-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="fd721-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="fd721-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="fd721-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="fd721-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)