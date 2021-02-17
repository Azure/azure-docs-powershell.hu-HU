---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: ba1f9372ffcf4a756debc02258a10b935581f377
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159930"
---
# <span data-ttu-id="7b1a6-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7b1a6-101">New-AzSearchService</span></span>

## <span data-ttu-id="7b1a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1a6-103">Létrehoz egy Azure Kognitív keresési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-103">Creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7b1a6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b1a6-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b1a6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b1a6-105">DESCRIPTION</span></span>
<span data-ttu-id="7b1a6-106">A **New-AzSearchService** parancsmag meghatározott paraméterekkel létrehoz egy Azure Kognitív keresési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-106">The **New-AzSearchService** cmdlet creates an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="7b1a6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b1a6-107">EXAMPLES</span></span>

### <span data-ttu-id="7b1a6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7b1a6-108">Example 1</span></span>
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

<span data-ttu-id="7b1a6-109">A parancs létrehoz egy Azure Kognitív keresési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-109">The command creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7b1a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b1a6-110">PARAMETERS</span></span>

### <span data-ttu-id="7b1a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1a6-111">-DefaultProfile</span></span>
<span data-ttu-id="7b1a6-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b1a6-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="7b1a6-113">-HostingMode</span></span>
<span data-ttu-id="7b1a6-114">Azure Kognitív keresési szolgáltatás üzemeltetési módja.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-114">Azure Cognitive Search Service hosting mode.</span></span>

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

### <span data-ttu-id="7b1a6-115">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7b1a6-115">-IdentityType</span></span>
<span data-ttu-id="7b1a6-116">(Nem kötelező) Azure Kognitív keresési szolgáltatás identitása (Nincs/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="7b1a6-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSIdentityType]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1a6-117">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="7b1a6-117">-IPRuleList</span></span>
<span data-ttu-id="7b1a6-118">(Nem kötelező) Azure Kognitív keresési szolgáltatás IP-szabályai</span><span class="sxs-lookup"><span data-stu-id="7b1a6-118">(Optional) Azure Cognitive Search Service IP rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1a6-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7b1a6-119">-Location</span></span>
<span data-ttu-id="7b1a6-120">Azure Kognitív keresési szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-120">Azure Cognitive Search Service location.</span></span>

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

### <span data-ttu-id="7b1a6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7b1a6-121">-Name</span></span>
<span data-ttu-id="7b1a6-122">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-122">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="7b1a6-123">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="7b1a6-123">-PartitionCount</span></span>
<span data-ttu-id="7b1a6-124">Azure Kognitív keresési szolgáltatás partíciószáma.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-124">Azure Cognitive Search Service partition count.</span></span>

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

### <span data-ttu-id="7b1a6-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="7b1a6-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="7b1a6-126">(Nem kötelező) Azure Kognitív keresési szolgáltatás nyilvános hálózati hozzáférés (engedélyezve/letiltva)</span><span class="sxs-lookup"><span data-stu-id="7b1a6-126">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSPublicNetworkAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1a6-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7b1a6-127">-ReplicaCount</span></span>
<span data-ttu-id="7b1a6-128">Azure Kognitív keresési szolgáltatás replikaszáma.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-128">Azure Cognitive Search Service replica count.</span></span>

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

### <span data-ttu-id="7b1a6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b1a6-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b1a6-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-130">Resource Group name.</span></span>

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

### <span data-ttu-id="7b1a6-131">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="7b1a6-131">-Sku</span></span>
<span data-ttu-id="7b1a6-132">Azure Kognitív keresési szolgáltatás termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-132">Azure Cognitive Search Service Sku.</span></span>

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

### <span data-ttu-id="7b1a6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b1a6-133">-Confirm</span></span>
<span data-ttu-id="7b1a6-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b1a6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b1a6-135">-WhatIf</span></span>
<span data-ttu-id="7b1a6-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b1a6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b1a6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1a6-138">CommonParameters</span></span>
<span data-ttu-id="7b1a6-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1a6-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b1a6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1a6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b1a6-141">INPUTS</span></span>

### <span data-ttu-id="7b1a6-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="7b1a6-142">None</span></span>

## <span data-ttu-id="7b1a6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b1a6-143">OUTPUTS</span></span>

### <span data-ttu-id="7b1a6-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7b1a6-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="7b1a6-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b1a6-145">NOTES</span></span>

## <span data-ttu-id="7b1a6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b1a6-146">RELATED LINKS</span></span>

[<span data-ttu-id="7b1a6-147">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7b1a6-147">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="7b1a6-148">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7b1a6-148">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="7b1a6-149">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7b1a6-149">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)