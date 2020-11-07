---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: b46c9be4c8731fa6b9082a8076dd9ae175e62422
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666516"
---
# <span data-ttu-id="8d299-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d299-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="8d299-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d299-102">SYNOPSIS</span></span>
<span data-ttu-id="8d299-103">Az Azure Event Grid-tartomány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8d299-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="8d299-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d299-104">SYNTAX</span></span>

### <span data-ttu-id="8d299-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d299-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d299-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d299-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d299-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d299-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d299-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d299-108">DESCRIPTION</span></span>
<span data-ttu-id="8d299-109">Az Azure Event Grid-tartomány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8d299-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="8d299-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8d299-110">EXAMPLES</span></span>

### <span data-ttu-id="8d299-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8d299-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="8d299-112">Eltávolítja az esemény rácsa tartományi \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8d299-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8d299-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8d299-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="8d299-114">Eltávolítja az esemény rácsa tartományi \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8d299-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="8d299-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d299-115">PARAMETERS</span></span>

### <span data-ttu-id="8d299-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d299-116">-DefaultProfile</span></span>
<span data-ttu-id="8d299-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d299-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d299-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d299-118">-InputObject</span></span>
<span data-ttu-id="8d299-119">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="8d299-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="8d299-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d299-120">-Name</span></span>
<span data-ttu-id="8d299-121">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="8d299-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="8d299-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d299-122">-PassThru</span></span>
<span data-ttu-id="8d299-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8d299-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8d299-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d299-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d299-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d299-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d299-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d299-126">-ResourceId</span></span>
<span data-ttu-id="8d299-127">Az esemény rácsát jelképező erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="8d299-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="8d299-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d299-128">-Confirm</span></span>
<span data-ttu-id="8d299-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d299-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d299-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d299-130">-WhatIf</span></span>
<span data-ttu-id="8d299-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d299-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d299-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d299-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d299-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d299-133">CommonParameters</span></span>
<span data-ttu-id="8d299-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d299-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d299-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d299-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d299-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d299-136">INPUTS</span></span>

### <span data-ttu-id="8d299-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8d299-137">System.String</span></span>

### <span data-ttu-id="8d299-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8d299-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="8d299-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d299-139">OUTPUTS</span></span>

### <span data-ttu-id="8d299-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d299-140">System.Boolean</span></span>

## <span data-ttu-id="8d299-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d299-141">NOTES</span></span>

## <span data-ttu-id="8d299-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d299-142">RELATED LINKS</span></span>
