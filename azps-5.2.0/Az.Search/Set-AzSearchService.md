---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340469"
---
# <span data-ttu-id="b049a-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b049a-101">Set-AzSearchService</span></span>

## <span data-ttu-id="b049a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b049a-102">SYNOPSIS</span></span>
<span data-ttu-id="b049a-103">Frissítsen egy Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b049a-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="b049a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b049a-104">SYNTAX</span></span>

### <span data-ttu-id="b049a-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b049a-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b049a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b049a-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b049a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b049a-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b049a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b049a-108">DESCRIPTION</span></span>
<span data-ttu-id="b049a-109">A **Set-AzSearchService** parancsmag módosítja az Azure Search szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b049a-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="b049a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b049a-110">EXAMPLES</span></span>

### <span data-ttu-id="b049a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b049a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="b049a-112">A példa 2-re módosítja az Azure Search szolgáltatás partíciók és replikaszámát.</span><span class="sxs-lookup"><span data-stu-id="b049a-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="b049a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b049a-113">PARAMETERS</span></span>

### <span data-ttu-id="b049a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b049a-114">-DefaultProfile</span></span>
<span data-ttu-id="b049a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b049a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b049a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b049a-116">-InputObject</span></span>
<span data-ttu-id="b049a-117">Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="b049a-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b049a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b049a-118">-Name</span></span>
<span data-ttu-id="b049a-119">Keresés a szolgáltatásnévben</span><span class="sxs-lookup"><span data-stu-id="b049a-119">Search Service name.</span></span>

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

### <span data-ttu-id="b049a-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b049a-120">-PartitionCount</span></span>
<span data-ttu-id="b049a-121">Search Service partition count.</span><span class="sxs-lookup"><span data-stu-id="b049a-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="b049a-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="b049a-122">-ReplicaCount</span></span>
<span data-ttu-id="b049a-123">Keresési szolgáltatás replikaszáma</span><span class="sxs-lookup"><span data-stu-id="b049a-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="b049a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b049a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b049a-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b049a-125">Resource Group name.</span></span>

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

### <span data-ttu-id="b049a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b049a-126">-ResourceId</span></span>
<span data-ttu-id="b049a-127">Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="b049a-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b049a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b049a-128">-Confirm</span></span>
<span data-ttu-id="b049a-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b049a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b049a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b049a-130">-WhatIf</span></span>
<span data-ttu-id="b049a-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b049a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b049a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b049a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b049a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b049a-133">CommonParameters</span></span>
<span data-ttu-id="b049a-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b049a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b049a-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b049a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b049a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b049a-136">INPUTS</span></span>

### <span data-ttu-id="b049a-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b049a-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="b049a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b049a-138">System.String</span></span>

## <span data-ttu-id="b049a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b049a-139">OUTPUTS</span></span>

### <span data-ttu-id="b049a-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b049a-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="b049a-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b049a-141">NOTES</span></span>

## <span data-ttu-id="b049a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b049a-142">RELATED LINKS</span></span>

[<span data-ttu-id="b049a-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b049a-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="b049a-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b049a-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="b049a-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b049a-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)