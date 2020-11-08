---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 2eb9fc2575af16f6f0bc2d6e239f63d95a0c27d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011429"
---
# <span data-ttu-id="52827-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="52827-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="52827-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52827-102">SYNOPSIS</span></span>
<span data-ttu-id="52827-103">Az Azure Event Grid-tartomány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="52827-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="52827-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52827-104">SYNTAX</span></span>

### <span data-ttu-id="52827-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52827-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52827-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="52827-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52827-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52827-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52827-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="52827-108">DESCRIPTION</span></span>
<span data-ttu-id="52827-109">Az Azure Event Grid-tartomány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="52827-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="52827-110">Példák</span><span class="sxs-lookup"><span data-stu-id="52827-110">EXAMPLES</span></span>

### <span data-ttu-id="52827-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="52827-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="52827-112">Eltávolítja az esemény rácsa tartományi \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="52827-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="52827-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="52827-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="52827-114">Eltávolítja az esemény rácsa tartományi \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="52827-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="52827-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52827-115">PARAMETERS</span></span>

### <span data-ttu-id="52827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52827-116">-DefaultProfile</span></span>
<span data-ttu-id="52827-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52827-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52827-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52827-118">-InputObject</span></span>
<span data-ttu-id="52827-119">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="52827-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="52827-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52827-120">-Name</span></span>
<span data-ttu-id="52827-121">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="52827-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52827-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52827-122">-PassThru</span></span>
<span data-ttu-id="52827-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="52827-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="52827-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52827-124">-ResourceGroupName</span></span>
<span data-ttu-id="52827-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52827-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52827-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52827-126">-ResourceId</span></span>
<span data-ttu-id="52827-127">Az esemény rácsát jelképező erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="52827-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="52827-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52827-128">-Confirm</span></span>
<span data-ttu-id="52827-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52827-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52827-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52827-130">-WhatIf</span></span>
<span data-ttu-id="52827-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52827-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52827-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52827-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52827-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52827-133">CommonParameters</span></span>
<span data-ttu-id="52827-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52827-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52827-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52827-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52827-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52827-136">INPUTS</span></span>

### <span data-ttu-id="52827-137">System. String</span><span class="sxs-lookup"><span data-stu-id="52827-137">System.String</span></span>

### <span data-ttu-id="52827-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="52827-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="52827-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52827-139">OUTPUTS</span></span>

### <span data-ttu-id="52827-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52827-140">System.Boolean</span></span>

## <span data-ttu-id="52827-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52827-141">NOTES</span></span>

## <span data-ttu-id="52827-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52827-142">RELATED LINKS</span></span>
