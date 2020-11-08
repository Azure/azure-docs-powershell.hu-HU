---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194412"
---
# <span data-ttu-id="ac6d4-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ac6d4-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="ac6d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6d4-103">Az Azure Event Grid-tartomány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="ac6d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac6d4-104">SYNTAX</span></span>

### <span data-ttu-id="ac6d4-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac6d4-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6d4-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6d4-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6d4-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6d4-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac6d4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac6d4-108">DESCRIPTION</span></span>
<span data-ttu-id="ac6d4-109">Az Azure Event Grid-tartomány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="ac6d4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ac6d4-110">EXAMPLES</span></span>

### <span data-ttu-id="ac6d4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac6d4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="ac6d4-112">Eltávolítja az esemény rácsa tartományi \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ac6d4-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ac6d4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ac6d4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="ac6d4-114">Eltávolítja az esemény rácsa tartományi \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ac6d4-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ac6d4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac6d4-115">PARAMETERS</span></span>

### <span data-ttu-id="ac6d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6d4-116">-DefaultProfile</span></span>
<span data-ttu-id="ac6d4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac6d4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac6d4-118">-InputObject</span></span>
<span data-ttu-id="ac6d4-119">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="ac6d4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac6d4-120">-Name</span></span>
<span data-ttu-id="ac6d4-121">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ac6d4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac6d4-122">-PassThru</span></span>
<span data-ttu-id="ac6d4-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ac6d4-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ac6d4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac6d4-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac6d4-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac6d4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac6d4-126">-ResourceId</span></span>
<span data-ttu-id="ac6d4-127">Az esemény rácsát jelképező erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="ac6d4-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac6d4-128">-Confirm</span></span>
<span data-ttu-id="ac6d4-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac6d4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac6d4-130">-WhatIf</span></span>
<span data-ttu-id="ac6d4-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac6d4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac6d4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6d4-133">CommonParameters</span></span>
<span data-ttu-id="ac6d4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac6d4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6d4-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ac6d4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6d4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac6d4-136">INPUTS</span></span>

### <span data-ttu-id="ac6d4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ac6d4-137">System.String</span></span>

### <span data-ttu-id="ac6d4-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ac6d4-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="ac6d4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac6d4-139">OUTPUTS</span></span>

### <span data-ttu-id="ac6d4-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac6d4-140">System.Boolean</span></span>

## <span data-ttu-id="ac6d4-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac6d4-141">NOTES</span></span>

## <span data-ttu-id="ac6d4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac6d4-142">RELATED LINKS</span></span>
