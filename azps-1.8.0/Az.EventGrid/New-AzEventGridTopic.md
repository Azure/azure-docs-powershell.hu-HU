---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 1922d399cf4b7c4fe1295f9a19409094ab5676c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670869"
---
# <span data-ttu-id="7f91c-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="7f91c-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="7f91c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f91c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f91c-103">Új Azure-esemény rácsvonal-témakörének létrehozása</span><span class="sxs-lookup"><span data-stu-id="7f91c-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="7f91c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f91c-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f91c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f91c-105">DESCRIPTION</span></span>
<span data-ttu-id="7f91c-106">Új Azure-esemény rácsvonal-témakörének létrehozása</span><span class="sxs-lookup"><span data-stu-id="7f91c-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="7f91c-107">Miután létrehozta a témát, az alkalmazás közzéteheti az eseményeket a téma végpontjának segítségével.</span><span class="sxs-lookup"><span data-stu-id="7f91c-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="7f91c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7f91c-108">EXAMPLES</span></span>

### <span data-ttu-id="7f91c-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7f91c-109">Example 1</span></span>
```
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="7f91c-110">A \` \` megadott földrajzi hely \` westus2 \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény rácshoz tartozó téma1.</span><span class="sxs-lookup"><span data-stu-id="7f91c-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7f91c-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="7f91c-111">Example 2</span></span>
```
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="7f91c-112">A megadott \` \` földrajzi hely \` westus2 \` , az erőforráscsoport \` MyResourceGroupName \` a megadott címkéket a "részleg" és a "környezet" téma1 hozza létre az esemény táblázatát.</span><span class="sxs-lookup"><span data-stu-id="7f91c-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="7f91c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f91c-113">PARAMETERS</span></span>

### <span data-ttu-id="7f91c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f91c-114">-DefaultProfile</span></span>
<span data-ttu-id="7f91c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f91c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f91c-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="7f91c-116">-Location</span></span>
<span data-ttu-id="7f91c-117">A témakör helye</span><span class="sxs-lookup"><span data-stu-id="7f91c-117">The location of the topic</span></span>

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

### <span data-ttu-id="7f91c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f91c-118">-Name</span></span>
<span data-ttu-id="7f91c-119">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="7f91c-119">The name of the topic.</span></span>

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

### <span data-ttu-id="7f91c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f91c-120">-ResourceGroupName</span></span>
<span data-ttu-id="7f91c-121">Az az erőforráscsoport, amelyben a témakört létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7f91c-121">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="7f91c-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="7f91c-122">-Tag</span></span>
<span data-ttu-id="7f91c-123">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="7f91c-123">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="7f91c-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f91c-124">-Confirm</span></span>
<span data-ttu-id="7f91c-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f91c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f91c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f91c-126">-WhatIf</span></span>
<span data-ttu-id="7f91c-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f91c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f91c-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f91c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f91c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f91c-129">CommonParameters</span></span>
<span data-ttu-id="7f91c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f91c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f91c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f91c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f91c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f91c-132">INPUTS</span></span>

### <span data-ttu-id="7f91c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7f91c-133">System.String</span></span>

### <span data-ttu-id="7f91c-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7f91c-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7f91c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f91c-135">OUTPUTS</span></span>

### <span data-ttu-id="7f91c-136">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7f91c-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="7f91c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f91c-137">NOTES</span></span>

## <span data-ttu-id="7f91c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f91c-138">RELATED LINKS</span></span>
