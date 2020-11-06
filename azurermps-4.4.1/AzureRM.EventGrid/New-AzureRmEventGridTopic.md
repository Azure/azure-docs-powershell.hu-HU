---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: fdd15de19f921781e89d7e24b57e1d82632e4735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505052"
---
# <span data-ttu-id="60274-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="60274-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="60274-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60274-102">SYNOPSIS</span></span>
<span data-ttu-id="60274-103">Új Azure-esemény rácsvonal-témakörének létrehozása</span><span class="sxs-lookup"><span data-stu-id="60274-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60274-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60274-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60274-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60274-105">DESCRIPTION</span></span>
<span data-ttu-id="60274-106">Új Azure-esemény rácsvonal-témakörének létrehozása</span><span class="sxs-lookup"><span data-stu-id="60274-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="60274-107">Miután létrehozta a témát, az alkalmazás közzéteheti az eseményeket a téma végpontjának segítségével.</span><span class="sxs-lookup"><span data-stu-id="60274-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="60274-108">Példák</span><span class="sxs-lookup"><span data-stu-id="60274-108">EXAMPLES</span></span>

### <span data-ttu-id="60274-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="60274-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="60274-110">A \` \` megadott földrajzi hely \` westus2 \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény rácshoz tartozó téma1.</span><span class="sxs-lookup"><span data-stu-id="60274-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="60274-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="60274-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="60274-112">A megadott \` \` földrajzi hely \` westus2 \` , az erőforráscsoport \` MyResourceGroupName \` a megadott címkéket a "részleg" és a "környezet" téma1 hozza létre az esemény táblázatát.</span><span class="sxs-lookup"><span data-stu-id="60274-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="60274-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60274-113">PARAMETERS</span></span>

### <span data-ttu-id="60274-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="60274-114">-Location</span></span>
<span data-ttu-id="60274-115">A témakör helye</span><span class="sxs-lookup"><span data-stu-id="60274-115">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60274-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60274-116">-Name</span></span>
<span data-ttu-id="60274-117">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="60274-117">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60274-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60274-118">-ResourceGroupName</span></span>
<span data-ttu-id="60274-119">Az az erőforráscsoport, amelyben a témakört létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="60274-119">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60274-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="60274-120">-Tag</span></span>
<span data-ttu-id="60274-121">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="60274-121">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60274-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60274-122">-Confirm</span></span>
<span data-ttu-id="60274-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60274-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60274-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60274-124">-WhatIf</span></span>
<span data-ttu-id="60274-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60274-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60274-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60274-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60274-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60274-127">-DefaultProfile</span></span>
<span data-ttu-id="60274-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60274-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60274-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60274-129">CommonParameters</span></span>
<span data-ttu-id="60274-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60274-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60274-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60274-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60274-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60274-132">INPUTS</span></span>

### <span data-ttu-id="60274-133">System. String</span><span class="sxs-lookup"><span data-stu-id="60274-133">System.String</span></span>
<span data-ttu-id="60274-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="60274-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="60274-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60274-135">OUTPUTS</span></span>

### <span data-ttu-id="60274-136">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="60274-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="60274-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60274-137">NOTES</span></span>

## <span data-ttu-id="60274-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60274-138">RELATED LINKS</span></span>

