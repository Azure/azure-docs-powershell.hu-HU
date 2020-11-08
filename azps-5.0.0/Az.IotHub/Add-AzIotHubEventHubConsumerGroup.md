---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187779"
---
# <span data-ttu-id="c4121-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c4121-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="c4121-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4121-102">SYNOPSIS</span></span>
<span data-ttu-id="c4121-103">Egy eventhub-fogyasztói csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c4121-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="c4121-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4121-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4121-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4121-105">DESCRIPTION</span></span>
<span data-ttu-id="c4121-106">Egy fogyasztói csoportot hoz létre a megadott IotHub társított Eventhub.</span><span class="sxs-lookup"><span data-stu-id="c4121-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="c4121-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c4121-107">EXAMPLES</span></span>

### <span data-ttu-id="c4121-108">1. példa: fogyasztói csoport felvétele a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="c4121-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="c4121-109">Egy "myconsumergroup" nevű új consumergroup ad a eventhub a telemetriai eseményeiről a iothub nevű "myiothub"-hoz.</span><span class="sxs-lookup"><span data-stu-id="c4121-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="c4121-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4121-110">PARAMETERS</span></span>

### <span data-ttu-id="c4121-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4121-111">-DefaultProfile</span></span>
<span data-ttu-id="c4121-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c4121-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4121-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="c4121-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="c4121-114">A felvenni kívánt EventHub-ConsumerGroup neve.</span><span class="sxs-lookup"><span data-stu-id="c4121-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4121-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4121-115">-Name</span></span>
<span data-ttu-id="c4121-116">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="c4121-116">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4121-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4121-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4121-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4121-118">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4121-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c4121-119">-Confirm</span></span>
<span data-ttu-id="c4121-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c4121-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4121-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4121-121">-WhatIf</span></span>
<span data-ttu-id="c4121-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c4121-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4121-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4121-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4121-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4121-124">CommonParameters</span></span>
<span data-ttu-id="c4121-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4121-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4121-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4121-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4121-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4121-127">INPUTS</span></span>

### <span data-ttu-id="c4121-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c4121-128">System.String</span></span>

## <span data-ttu-id="c4121-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4121-129">OUTPUTS</span></span>

### <span data-ttu-id="c4121-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c4121-130">System.String</span></span>

## <span data-ttu-id="c4121-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4121-131">NOTES</span></span>

## <span data-ttu-id="c4121-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4121-132">RELATED LINKS</span></span>
