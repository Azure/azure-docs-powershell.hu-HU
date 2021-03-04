---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 703b01ef012f77126e0db3d425cd892fa7256317
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924977"
---
# <span data-ttu-id="69c15-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="69c15-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="69c15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69c15-102">SYNOPSIS</span></span>
<span data-ttu-id="69c15-103">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="69c15-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="69c15-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69c15-104">SYNTAX</span></span>

### <span data-ttu-id="69c15-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69c15-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69c15-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c15-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69c15-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c15-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c15-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69c15-108">DESCRIPTION</span></span>
<span data-ttu-id="69c15-109">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="69c15-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="69c15-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69c15-110">EXAMPLES</span></span>

### <span data-ttu-id="69c15-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="69c15-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="69c15-112">Eltávolítja az Eseményrács \` tartomány1 tartományát \` a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="69c15-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="69c15-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="69c15-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="69c15-114">Eltávolítja az Eseményrács \` tartomány1 tartományát \` a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="69c15-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="69c15-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69c15-115">PARAMETERS</span></span>

### <span data-ttu-id="69c15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c15-116">-DefaultProfile</span></span>
<span data-ttu-id="69c15-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69c15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69c15-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69c15-118">-InputObject</span></span>
<span data-ttu-id="69c15-119">EventGrid Domain objektum.</span><span class="sxs-lookup"><span data-stu-id="69c15-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69c15-120">-Name</span><span class="sxs-lookup"><span data-stu-id="69c15-120">-Name</span></span>
<span data-ttu-id="69c15-121">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="69c15-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c15-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69c15-122">-PassThru</span></span>
<span data-ttu-id="69c15-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="69c15-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="69c15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c15-124">-ResourceGroupName</span></span>
<span data-ttu-id="69c15-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="69c15-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c15-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69c15-126">-ResourceId</span></span>
<span data-ttu-id="69c15-127">Az Eseményrács tartományt képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="69c15-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c15-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69c15-128">-Confirm</span></span>
<span data-ttu-id="69c15-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69c15-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69c15-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c15-130">-WhatIf</span></span>
<span data-ttu-id="69c15-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69c15-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69c15-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69c15-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69c15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c15-133">CommonParameters</span></span>
<span data-ttu-id="69c15-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c15-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69c15-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c15-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69c15-136">INPUTS</span></span>

### <span data-ttu-id="69c15-137">System.String</span><span class="sxs-lookup"><span data-stu-id="69c15-137">System.String</span></span>

### <span data-ttu-id="69c15-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="69c15-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="69c15-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c15-139">OUTPUTS</span></span>

### <span data-ttu-id="69c15-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69c15-140">System.Boolean</span></span>

## <span data-ttu-id="69c15-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69c15-141">NOTES</span></span>

## <span data-ttu-id="69c15-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69c15-142">RELATED LINKS</span></span>
