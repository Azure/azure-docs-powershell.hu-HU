---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204150"
---
# <span data-ttu-id="b9595-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b9595-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="b9595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9595-102">SYNOPSIS</span></span>
<span data-ttu-id="b9595-103">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="b9595-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="b9595-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9595-104">SYNTAX</span></span>

### <span data-ttu-id="b9595-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9595-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9595-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9595-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9595-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9595-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9595-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9595-108">DESCRIPTION</span></span>
<span data-ttu-id="b9595-109">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="b9595-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="b9595-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9595-110">EXAMPLES</span></span>

### <span data-ttu-id="b9595-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b9595-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="b9595-112">Eltávolítja az Eseményrács \` tartomány1 tartományát \` a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="b9595-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b9595-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b9595-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="b9595-114">Eltávolítja az Eseményrács \` tartomány1 tartományát \` a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="b9595-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b9595-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9595-115">PARAMETERS</span></span>

### <span data-ttu-id="b9595-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9595-116">-DefaultProfile</span></span>
<span data-ttu-id="b9595-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9595-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9595-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9595-118">-InputObject</span></span>
<span data-ttu-id="b9595-119">EventGrid Domain objektum.</span><span class="sxs-lookup"><span data-stu-id="b9595-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="b9595-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b9595-120">-Name</span></span>
<span data-ttu-id="b9595-121">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="b9595-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="b9595-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9595-122">-PassThru</span></span>
<span data-ttu-id="b9595-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b9595-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b9595-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9595-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9595-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9595-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9595-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9595-126">-ResourceId</span></span>
<span data-ttu-id="b9595-127">Az Eseményrács tartományt képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b9595-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="b9595-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9595-128">-Confirm</span></span>
<span data-ttu-id="b9595-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b9595-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9595-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9595-130">-WhatIf</span></span>
<span data-ttu-id="b9595-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b9595-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9595-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9595-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9595-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9595-133">CommonParameters</span></span>
<span data-ttu-id="b9595-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9595-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9595-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9595-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9595-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9595-136">INPUTS</span></span>

### <span data-ttu-id="b9595-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b9595-137">System.String</span></span>

### <span data-ttu-id="b9595-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="b9595-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="b9595-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9595-139">OUTPUTS</span></span>

### <span data-ttu-id="b9595-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9595-140">System.Boolean</span></span>

## <span data-ttu-id="b9595-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9595-141">NOTES</span></span>

## <span data-ttu-id="b9595-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9595-142">RELATED LINKS</span></span>
