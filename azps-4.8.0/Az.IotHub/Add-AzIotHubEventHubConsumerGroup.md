---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181965"
---
# <span data-ttu-id="d1fa1-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d1fa1-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d1fa1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fa1-103">Egy eventhub-fogyasztói csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d1fa1-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="d1fa1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1fa1-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1fa1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1fa1-105">DESCRIPTION</span></span>
<span data-ttu-id="d1fa1-106">Egy fogyasztói csoportot hoz létre a megadott IotHub társított Eventhub.</span><span class="sxs-lookup"><span data-stu-id="d1fa1-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="d1fa1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d1fa1-107">EXAMPLES</span></span>

### <span data-ttu-id="d1fa1-108">1. példa: fogyasztói csoport felvétele a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="d1fa1-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="d1fa1-109">Egy "myconsumergroup" nevű új consumergroup ad a eventhub a telemetriai eseményeiről a iothub nevű "myiothub"-hoz.</span><span class="sxs-lookup"><span data-stu-id="d1fa1-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="d1fa1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1fa1-110">PARAMETERS</span></span>

### <span data-ttu-id="d1fa1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fa1-111">-DefaultProfile</span></span>
<span data-ttu-id="d1fa1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d1fa1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1fa1-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="d1fa1-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="d1fa1-114">A felvenni kívánt EventHub-ConsumerGroup neve.</span><span class="sxs-lookup"><span data-stu-id="d1fa1-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="d1fa1-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1fa1-115">-Name</span></span>
<span data-ttu-id="d1fa1-116">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="d1fa1-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d1fa1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1fa1-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1fa1-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d1fa1-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="d1fa1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1fa1-119">-Confirm</span></span>
<span data-ttu-id="d1fa1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1fa1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1fa1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1fa1-121">-WhatIf</span></span>
<span data-ttu-id="d1fa1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1fa1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1fa1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1fa1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1fa1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fa1-124">CommonParameters</span></span>
<span data-ttu-id="d1fa1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1fa1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fa1-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fa1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fa1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1fa1-127">INPUTS</span></span>

### <span data-ttu-id="d1fa1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d1fa1-128">System.String</span></span>

## <span data-ttu-id="d1fa1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1fa1-129">OUTPUTS</span></span>

### <span data-ttu-id="d1fa1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d1fa1-130">System.String</span></span>

## <span data-ttu-id="d1fa1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1fa1-131">NOTES</span></span>

## <span data-ttu-id="d1fa1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1fa1-132">RELATED LINKS</span></span>
