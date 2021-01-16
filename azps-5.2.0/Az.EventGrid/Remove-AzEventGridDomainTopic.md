---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363703"
---
# <span data-ttu-id="e3026-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e3026-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="e3026-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3026-102">SYNOPSIS</span></span>
<span data-ttu-id="e3026-103">Eltávolít egy Azure Event Grid-tartománytémát.</span><span class="sxs-lookup"><span data-stu-id="e3026-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="e3026-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3026-104">SYNTAX</span></span>

### <span data-ttu-id="e3026-105">DomainTopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3026-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3026-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3026-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3026-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3026-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3026-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3026-108">DESCRIPTION</span></span>
<span data-ttu-id="e3026-109">Eltávolít egy Azure Event Grid-tartománytémát.</span><span class="sxs-lookup"><span data-stu-id="e3026-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="e3026-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3026-110">EXAMPLES</span></span>

### <span data-ttu-id="e3026-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e3026-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="e3026-112">A MyResourceGroupName erőforráscsoport Domain Domain1 (Tartomány1) csoportjában található Event Grid \` \` Domain Topic \` \` \` Topic1 (Eseményrács-tartomány témakör1) \` eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e3026-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e3026-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e3026-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="e3026-114">A MyResourceGroupName erőforráscsoport Domain Domain1 (Tartomány1) csoportjában található Event Grid \` \` Domain Topic \` \` \` Topic1 (Eseményrács-tartomány témakör1) \` eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e3026-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e3026-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3026-115">PARAMETERS</span></span>

### <span data-ttu-id="e3026-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3026-116">-DefaultProfile</span></span>
<span data-ttu-id="e3026-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3026-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3026-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="e3026-118">-DomainName</span></span>
<span data-ttu-id="e3026-119">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="e3026-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3026-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3026-120">-InputObject</span></span>
<span data-ttu-id="e3026-121">EventGrid domain Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="e3026-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3026-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e3026-122">-Name</span></span>
<span data-ttu-id="e3026-123">EventGrid tartomány témakörének neve.</span><span class="sxs-lookup"><span data-stu-id="e3026-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3026-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3026-124">-PassThru</span></span>
<span data-ttu-id="e3026-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e3026-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3026-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3026-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3026-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3026-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3026-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3026-128">-ResourceId</span></span>
<span data-ttu-id="e3026-129">Az Eseményrács tartománytémát képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e3026-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3026-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3026-130">-Confirm</span></span>
<span data-ttu-id="e3026-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e3026-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3026-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3026-132">-WhatIf</span></span>
<span data-ttu-id="e3026-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e3026-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3026-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3026-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3026-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3026-135">CommonParameters</span></span>
<span data-ttu-id="e3026-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3026-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3026-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3026-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3026-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3026-138">INPUTS</span></span>

### <span data-ttu-id="e3026-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e3026-139">System.String</span></span>

### <span data-ttu-id="e3026-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e3026-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="e3026-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3026-141">OUTPUTS</span></span>

### <span data-ttu-id="e3026-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3026-142">System.Boolean</span></span>

## <span data-ttu-id="e3026-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3026-143">NOTES</span></span>

## <span data-ttu-id="e3026-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3026-144">RELATED LINKS</span></span>
