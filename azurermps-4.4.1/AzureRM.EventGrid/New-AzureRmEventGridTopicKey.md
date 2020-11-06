---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: bb9cd92ff614a944c144f056d8d59aa1d4239b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505051"
---
# <span data-ttu-id="3b1f7-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="3b1f7-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="3b1f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1f7-103">Újra létrehoz egy Azure-esemény rácsvonal-témakörének megosztott elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b1f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b1f7-104">SYNTAX</span></span>

### <span data-ttu-id="3b1f7-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b1f7-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b1f7-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1f7-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b1f7-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1f7-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b1f7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b1f7-108">DESCRIPTION</span></span>
<span data-ttu-id="3b1f7-109">Újra létrehoz egy Azure-esemény rácsvonal-témakörének megosztott elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="3b1f7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3b1f7-110">EXAMPLES</span></span>

### <span data-ttu-id="3b1f7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b1f7-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="3b1f7-112">Az \' \` \` erőforráscsoport-MyResourceGroupName az esemény rácshoz tartozó Key1 (az esemény rácsvonala \` \` ) téma1 tartozó kulcs ismételt létrehozása</span><span class="sxs-lookup"><span data-stu-id="3b1f7-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3b1f7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3b1f7-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="3b1f7-114">Az \' \` \` erőforráscsoport-MyResourceGroupName az esemény rácshoz tartozó Key1 (az esemény rácsvonala \` \` ) téma1 tartozó kulcs ismételt létrehozása</span><span class="sxs-lookup"><span data-stu-id="3b1f7-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3b1f7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b1f7-115">PARAMETERS</span></span>

### <span data-ttu-id="3b1f7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b1f7-116">-InputObject</span></span>
<span data-ttu-id="3b1f7-117">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="3b1f7-117">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1f7-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="3b1f7-118">-KeyName</span></span>
<span data-ttu-id="3b1f7-119">Annak a kulcsnak a neve, amelyet újra létre kell hoznia</span><span class="sxs-lookup"><span data-stu-id="3b1f7-119">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b1f7-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1f7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b1f7-122">-ResourceId</span></span>
<span data-ttu-id="3b1f7-123">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="3b1f7-124">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3b1f7-124">-TopicName</span></span>
<span data-ttu-id="3b1f7-125">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-125">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1f7-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b1f7-126">-Confirm</span></span>
<span data-ttu-id="3b1f7-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b1f7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b1f7-128">-WhatIf</span></span>
<span data-ttu-id="3b1f7-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b1f7-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b1f7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1f7-131">-DefaultProfile</span></span>
<span data-ttu-id="3b1f7-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b1f7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1f7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1f7-133">CommonParameters</span></span>
<span data-ttu-id="3b1f7-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b1f7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1f7-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b1f7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1f7-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b1f7-136">INPUTS</span></span>

### <span data-ttu-id="3b1f7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3b1f7-137">System.String</span></span>

## <span data-ttu-id="3b1f7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b1f7-138">OUTPUTS</span></span>

### <span data-ttu-id="3b1f7-139">Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3b1f7-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="3b1f7-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b1f7-140">NOTES</span></span>

## <span data-ttu-id="3b1f7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b1f7-141">RELATED LINKS</span></span>

