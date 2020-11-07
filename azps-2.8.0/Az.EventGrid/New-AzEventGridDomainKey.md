---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 2ed323b9d454ca97bceaf27c00aab4460a792941
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666525"
---
# <span data-ttu-id="f3e81-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f3e81-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="f3e81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3e81-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e81-103">Újra létrehoz egy Azure-esemény rácsvonal-tartományának megosztott hozzáférési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="f3e81-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="f3e81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3e81-104">SYNTAX</span></span>

### <span data-ttu-id="f3e81-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3e81-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3e81-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3e81-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3e81-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3e81-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3e81-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3e81-108">DESCRIPTION</span></span>
<span data-ttu-id="f3e81-109">Újra létrehoz egy Azure-esemény rácsvonal-tartományának megosztott hozzáférési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="f3e81-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="f3e81-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f3e81-110">EXAMPLES</span></span>

### <span data-ttu-id="f3e81-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f3e81-111">Example 1</span></span>

<span data-ttu-id="f3e81-112">Újra létrehozhatja a kulcs key1 az \' esemény rácshoz tartozó \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f3e81-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="f3e81-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f3e81-113">Example 2</span></span>

<span data-ttu-id="f3e81-114">Újra létrehozhatja a kulcs key1 az \' esemény rácshoz tartozó \` Domain1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f3e81-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="f3e81-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="f3e81-115">Example 3</span></span>

<span data-ttu-id="f3e81-116">A \' \` \` \` \` teljes erőforrás-azonosítóval az erőforráscsoport MyResourceGroupName az esemény rácsvonalának azonosító2 tartozó "\" Domain1</span><span class="sxs-lookup"><span data-stu-id="f3e81-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="f3e81-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3e81-117">PARAMETERS</span></span>

### <span data-ttu-id="f3e81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e81-118">-DefaultProfile</span></span>
<span data-ttu-id="f3e81-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3e81-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3e81-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="f3e81-120">-DomainInputObject</span></span>
<span data-ttu-id="f3e81-121">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="f3e81-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="f3e81-122">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="f3e81-122">-DomainName</span></span>
<span data-ttu-id="f3e81-123">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="f3e81-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="f3e81-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="f3e81-124">-DomainResourceId</span></span>
<span data-ttu-id="f3e81-125">Az esemény rácsát jelképező erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f3e81-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="f3e81-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3e81-126">-Name</span></span>
<span data-ttu-id="f3e81-127">Annak a kulcsnak a neve, amelyet újra létre kell hoznia</span><span class="sxs-lookup"><span data-stu-id="f3e81-127">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="f3e81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e81-128">-ResourceGroupName</span></span>
<span data-ttu-id="f3e81-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3e81-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3e81-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3e81-130">-Confirm</span></span>
<span data-ttu-id="f3e81-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3e81-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3e81-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3e81-132">-WhatIf</span></span>
<span data-ttu-id="f3e81-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3e81-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3e81-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3e81-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3e81-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e81-135">CommonParameters</span></span>
<span data-ttu-id="f3e81-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3e81-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e81-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e81-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e81-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3e81-138">INPUTS</span></span>

### <span data-ttu-id="f3e81-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f3e81-139">System.String</span></span>

### <span data-ttu-id="f3e81-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="f3e81-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="f3e81-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3e81-141">OUTPUTS</span></span>

### <span data-ttu-id="f3e81-142">Microsoft. Azure. Management. EventGrid. models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f3e81-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="f3e81-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3e81-143">NOTES</span></span>

## <span data-ttu-id="f3e81-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3e81-144">RELATED LINKS</span></span>
