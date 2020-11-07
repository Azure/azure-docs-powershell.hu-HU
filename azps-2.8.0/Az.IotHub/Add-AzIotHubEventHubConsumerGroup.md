---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 938949ae1eada6d85bb6e01728f5be09655c3e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666301"
---
# <span data-ttu-id="b6131-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b6131-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b6131-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6131-102">SYNOPSIS</span></span>
<span data-ttu-id="b6131-103">Egy eventhub-fogyasztói csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b6131-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="b6131-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6131-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6131-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6131-105">DESCRIPTION</span></span>
<span data-ttu-id="b6131-106">Egy fogyasztói csoportot hoz létre a megadott IotHub társított Eventhub.</span><span class="sxs-lookup"><span data-stu-id="b6131-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="b6131-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6131-107">EXAMPLES</span></span>

### <span data-ttu-id="b6131-108">1. példa: fogyasztói csoport felvétele a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="b6131-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="b6131-109">Egy "myconsumergroup" nevű új consumergroup ad a eventhub a telemetriai eseményeiről a iothub nevű "myiothub"-hoz.</span><span class="sxs-lookup"><span data-stu-id="b6131-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="b6131-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6131-110">PARAMETERS</span></span>

### <span data-ttu-id="b6131-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6131-111">-DefaultProfile</span></span>
<span data-ttu-id="b6131-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b6131-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6131-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="b6131-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="b6131-114">A felvenni kívánt EventHub-ConsumerGroup neve.</span><span class="sxs-lookup"><span data-stu-id="b6131-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6131-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="b6131-115">-EventHubEndpointName</span></span>
<span data-ttu-id="b6131-116">A EventHub végpont neve.</span><span class="sxs-lookup"><span data-stu-id="b6131-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="b6131-117">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="b6131-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6131-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6131-118">-Name</span></span>
<span data-ttu-id="b6131-119">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="b6131-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b6131-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6131-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6131-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6131-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="b6131-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6131-122">-Confirm</span></span>
<span data-ttu-id="b6131-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6131-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6131-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6131-124">-WhatIf</span></span>
<span data-ttu-id="b6131-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6131-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6131-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6131-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6131-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6131-127">CommonParameters</span></span>
<span data-ttu-id="b6131-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6131-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6131-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6131-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6131-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6131-130">INPUTS</span></span>

### <span data-ttu-id="b6131-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b6131-131">System.String</span></span>

## <span data-ttu-id="b6131-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6131-132">OUTPUTS</span></span>

### <span data-ttu-id="b6131-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b6131-133">System.String</span></span>

## <span data-ttu-id="b6131-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6131-134">NOTES</span></span>

## <span data-ttu-id="b6131-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6131-135">RELATED LINKS</span></span>
