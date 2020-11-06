---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 00342fddd1a8755f22f925e25595ec36b9326c09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496095"
---
# <span data-ttu-id="0e8c5-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0e8c5-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="0e8c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8c5-103">Egy eventhub-fogyasztói csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e8c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e8c5-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e8c5-105">DESCRIPTION</span></span>
<span data-ttu-id="0e8c5-106">Egy fogyasztói csoportot hoz létre a megadott IotHub társított Eventhub.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="0e8c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0e8c5-107">EXAMPLES</span></span>

### <span data-ttu-id="0e8c5-108">1. példa: fogyasztói csoport felvétele a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="0e8c5-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="0e8c5-109">Egy "myconsumergroup" nevű új consumergroup ad a eventhub a telemetriai eseményeiről a iothub nevű "myiothub"-hoz.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="0e8c5-110">2. példa: fogyasztói csoport felvétele a műveletek figyelési eventhub</span><span class="sxs-lookup"><span data-stu-id="0e8c5-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="0e8c5-111">Egy "myconsumergroup" nevű új consumergroup ad a eventhub az "myiothub" nevű iothub műveletek figyelési eseményeihez.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="0e8c5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e8c5-112">PARAMETERS</span></span>

### <span data-ttu-id="0e8c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8c5-113">-DefaultProfile</span></span>
<span data-ttu-id="0e8c5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0e8c5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e8c5-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8c5-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="0e8c5-116">A felvenni kívánt EventHub-ConsumerGroup neve.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="0e8c5-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="0e8c5-117">-EventHubEndpointName</span></span>
<span data-ttu-id="0e8c5-118">A EventHub végpont neve.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="0e8c5-119">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="0e8c5-119">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="0e8c5-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e8c5-120">-Name</span></span>
<span data-ttu-id="0e8c5-121">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="0e8c5-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0e8c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e8c5-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="0e8c5-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e8c5-124">-Confirm</span></span>
<span data-ttu-id="0e8c5-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8c5-126">-WhatIf</span></span>
<span data-ttu-id="0e8c5-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8c5-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e8c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8c5-129">CommonParameters</span></span>
<span data-ttu-id="0e8c5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e8c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8c5-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e8c5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8c5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e8c5-132">INPUTS</span></span>

### <span data-ttu-id="0e8c5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0e8c5-133">System.String</span></span>

## <span data-ttu-id="0e8c5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e8c5-134">OUTPUTS</span></span>

### <span data-ttu-id="0e8c5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0e8c5-135">System.String</span></span>

## <span data-ttu-id="0e8c5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e8c5-136">NOTES</span></span>

## <span data-ttu-id="0e8c5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e8c5-137">RELATED LINKS</span></span>
