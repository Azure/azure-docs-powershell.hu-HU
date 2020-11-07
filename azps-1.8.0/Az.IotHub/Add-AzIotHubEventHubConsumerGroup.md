---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: c4378b156d17759c180ee3bf966bc20d06d00b41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835929"
---
# <span data-ttu-id="0d1ae-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0d1ae-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="0d1ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1ae-103">Egy eventhub-fogyasztói csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="0d1ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d1ae-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="0d1ae-106">Egy fogyasztói csoportot hoz létre a megadott IotHub társított Eventhub.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="0d1ae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0d1ae-107">EXAMPLES</span></span>

### <span data-ttu-id="0d1ae-108">1. példa: fogyasztói csoport felvétele a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="0d1ae-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="0d1ae-109">Egy "myconsumergroup" nevű új consumergroup ad a eventhub a telemetriai eseményeiről a iothub nevű "myiothub"-hoz.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="0d1ae-110">2. példa: fogyasztói csoport felvétele a műveletek figyelési eventhub</span><span class="sxs-lookup"><span data-stu-id="0d1ae-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="0d1ae-111">Egy "myconsumergroup" nevű új consumergroup ad a eventhub az "myiothub" nevű iothub műveletek figyelési eseményeihez.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="0d1ae-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d1ae-112">PARAMETERS</span></span>

### <span data-ttu-id="0d1ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1ae-113">-DefaultProfile</span></span>
<span data-ttu-id="0d1ae-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0d1ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d1ae-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1ae-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="0d1ae-116">A felvenni kívánt EventHub-ConsumerGroup neve.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="0d1ae-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="0d1ae-117">-EventHubEndpointName</span></span>
<span data-ttu-id="0d1ae-118">A EventHub végpont neve.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="0d1ae-119">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="0d1ae-119">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="0d1ae-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d1ae-120">-Name</span></span>
<span data-ttu-id="0d1ae-121">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="0d1ae-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0d1ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d1ae-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="0d1ae-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d1ae-124">-Confirm</span></span>
<span data-ttu-id="0d1ae-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d1ae-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1ae-126">-WhatIf</span></span>
<span data-ttu-id="0d1ae-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d1ae-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d1ae-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d1ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1ae-129">CommonParameters</span></span>
<span data-ttu-id="0d1ae-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d1ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1ae-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d1ae-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1ae-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d1ae-132">INPUTS</span></span>

### <span data-ttu-id="0d1ae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0d1ae-133">System.String</span></span>

## <span data-ttu-id="0d1ae-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d1ae-134">OUTPUTS</span></span>

### <span data-ttu-id="0d1ae-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0d1ae-135">System.String</span></span>

## <span data-ttu-id="0d1ae-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d1ae-136">NOTES</span></span>

## <span data-ttu-id="0d1ae-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d1ae-137">RELATED LINKS</span></span>
