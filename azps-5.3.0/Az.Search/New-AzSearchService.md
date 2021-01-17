---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467190"
---
# <span data-ttu-id="608b4-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="608b4-101">New-AzSearchService</span></span>

## <span data-ttu-id="608b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="608b4-102">SYNOPSIS</span></span>
<span data-ttu-id="608b4-103">Létrehoz egy Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="608b4-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="608b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="608b4-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="608b4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="608b4-105">DESCRIPTION</span></span>
<span data-ttu-id="608b4-106">A **New-AzSearchService** parancsmag megadott paraméterekkel létrehoz egy Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="608b4-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="608b4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="608b4-107">EXAMPLES</span></span>

### <span data-ttu-id="608b4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="608b4-108">Example 1</span></span>
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

<span data-ttu-id="608b4-109">A parancs létrehoz egy Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="608b4-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="608b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="608b4-110">PARAMETERS</span></span>

### <span data-ttu-id="608b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608b4-111">-DefaultProfile</span></span>
<span data-ttu-id="608b4-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="608b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="608b4-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="608b4-113">-HostingMode</span></span>
<span data-ttu-id="608b4-114">Keresés szolgáltatás-üzemeltető módban.</span><span class="sxs-lookup"><span data-stu-id="608b4-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="608b4-115">-Location</span><span class="sxs-lookup"><span data-stu-id="608b4-115">-Location</span></span>
<span data-ttu-id="608b4-116">Keresés a szolgáltatás helyében</span><span class="sxs-lookup"><span data-stu-id="608b4-116">Search Service location.</span></span>

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

### <span data-ttu-id="608b4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="608b4-117">-Name</span></span>
<span data-ttu-id="608b4-118">Keresés a szolgáltatásnévben</span><span class="sxs-lookup"><span data-stu-id="608b4-118">Search Service name.</span></span>

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

### <span data-ttu-id="608b4-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="608b4-119">-PartitionCount</span></span>
<span data-ttu-id="608b4-120">Search Service partition count.</span><span class="sxs-lookup"><span data-stu-id="608b4-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="608b4-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="608b4-121">-ReplicaCount</span></span>
<span data-ttu-id="608b4-122">Keresési szolgáltatás replikaszáma</span><span class="sxs-lookup"><span data-stu-id="608b4-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="608b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="608b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="608b4-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="608b4-124">Resource Group name.</span></span>

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

### <span data-ttu-id="608b4-125">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="608b4-125">-Sku</span></span>
<span data-ttu-id="608b4-126">Keresési szolgáltatás termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="608b4-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="608b4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="608b4-127">-Confirm</span></span>
<span data-ttu-id="608b4-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="608b4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="608b4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="608b4-129">-WhatIf</span></span>
<span data-ttu-id="608b4-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="608b4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="608b4-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="608b4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="608b4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608b4-132">CommonParameters</span></span>
<span data-ttu-id="608b4-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="608b4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608b4-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="608b4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608b4-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="608b4-135">INPUTS</span></span>

### <span data-ttu-id="608b4-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="608b4-136">None</span></span>

## <span data-ttu-id="608b4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="608b4-137">OUTPUTS</span></span>

### <span data-ttu-id="608b4-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="608b4-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="608b4-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="608b4-139">NOTES</span></span>

## <span data-ttu-id="608b4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="608b4-140">RELATED LINKS</span></span>

[<span data-ttu-id="608b4-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="608b4-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="608b4-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="608b4-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="608b4-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="608b4-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)