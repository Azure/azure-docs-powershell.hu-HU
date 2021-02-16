---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161627"
---
# <span data-ttu-id="850b1-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="850b1-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="850b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="850b1-102">SYNOPSIS</span></span>
<span data-ttu-id="850b1-103">Az Azure Event Grid-tartomány megosztott hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="850b1-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="850b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="850b1-104">SYNTAX</span></span>

### <span data-ttu-id="850b1-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="850b1-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="850b1-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="850b1-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="850b1-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="850b1-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="850b1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="850b1-108">DESCRIPTION</span></span>
<span data-ttu-id="850b1-109">Az Azure Event Grid-tartomány megosztott hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="850b1-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="850b1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="850b1-110">EXAMPLES</span></span>

### <span data-ttu-id="850b1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="850b1-111">Example 1</span></span>

<span data-ttu-id="850b1-112">A \' \` \` \` MyResourceGroupName erőforráscsoport Eseményrács tartomány1 kulcs1\\ kulcsának megfelelő kulcs újragenerálásával. \`</span><span class="sxs-lookup"><span data-stu-id="850b1-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="850b1-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="850b1-113">Example 2</span></span>

<span data-ttu-id="850b1-114">A \' \` \` \` MyResourceGroupName erőforráscsoport Eseményrács tartomány1 kulcs1\\ kulcsának megfelelő kulcs újragenerálásával. \`</span><span class="sxs-lookup"><span data-stu-id="850b1-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="850b1-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="850b1-115">Example 3</span></span>

<span data-ttu-id="850b1-116">A MyResourceGroupName erőforráscsoportban a \' \` \` \` MyResourceGroupName erőforráscsoportban a key key2\\ eseményrács tartományának megfelelő kulcsot a teljes erőforrás-azonosító használatával \` újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="850b1-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="850b1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="850b1-117">PARAMETERS</span></span>

### <span data-ttu-id="850b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="850b1-118">-DefaultProfile</span></span>
<span data-ttu-id="850b1-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="850b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="850b1-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="850b1-120">-DomainInputObject</span></span>
<span data-ttu-id="850b1-121">EventGrid Domain objektum.</span><span class="sxs-lookup"><span data-stu-id="850b1-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="850b1-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="850b1-122">-DomainName</span></span>
<span data-ttu-id="850b1-123">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="850b1-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="850b1-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="850b1-124">-DomainResourceId</span></span>
<span data-ttu-id="850b1-125">Az Eseményrács tartományt képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="850b1-125">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="850b1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="850b1-126">-Name</span></span>
<span data-ttu-id="850b1-127">Az újragenerálható kulcs neve</span><span class="sxs-lookup"><span data-stu-id="850b1-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="850b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="850b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="850b1-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="850b1-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="850b1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="850b1-130">-Confirm</span></span>
<span data-ttu-id="850b1-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="850b1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="850b1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="850b1-132">-WhatIf</span></span>
<span data-ttu-id="850b1-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="850b1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="850b1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="850b1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="850b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850b1-135">CommonParameters</span></span>
<span data-ttu-id="850b1-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="850b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850b1-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="850b1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850b1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="850b1-138">INPUTS</span></span>

### <span data-ttu-id="850b1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="850b1-139">System.String</span></span>

### <span data-ttu-id="850b1-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="850b1-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="850b1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="850b1-141">OUTPUTS</span></span>

### <span data-ttu-id="850b1-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="850b1-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="850b1-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="850b1-143">NOTES</span></span>

## <span data-ttu-id="850b1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="850b1-144">RELATED LINKS</span></span>
