---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59e7652d8ca3b2e26246ba4f8924f6a6b9d48f96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493690"
---
# <span data-ttu-id="f122b-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f122b-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="f122b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f122b-102">SYNOPSIS</span></span>
<span data-ttu-id="f122b-103">Töröl egy eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="f122b-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f122b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f122b-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f122b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f122b-105">DESCRIPTION</span></span>
<span data-ttu-id="f122b-106">Töröl egy eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="f122b-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="f122b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f122b-107">EXAMPLES</span></span>

### <span data-ttu-id="f122b-108">Példa 1 a eventhub consumergroup eltávolítása a telemetriai eventhub</span><span class="sxs-lookup"><span data-stu-id="f122b-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="f122b-109">Eltávolítja a myconsumergroup nevű consumergroup a "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="f122b-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f122b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f122b-110">PARAMETERS</span></span>

### <span data-ttu-id="f122b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f122b-111">-DefaultProfile</span></span>
<span data-ttu-id="f122b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f122b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f122b-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="f122b-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="f122b-114">EventHub ConsumerGroup név.</span><span class="sxs-lookup"><span data-stu-id="f122b-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="f122b-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="f122b-115">-EventHubEndpointName</span></span>
<span data-ttu-id="f122b-116">EventHub végpont neve.</span><span class="sxs-lookup"><span data-stu-id="f122b-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="f122b-117">Események lehetséges értékei, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="f122b-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="f122b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f122b-118">-Name</span></span>
<span data-ttu-id="f122b-119">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="f122b-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="f122b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f122b-120">-ResourceGroupName</span></span>
<span data-ttu-id="f122b-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f122b-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f122b-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f122b-122">-Confirm</span></span>
<span data-ttu-id="f122b-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f122b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f122b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f122b-124">-WhatIf</span></span>
<span data-ttu-id="f122b-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f122b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f122b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f122b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f122b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f122b-127">CommonParameters</span></span>
<span data-ttu-id="f122b-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f122b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f122b-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f122b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f122b-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f122b-130">INPUTS</span></span>

### <span data-ttu-id="f122b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f122b-131">System.String</span></span>

## <span data-ttu-id="f122b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f122b-132">OUTPUTS</span></span>

### <span data-ttu-id="f122b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f122b-133">System.String</span></span>

## <span data-ttu-id="f122b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f122b-134">NOTES</span></span>

## <span data-ttu-id="f122b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f122b-135">RELATED LINKS</span></span>
