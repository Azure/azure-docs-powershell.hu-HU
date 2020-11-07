---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: d321892ef2ebbe8e50908a5d519f1990ebb875ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666247"
---
# <span data-ttu-id="0ffde-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0ffde-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="0ffde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ffde-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffde-103">Töröl egy eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="0ffde-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="0ffde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ffde-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ffde-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ffde-105">DESCRIPTION</span></span>
<span data-ttu-id="0ffde-106">Töröl egy eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="0ffde-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="0ffde-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ffde-107">EXAMPLES</span></span>

### <span data-ttu-id="0ffde-108">Példa 1 a eventhub consumergroup eltávolítása a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="0ffde-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="0ffde-109">Eltávolítja a myconsumergroup nevű consumergroup a "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="0ffde-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0ffde-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ffde-110">PARAMETERS</span></span>

### <span data-ttu-id="0ffde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffde-111">-DefaultProfile</span></span>
<span data-ttu-id="0ffde-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ffde-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ffde-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="0ffde-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="0ffde-114">EventHub ConsumerGroup név.</span><span class="sxs-lookup"><span data-stu-id="0ffde-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffde-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="0ffde-115">-EventHubEndpointName</span></span>
<span data-ttu-id="0ffde-116">EventHub végpont neve.</span><span class="sxs-lookup"><span data-stu-id="0ffde-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="0ffde-117">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="0ffde-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="0ffde-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ffde-118">-Name</span></span>
<span data-ttu-id="0ffde-119">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="0ffde-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="0ffde-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ffde-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ffde-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0ffde-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0ffde-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ffde-122">-Confirm</span></span>
<span data-ttu-id="0ffde-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ffde-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ffde-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ffde-124">-WhatIf</span></span>
<span data-ttu-id="0ffde-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ffde-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ffde-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ffde-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ffde-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffde-127">CommonParameters</span></span>
<span data-ttu-id="0ffde-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ffde-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffde-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ffde-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffde-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ffde-130">INPUTS</span></span>

### <span data-ttu-id="0ffde-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0ffde-131">System.String</span></span>

## <span data-ttu-id="0ffde-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ffde-132">OUTPUTS</span></span>

### <span data-ttu-id="0ffde-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0ffde-133">System.String</span></span>

## <span data-ttu-id="0ffde-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ffde-134">NOTES</span></span>

## <span data-ttu-id="0ffde-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ffde-135">RELATED LINKS</span></span>
